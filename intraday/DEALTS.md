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
https://api.fugle.tw/realtime/v0/intraday/dealts?symbolId=2884&apiToken=demo
```

### parameters

| Name | Type | Description |
|:--|:--|:--|
|  `symbolId` | string | 個股、指數識別代碼 |
|  `apiToken` | string | realtime api token |
|  `limit` | number | 限制最多回傳的資料筆數。預設值：50 |
|  `offset` | number | 指定從第幾筆後開始回傳。預設值：0 |

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
      },
      {
        "at": "2020-04-20T05:24:52.236Z",
        "price": 26.15,
        "unit": 3,
        "serial": 4424723
      },
      {
        "at": "2020-04-20T05:24:51.723Z",
        "price": 26.15,
        "unit": 1,
        "serial": 4424569
      },
      {
        "at": "2020-04-20T05:24:50.198Z",
        "price": 26.15,
        "unit": 2,
        "serial": 4424008
      },
      {
        "at": "2020-04-20T05:24:44.931Z",
        "price": 26.15,
        "unit": 1,
        "serial": 4422336
      },
      {
        "at": "2020-04-20T05:24:43.482Z",
        "price": 26.15,
        "unit": 1,
        "serial": 4421877
      },
      {
        "at": "2020-04-20T05:24:39.674Z",
        "price": 26.15,
        "unit": 4,
        "serial": 4420447
      },
      {
        "at": "2020-04-20T05:24:38.679Z",
        "price": 26.15,
        "unit": 2,
        "serial": 4420015
      },
      {
        "at": "2020-04-20T05:24:31.838Z",
        "price": 26.1,
        "unit": 4,
        "serial": 4417723
      },
      {
        "at": "2020-04-20T05:24:31.443Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4417612
      },
      {
        "at": "2020-04-20T05:24:30.579Z",
        "price": 26.1,
        "unit": 15,
        "serial": 4417279
      },
      {
        "at": "2020-04-20T05:24:30.271Z",
        "price": 26.1,
        "unit": 4,
        "serial": 4416951
      },
      {
        "at": "2020-04-20T05:24:27.809Z",
        "price": 26.1,
        "unit": 4,
        "serial": 4415905
      },
      {
        "at": "2020-04-20T05:24:26.166Z",
        "price": 26.15,
        "unit": 1,
        "serial": 4415372
      },
      {
        "at": "2020-04-20T05:24:22.192Z",
        "price": 26.15,
        "unit": 6,
        "serial": 4414077
      },
      {
        "at": "2020-04-20T05:24:19.428Z",
        "price": 26.1,
        "unit": 4,
        "serial": 4413226
      },
      {
        "at": "2020-04-20T05:24:12.409Z",
        "price": 26.15,
        "unit": 1,
        "serial": 4410988
      },
      {
        "at": "2020-04-20T05:24:07.503Z",
        "price": 26.1,
        "unit": 2,
        "serial": 4408951
      },
      {
        "at": "2020-04-20T05:24:07.499Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4408948
      },
      {
        "at": "2020-04-20T05:24:00.898Z",
        "price": 26.1,
        "unit": 3,
        "serial": 4406160
      },
      {
        "at": "2020-04-20T05:24:00.897Z",
        "price": 26.1,
        "unit": 5,
        "serial": 4406159
      },
      {
        "at": "2020-04-20T05:24:00.477Z",
        "price": 26.15,
        "unit": 7,
        "serial": 4405896
      },
      {
        "at": "2020-04-20T05:24:00.216Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4405733
      },
      {
        "at": "2020-04-20T05:23:59.665Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4405457
      },
      {
        "at": "2020-04-20T05:23:59.154Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4405301
      },
      {
        "at": "2020-04-20T05:23:52.018Z",
        "price": 26.15,
        "unit": 5,
        "serial": 4402763
      },
      {
        "at": "2020-04-20T05:23:51.998Z",
        "price": 26.15,
        "unit": 1,
        "serial": 4402754
      },
      {
        "at": "2020-04-20T05:23:51.986Z",
        "price": 26.1,
        "unit": 10,
        "serial": 4402742
      },
      {
        "at": "2020-04-20T05:23:51.055Z",
        "price": 26.1,
        "unit": 12,
        "serial": 4402280
      },
      {
        "at": "2020-04-20T05:23:50.614Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4402131
      },
      {
        "at": "2020-04-20T05:23:46.753Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4400398
      },
      {
        "at": "2020-04-20T05:23:43.450Z",
        "price": 26.1,
        "unit": 5,
        "serial": 4399265
      },
      {
        "at": "2020-04-20T05:23:43.248Z",
        "price": 26.15,
        "unit": 1,
        "serial": 4399208
      },
      {
        "at": "2020-04-20T05:23:41.611Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4398659
      },
      {
        "at": "2020-04-20T05:23:39.981Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4398038
      },
      {
        "at": "2020-04-20T05:23:37.624Z",
        "price": 26.15,
        "unit": 2,
        "serial": 4397311
      },
      {
        "at": "2020-04-20T05:23:36.768Z",
        "price": 26.1,
        "unit": 3,
        "serial": 4397046
      },
      {
        "at": "2020-04-20T05:23:32.590Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4395661
      },
      {
        "at": "2020-04-20T05:23:32.333Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4395601
      },
      {
        "at": "2020-04-20T05:23:32.054Z",
        "price": 26.15,
        "unit": 6,
        "serial": 4395512
      },
      {
        "at": "2020-04-20T05:23:29.085Z",
        "price": 26.1,
        "unit": 5,
        "serial": 4394267
      },
      {
        "at": "2020-04-20T05:23:28.974Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4394185
      },
      {
        "at": "2020-04-20T05:23:26.050Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4392971
      },
      {
        "at": "2020-04-20T05:23:26.045Z",
        "price": 26.1,
        "unit": 3,
        "serial": 4392968
      },
      {
        "at": "2020-04-20T05:23:24.235Z",
        "price": 26.1,
        "unit": 16,
        "serial": 4392324
      },
      {
        "at": "2020-04-20T05:23:23.537Z",
        "price": 26.1,
        "unit": 1,
        "serial": 4392184
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
|  `at` | ISO 8601 | 此筆成交時間 |
|  `price` | number | 此筆成交的價格 |
|  `unit` | number | 此筆成交的張數 |
|  `volume` | number |  此筆成交的成交量 |
|  `serial` | number |  此筆成交之序號 |
