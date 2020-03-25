# Fugle Realtime API

Fugle Realtime API 是由時報資訊與[Fugle](https://www.fugle.tw/) 技術團隊開發提供，詳細文件請參閱[Document](./DOCUMENT.md)。  
即時行情資料來源為臺灣證券交易所、臺灣期貨交易所及財團法人中華民國證券櫃檯買賣中心。請您詳閱相關使用[規範與聲明](https://github.com/fortuna-intelligence/fugle-realtime-docs#Statement-中文使用規範與聲明)。

* [Price](#price)
* [Libraries](#libraries)
* [More Information](#more-Informatio)
* [Contact Fugle](#contact-Fugle)
* [Statement](#Statement)

## Price
|  | Demo | 富果帳戶[如何取得](https://www.fugle.tw/events/trade-landing-page/) |
|:--|:--|:--|
| Request / min | 60 | 60 |
| Websocket limit | 1 | 5 |
| Content | only 2884(玉山金) | 上市股票 <br/> 上櫃股票 <br/> 興櫃股票 <br/> 指數 <br/> ETF <br/> 權證 <br/> ETN |
| Price |  free |  free |

## Libraries
| language | github  |
|:---|:---|
| Python | [fugle-realtime-py](https://github.com/fortuna-intelligence/fugle-realtime-py)  |
| Python Demo | [fugle-realtime-demo](https://github.com/fortuna-intelligence/fugle-realtime-demo/tree/master) |
| JavaScript | [fugle-api-client](https://github.com/fortuna-intelligence/fugle-api-client)  |

## More Information
* [Index ID List](https://developer.fugle.tw/realtime/symbolIdList)
* [Realtime Status](https://developer.fugle.tw/realtime/status)


## Contact Fugle
* [Discord](https://discordapp.com/channels/601582504129855503/601583272555970560)
* [Form](https://www.fugle.tw/contact)
* [service@fugle.tw](mailto:service@fugle.tw)


## Statement 中文使用規範與聲明
1. 透過本服務取得之行情資料僅供參考，成交值及成交量不含零股及鉅額交易，使用者依本資料交易發生交易損失需自行負責。
2. 時報資訊與群馥科技對資料內容錯誤、更新延誤或傳輸中斷不負任何責任。您應對您所為之任何金融或投資決策自行負責。
3. 使用者應遵守[臺灣證券交易所股份有限公司交易資訊使用管理辦法](http://www.selaw.com.tw/LawArticle.aspx?LawID=G0100124)、[臺灣期貨交易所股份有限公司交易資訊使用管理辦法](http://www.selaw.com.tw/LawArticle.aspx?LawID=G0101422)、[財團法人中華民國證券櫃檯買賣中心有價證券交易資訊使用管理辦法](http://www.selaw.com.tw/LawArticle.aspx?LawID=G0100766)、各資訊來源提供者所定之資訊使用相關規範及智慧財產權相關法令，如有盜接、轉接交易資訊，或以其他方式出售、出租、轉讓、再授權交易資訊，或將交易資訊另行取樣並編製指數、其他衍生性商品或將之傳送予第三人，應負違約及侵權之相關民、刑事責任。


provided by [Fugle](https://www.fugle.tw/)