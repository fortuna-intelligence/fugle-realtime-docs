# QUOTE

提供盤中個股/指數逐筆交易金額、狀態、最佳五檔及統計資訊

```
GET /intraday/quote
```

```
curl -X GET "https://api.fugle.tw/realtime/v0.2/intraday/quote?symbolId=2884&apiToken=demo" -H "accept: */*"
```

## Example

### request url
```
https://api.fugle.tw/realtime/v0.2/intraday/quote?symbolId=2884&apiToken=demo
```

### websocket
```
wss://api.fugle.tw/realtime/v0.2/intraday/quote?symbolId=2884&apiToken=demo
```

### parameters
| Name | Type | Required | Description |
|:--|:--|:--|:--|
|  `symbolId` | string | yes | 個股、指數識別代碼 |
|  `apiToken` | string | yes | personal api token |
|  `oddLot` | boolean | no | 設置 `true` 回傳零股行情。預設值：`false` |

### response
```json
{
  "apiVersion": "0.2.0",
  "data": {
    "info": {
      "date": "2021-03-30",
      "mode": "twse-sem",
      "symbolId": "2884",
      "countryCode": "TW",
      "timeZone": "Asia/Taipei",
      "lastUpdatedAt": "2021-03-30T16:32:44.848+08:00"
    },
    "quote": {
      "isCurbing": false,
      "isCurbingRise": false,
      "isCurbingFall": false,
      "isTrial": false,
      "isOpenDelayed": false,
      "isCloseDelayed": false,
      "isClosed": true,
      "total": {
        "at": "2021-03-30T13:30:00.000+08:00",
        "unit": 25421,
        "volume": 25421000
      },
      "trade": {
        "at": "2021-03-30T13:30:00.000+08:00",
        "price": 26.2,
        "unit": 2766,
        "volume": 2766000,
        "serial": 6333245
      },
      "order": {
        "at": "2021-03-30T13:30:00.000+08:00",
        "bestBids": [
          {
            "price": 26.15,
            "unit": 193,
            "volume": 193000
          }
        ],
        "bestAsks": [
          {
            "price": 26.2,
            "unit": 3253,
            "volume": 3253000
          }
        ]
      },
      "priceHigh": {
        "price": 26.25,
        "at": "2021-03-30T09:00:16.280+08:00"
      },
      "priceLow": {
        "price": 26.05,
        "at": "2021-03-30T09:48:51.546+08:00"
      },
      "priceOpen": {
        "price": 26.2,
        "at": "2021-03-30T09:00:11.082+08:00"
      },
      "change": 0,
      "changePercent": 0,
      "amplitude": 0.00190839694656,
      "priceLimit": "NORMAL"
    }
  }
}
```

## Schema
| Name | Type | Description |
|:--|:--|:--|
|  `apiVersion` | string |  api version |
|  `data` | [data object](#data-object) |  - |

### data object
| Name | Type | Description |
|:--|:--|:--|
|  `info` | [info object](#info-object) | - |
|  `quote` | [quote object](#quote-object) | -  |


### info object
| Name | Type | Description |
|:--|:--|:--|
|  `lastUpdatedAt` | ISO 8601 | 本筆資料最後更新時間 |
|  `date` | string | 本筆資料所屬日期 |
|  `mode` | string | 交易所-交易市場 |
|  `symbolId` | string | 股票代號 |
|  `countryCode` | string | 股票所屬國家ISO2代碼 |
|  `timeZone` | string | 股票所屬時區 |


### quote object
| Name | Type | Description |
|:--|:--|:--|
|  `isCurbing` | boolean | 最近一次更新是否為瞬間價格穩定措施 |
|  `isCurbingRise` | boolean | 最近一次更新是否為暫緩撮合且瞬間趨漲 |
|  `isCurbingFall` | boolean | 最近一次更新是否為暫緩撮合且瞬間趨跌 |
|  `isTrial` | boolean |  最近一次更新是否為試算 |
|  `isOpenDelayed` | boolean | 當日是否曾發生延後開盤 |
|  `isCloseDelayed` | boolean | 當日是否曾發生延後收盤 |
|  `isHalting` | boolean | 最近一次更新是否為暫停交易 |
|  `isClosed` | boolean | 當日是否為已收盤 |
|  `change` | number | 當日股價之漲跌 |
|  `changePercent` | number | 當日股價之漲跌幅 |
|  `amplitude` | number | 當日股價之振幅 |
|  `total` | [total object](#total-object) |   |
|  `trial` | [trial object](#trial-object) |   |
|  `trade` | [trade object](#trade-object) |   |
|  `order` | [order object](#order-object) |   |
|  `priceHigh` | [price object](#price-object) | 當日之最高價<br/>第一次到達當日最高價之時間 |
|  `priceLow` | [price object](#price-object) | 當日之最低價<br/>第一次到達當日最低價之時間 |
|  `priceOpen` | [price object](#price-object) | 當日之開盤價，開盤定義：當天第一筆成交時才開盤<br/>當日第一筆成交時間 |


### total object
| Name | Type | Description |
|:--|:--|:--|
|  `at` | ISO 8601 | 最新一筆成交時間  |
|  `order` | number |  總成交委託, 負數表示無 order |
|  `price` | number |  總成交價, 負數表示無 price |
|  `unit` | number |  總成交張數 |
|  `volume` | number |  總成交量 |


### trial object
| Name | Type | Description |
|:--|:--|:--|
|  `at` | ISO 8601 | 最新一筆試撮時間  |
|  `price` | number |  最新一筆試撮價格 |
|  `unit` | number |  最新一筆試撮張數 |
|  `volume` | number |  最新一筆試撮成交量 |


### trade object
| Name | Type | Description |
|:--|:--|:--|
|  `at` | ISO 8601 | 最新一筆成交時間  |
|  `price` | number |  最新一筆成交價格 |
|  `unit` | number |  最新一筆成交張數 |
|  `volume` | number |  最新一筆成交之成交量 |
|  `serial` | number |  最新一筆成交之序號 |


### order object
| Name | Type | Description |
|:--|:--|:--|
|  `at` | ISO 8601 | 最新一筆最佳五檔更新時間  |
|  `bestBids` | [[best price object](#best-price-object)] |   |
|  `bestAsks` | [[best price object](#best-price-object)] |   |


#### best price object
| Name | Type | Description |
|:--|:--|:--|
|  `price` | number | 價格  |
|  `unit` | number |  張數 |
|  `volume` | number | 量 |

#### price object
| Name | Type | Description |
|:--|:--|:--|
|  `price` | number | 價格  |
|  `at` | ISO 8601 |  時間 |