# QUOTE

提供盤中個股/指數逐筆交易金額、狀態、最佳五檔及統計資訊

```
GET /intraday/quote
```

```
curl -X GET "https://api.fugle.tw/realtime/v0/intraday/quote?symbolId=2884&apiToken=demo" -H "accept: */*"
```

### Example of request url
```
https://api.fugle.tw/realtime/v0/intraday/quote?symbolId=2884&apiToken=demo
```

### Example of websocket
```
wss://api.fugle.tw/realtime/v0/intraday/quote?symbolId=2884&apiToken=demo
```

### Example of response
```json
{
  "apiVersion": "0.0.0",
  "data": {
    "info": {
      "lastUpdatedAt": "2018-07-10T23:33:02.690Z",
      "date": "2018-07-11",
      "mode": "twse-sem",
      "symbolId": "2330",
      "countryCode": "TW ",
      "timeZone": "Asia/Taipei"
    },
    "quote": {
      "isCurbing": false,
      "isTrial": false,
      "isOpenDelayed": false,
      "isCloseDelayed": false,
      "isHalting": false,
      "isClosed": false,
      "total": {
        "at": "2018-07-11T05:30:00.000Z",
        "order": -1,
        "price": -1,
        "unit": 19816,
        "volume": 19816000
      },
      "trial": {
        "at": "2018-07-11T05:29:58.269Z",
        "price": 220,
        "unit": 4304,
        "volume": 4304000
      },
      "trade": {
        "at": "2018-07-11T05:30:00.000Z",
        "price": 220,
        "unit": 4304,
        "volume": 4304000,
        "serial": 919386
      },
      "order": {
        "at": "2018-07-11T05:30:00.000Z",
        "bestBids": [
            {
              "price": 217.5,
              "unit": 734,
              "volume": 734000
            }
        ],
        "bestAsks": [
          {
            "price": 220,
            "unit": 411,
            "volume": 411000
          }
        ]
      },
      "priceHigh": {
        "price": 220,
        "at": "2018-07-11T04:16:46.286Z"
      },
      "priceLow": {
        "price": 218,
        "at": "2018-07-11T04:17:31.419Z"
      },
      "priceOpen": {
        "price": 220,
        "at": "2018-07-11T01:00:01.284Z"
      }
    }
  }
}
```

### Schema
| Name | Type | Description |
|:--|:--|:--|
|  `apiVersion` | string |  api version |
|  `data` | [data object](#data-object) |  - |

#### data object
| Name | Type | Description |
|:--|:--|:--|
|  `info` | [info object](#info-object) | - |
|  `quote` | [quote object](#quote-object) | -  |


#### info object
| Name | Type | Description |
|:--|:--|:--|
|  `lastUpdatedAt` | ISO 8601 | 本筆資料最後更新時間 |
|  `date` | string | 本筆資料所屬日期 |
|  `mode` | string | 交易所-交易市場 |
|  `symbolId` | string | 股票代號 |
|  `countryCode` | string | 股票所屬國家ISO2代碼 |
|  `timeZone` | string | 股票所屬時區 |


#### quote object
| Name | Type | Description |
|:--|:--|:--|
|  `isCurbing` | boolean | 最近一次更新是否為瞬間價格穩定措施 |
|  `isTrial` | boolean |  最近一次更新是否為試算 |
|  `isOpenDelayed` | boolean | 當日是否曾發生延後開盤 |
|  `isCloseDelayed` | boolean | 當日是否曾發生延後收盤 |
|  `isHalting` | boolean | 最近一次更新是否為暫停交易 |
|  `isClosed` | boolean | 當日是否為已收盤 |
|  `total` | [total object](#total-object) |   |
|  `trial` | [trial object](#trial-object) |   |
|  `trade` | [trade object](#trade-object) |   |
|  `order` | [order object](#order-object) |   |
|  `priceHigh` | [price object](#price-object) | 當日之最高價<br/>第一次到達當日最高價之時間 |
|  `priceLow` | [price object](#price-object) |  當日之最低價<br/>第一次到達當日最低價之時間 |
|  `priceOpen` | [price object](#price-object) |  當日之開盤價，開盤定義：當天第一筆成交時才開盤<br/>當日第一筆成交時間 |


#### total object
| Name | Type | Description |
|:--|:--|:--|
|  `at` | ISO 8601 | 最新一筆成交時間  |
|  `order` | number |  總成交委託, 負數表示無 order |
|  `price` | number |  總成交價, 負數表示無 price |
|  `unit` | number |  總成交張數 |
|  `volume` | number |  總成交量 |


#### trial object
| Name | Type | Description |
|:--|:--|:--|
|  `at` | ISO 8601 | 最新一筆試撮時間  |
|  `price` | number |  最新一筆試撮價格 |
|  `unit` | number |  最新一筆試撮張數 |
|  `volume` | number |  最新一筆試撮成交量 |


#### trade object
| Name | Type | Description |
|:--|:--|:--|
|  `at` | ISO 8601 | 最新一筆成交時間  |
|  `price` | number |  最新一筆成交價格 |
|  `unit` | number |  最新一筆成交張數 |
|  `volume` | number |  最新一筆成交之成交量 |
|  `serial` | number |  最新一筆成交之序號 |


#### order object
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