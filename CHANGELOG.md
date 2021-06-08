## v0.2 - 2021-06-04

* 修正版號並與 realtime api 版號同步
* 更新 changelog.md 文件
* 原 v.0 api 服務將終止於 2021-06-26

## v0.2 - 2021-04-06

合併 `TWSE_SEM_TOTAL_X` 內容到 `TWSE_SEM_INDEX_X` 裡面, `TWSE_SEM_INDEX_X` 可以直接拿到指數的量

### Meta

* Mode `twse-sem` 移除以下 `symbolId`：
  - `TWSE_SEM_TOTAL_1`、`TWSE_SEM_TOTAL_2`、`TWSE_SEM_TOTAL_3`、`TWSE_SEM_TOTAL_4`、`TWSE_SEM_TOTAL_5`
* Mode `tpex-otc` 移除以下 `symbolId`：
  - `TPEX_OTC_TOTAL_1`、`TPEX_OTC_TOTAL_2`、`TPEX_OTC_TOTAL_3`、`TPEX_OTC_TOTAL_4`、`TPEX_OTC_TOTAL_5`

### Quote

* 新增 `change` 欄位反映盤中股價/指數變化
* 新增 `changePercent` 欄位反映盤中股價/指數漲幅
* 新增 `amplitude` 欄位反映盤中股價/指數振幅
* 修正 上市/上櫃/興櫃 股票最佳五檔報價順序
* 加權指數 `TWSE_SEM_INDEX_1` 新增 `last` 欄位反映最新單筆成交總額、成交數量、成交筆數
* 加權指數 `TWSE_SEM_INDEX_1` 新增 `total` 欄位反映當日總成交總額、成交數量、成交筆數
* 櫃買指數 `TWSE_OTC_INDEX_1` 新增 `last` 欄位反映最新單筆成交總額、成交數量、成交筆數
* 櫃買指數 `TWSE_OTC_INDEX_1` 新增 `total` 欄位反映當日總成交總額、成交數量、成交筆數
* Mode `twse-sem` 移除以下 `symbolId`：
  - `TWSE_SEM_TOTAL_1`、`TWSE_SEM_TOTAL_2`、`TWSE_SEM_TOTAL_3`、`TWSE_SEM_TOTAL_4`、`TWSE_SEM_TOTAL_5`
* Mode `tpex-otc` 移除以下 `symbolId`：
  - `TPEX_OTC_TOTAL_1`、`TPEX_OTC_TOTAL_2`、`TPEX_OTC_TOTAL_3`、`TPEX_OTC_TOTAL_4`、`TPEX_OTC_TOTAL_5`

### Chart

* 加權指數 `TWSE_SEM_INDEX_1` 新增 `unit` 欄位反映每分鐘成交金額
* 櫃買指數 `TWSE_OTC_INDEX_1` 新增 `unit` 欄位反映每分鐘成交金額
* Mode `twse-sem` 移除以下 `symbolId`：
  - `TWSE_SEM_TOTAL_1`、`TWSE_SEM_TOTAL_2`、`TWSE_SEM_TOTAL_3`、`TWSE_SEM_TOTAL_4`、`TWSE_SEM_TOTAL_5`
* Mode `tpex-otc` 移除以下 `symbolId`：
  - `TPEX_OTC_TOTAL_1`、`TPEX_OTC_TOTAL_2`、`TPEX_OTC_TOTAL_3`、`TPEX_OTC_TOTAL_4`、`TPEX_OTC_TOTAL_5`

### Dealts

* 新增上市/上櫃股票盤後定價交易明細
* Mode `twse-sem` 移除以下 `symbolId`：
  - `TWSE_SEM_TOTAL_1`、`TWSE_SEM_TOTAL_2`、`TWSE_SEM_TOTAL_3`、`TWSE_SEM_TOTAL_4`、`TWSE_SEM_TOTAL_5`
* Mode `tpex-otc` 移除以下 `symbolId`：
  - `TPEX_OTC_TOTAL_1`、`TPEX_OTC_TOTAL_2`、`TPEX_OTC_TOTAL_3`、`TPEX_OTC_TOTAL_4`、`TPEX_OTC_TOTAL_5`

## v.0 - 2020-03-16
* initial release.
