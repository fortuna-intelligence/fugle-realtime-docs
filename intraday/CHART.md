# CHART

提供盤中個股/指數 線圖時所需的各項即時資訊

```
GET /intraday/chart
```

```
curl -X GET "https://api.fugle.tw/realtime/v0.2/intraday/chart?symbolId=2884&apiToken=demo" -H "accept: */*"
```

## Example

### request url
```
https://api.fugle.tw/realtime/v0.2/intraday/chart?symbolId=2884&apiToken=demo
```

### websocket
```
wss://api.fugle.tw/realtime/v0.2/intraday/chart?symbolId=2884&apiToken=demo
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
    "chart": {
      "2021-03-30T13:30:00.000+08:00": {
        "open": 26.2,
        "high": 26.2,
        "low": 26.2,
        "close": 26.2,
        "volume": 2766000,
        "unit": 2766
      }
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
|  `chart` | [chart object](#chart-object) | -  |


### info object
| Name | Type | Description |
|:--|:--|:--|
|  `lastUpdatedAt` | ISO 8601 | 本筆資料最後更新時間 |
|  `date` | string | 本筆資料所屬日期 |
|  `mode` | string | 交易所-交易市場 |
|  `symbolId` | string | 股票代號 |
|  `countryCode` | string | 股票所屬國家ISO2代碼 |
|  `timeZone` | string | 股票所屬時區 |


### chart object
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