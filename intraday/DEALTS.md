# DEALTS

取得個股當日所有成交資訊（ex: 個股價量、大盤總量）

```
GET /intraday/dealts
```

```
curl -X GET "https://api.fugle.tw/realtime/v0/intraday/dealts?symbolId=2884&apiToken=demo" -H "accept: */*"
```

## Example

### request url
```
https://api.fugle.tw/realtime/v0/intraday/dealts?symbolId=2884&apiToken=demo&limit=5
```

### parameters
| Name | Type | Required | Description |
|:--|:--|:--|:--|
|  `symbolId` | string | yes | 個股、指數識別代碼 |
|  `apiToken` | string | yes | realtime api token |
|  `limit` | number | no | 限制最多回傳的資料筆數。預設值：50 |
|  `offset` | number | no | 指定從第幾筆後開始回傳。預設值：0 |

### response
```json
{
  "apiVersion": "0.0.0",
  "data": {
    "info": {
      "countryCode": "TW",
      "timeZone": "Asia/Taipei",
      "date": "2020-04-20",
      "mode": "twse-sem",
      "symbolId": "2884"
    },
    "dealts": [
      {
        "at": "2020-04-20T05:30:00.000Z",
        "price": 26.2,
        "unit": 1950,
        "serial": 4450756
      },
      {
        "at": "2020-04-20T05:24:59.754Z",
        "price": 26.15,
        "unit": 5,
        "serial": 4427494
      },
      {
        "at": "2020-04-20T05:24:55.345Z",
        "price": 26.1,
        "unit": 3,
        "serial": 4426051
      },
      {
        "at": "2020-04-20T05:24:55.295Z",
        "price": 26.1,
        "unit": 3,
        "serial": 4425977
      },
      {
        "at": "2020-04-20T05:24:52.250Z",
        "price": 26.1,
        "unit": 15,
        "serial": 4424733
      }
    ]
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
|  `dealts` | [[dealt object](#dealt-object)] | -  |

### info object
| Name | Type | Description |
|:--|:--|:--|
|  `date` | string | 本筆資料所屬日期 |
|  `mode` | string | 交易所-交易市場 |
|  `symbolId` | string | 股票代號 |
|  `countryCode` | string | 股票所屬國家ISO2代碼 |
|  `timeZone` | string | 股票所屬時區 |

### dealt object
| Name | Type | Description |
|:--|:--|:--|
|  `at` | ISO 8601 | 此筆交易的成交時間 |
|  `price` | number | 此筆交易的成交價格 |
|  `unit` | number | 此筆交易的成交張數 (上市、上櫃股票) |
|  `volume` | number |  此筆交易的成交股數 (興櫃股票) |
|  `serial` | number |  此筆交易的序號 |
