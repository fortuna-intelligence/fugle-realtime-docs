# META

提供盤中個股/指數當日基本資訊

```
GET /intraday/meta
```

```
curl -X GET "https://api.fugle.tw/realtime/v0.2/intraday/meta?symbolId=2884&apiToken=demo" -H "accept: */*"
```

## Example

### request url
```
https://api.fugle.tw/realtime/v0.2/intraday/meta?symbolId=2884&apiToken=demo
```

### websocket
```
wss://api.fugle.tw/realtime/v0.2/intraday/meta?symbolId=2884&apiToken=demo
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
      "lastUpdatedAt": "2021-03-30T13:30:00.000+08:00"
    },
    "meta": {
      "isIndex": false,
      "nameZhTw": "玉山金",
      "industryZhTw": "金融保險",
      "priceReference": 26.2,
      "priceHighLimit": 28.8,
      "priceLowLimit": 23.6,
      "canDayBuySell": true,
      "canDaySellBuy": true,
      "canShortMargin": true,
      "canShortLend": true,
      "volumePerUnit": 1000,
      "currency": "TWD",
      "isTerminated": false,
      "isSuspended": false,
      "isWarrant": false,
      "typeZhTw": "一般股票",
      "abnormal": "正常"
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
|  `mode` | string | 市場別 |
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
|  `abnormal` | string | 警示或處置股標示 (正常、注意、處置、注意及處置、再次處置、注意及再次處置、彈性處置、注意及彈性處置) |
