# getAsset

アイテムのデータを取得します。

```
GET https://your-host/your-mt-api.cgi/v2/sites/:site_id/assets/:asset_id
```

認証不要

## メソッドパラメータ

|パラメータ名|タイプ|説明|
|---|---|---|
|site_id|integer|サイトID|
|asset_id|unsigned integer|アイテムID|

## クエリパラメータ

|パラメータ|タイプ|説明|
|---|---|---|
|fields|string|出力するフィールドをカンマ区切りで設定する。未指定の場合は全フィールドを出力する。初期値:なし|

## 戻り値

|パラメータ|タイプ|説明|
|---|---|---|

## 例
