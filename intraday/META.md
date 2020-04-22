# META

提供盤中個股/指數當日基本資訊

```
GET /intraday/meta
```

```
curl -X GET "https://api.fugle.tw/realtime/v0/intraday/meta?symbolId=2884&apiToken=demo" -H "accept: */*"
```

## Example

### request url
```
https://api.fugle.tw/realtime/v0/intraday/meta?symbolId=2884&apiToken=demo
```

### websocket
```
wss://api.fugle.tw/realtime/v0/intraday/meta?symbolId=2884&apiToken=demo
```

### parameters
| Name | Type | Required | Description |
|:--|:--|:--|:--|
|  `symbolId` | string | yes | 個股、指數識別代碼 |
|  `apiToken` | string | yes | personal api token |

### response
```json
{
  "apiVersion": "0.0.0",
  "data": {
    "info": {
      "lastUpdatedAt": "2018-07-10T23:33:02.690Z",
      "date": "2018-07-11",
      "mode": "twse-sem",
      "symbolId": "2330",
      "countryCode": "TW",
      "timeZone": "Asia/Taipei"
    },
    "meta": {
      "isIndex": false,
      "nameZhTw": "台積電",
      "industryZhTw": "半導體業",
      "priceReference": 222,
      "priceHighLimit": 244,
      "priceLowLimit": 200,
      "canDayBuySell": true,
      "canDaySellBuy": true,
      "canShortMargin": true,
      "canShortLend": true,
      "volumePerUnit": 1000,
      "currency": "TWD",
      "isTerminated": false,
      "isSuspended": false,
      "isWarrant": false,
      "typeZhTw": "一般股票"
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
|  `meta` | [meta object](#meta-object) | -  |

### info object
| Name | Type | Description |
|:--|:--|:--|
|  `lastUpdatedAt` | ISO 8601 | 本筆資料最後更新時間 |
|  `date` | string | 本筆資料所屬日期 |
|  `mode` | string | 交易所-交易市場 |
|  `symbolId` | string | 股票代號 |
|  `countryCode` | string | 股票所屬國家ISO2代碼 |
|  `timeZone` | string | 股票所屬時區 |

### meta object
| Name | Type | Description |
|:--|:--|:--|
|  `isIndex` | boolean |  是否為指數 |
|  `nameZhTw` | string | 股票中文簡稱 |
|  `industryZhTw` | string | 產業別 |
|  `priceReference` | number | 今日參考價 |
|  `priceHighLimit` | number | 漲停價 |
|  `priceLowLimit` | number | 跌停價 |
|  `canDayBuySell` | boolean | 是否可先買後賣現股當沖 |
|  `canDaySellBuy` | boolean | 是否可先賣後買現股當沖 |
|  `canShortMargin` | boolean | 是否豁免平盤下融券賣出 |
|  `canShortLend` | boolean | 是否豁免平盤下借券賣出 |
|  `volumePerUnit` | integer | 交易單位：股/張 |
|  `currency` | string | 交易幣別代號 |
|  `isTerminated` | boolean | 今日是否已終止上市 |
|  `isSuspended` | boolean | 今日是否暫停買賣 |
|  `isWarrant` | boolean | 是否為權證 |
|  `typeZhTw` | string | 股票類別 |