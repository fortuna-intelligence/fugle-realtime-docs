# CHART

提供盤中個股/指數 線圖時所需的各項即時資訊

```
GET /intraday/chart
```

```
curl -X GET "https://api.fugle.tw/realtime/v0/intraday/chart?symbolId=2884&apiToken=demo" -H "accept: */*"
```

### Example of request url
```
https://api.fugle.tw/realtime/v0/intraday/chart?symbolId=2884&apiToken=demo
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
      "countryCode": "TW",
      "timeZone": "Asia/Taipei"
    },
    "chart": {
      "2018-07-11T05:30:00.000Z": {
        "open": 102.12,
        "high": 102.15,
        "low": 102.02,
        "close": 102.12,
        "unit": 2493,
        "volume": 2493000
      },
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
|  `chart` | [chart object](#chart-object) | -  |


#### info object
| Name | Type | Description |
|:--|:--|:--|
|  `lastUpdatedAt` | ISO 8601 | 本筆資料最後更新時間 |
|  `date` | string | 本筆資料所屬日期 |
|  `mode` | string | 交易所-交易市場 |
|  `symbolId` | string | 股票代號 |
|  `countryCode` | string | 股票所屬國家ISO2代碼 |
|  `timeZone` | string | 股票所屬時區 |


#### chart object
| Name | Type | Description |
|:--|:--|:--|
|  `dateTimeKey` | [price object](#price-object) | - |


#### price object
| Name | Type | Description |
|:--|:--|:--|
|  `open` | number | 此分鐘的開盤價 |
|  `high` | number | 此分鐘的最高價 |
|  `low` | number | 此分鐘的最低價 |
|  `close` | number | 此分鐘的收盤價 |
|  `unit` | number | 此分鐘的交易張數 |
|  `volume` | number | 此分鐘的交易量 |