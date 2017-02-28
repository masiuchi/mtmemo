# listAssets

アイテムの一覧を取得します

```
GET https://your-host/your-mt-api.cgi/v2/sites/:site_id/assets
```

## パラメータ

### 必須パラメータ

|パラメータ名|タイプ|説明|
|---|---|---|
|site_id|integer|サイトID|

### クエリパラメータ

|パラメータ名|タイプ|説明|
|---|---|---|
|search|string|検索文字列。初期値:なし|
|searchFields|string|検索するフィールド。初期値:label|
|class|string|クラスフィルタ。file, audio, image, video が設定可能。|
|limit|unsigned integer|１回のリクエストで所得するアイテムの数。初期値:10|
|offset|integer|オフセット。初期値:0|
|sortBy|string|ソートに使うフィールド。初期値:created_on|
|sortOrder|string|ascend:昇順、descend:降順。初期値:descend|
|fields|string|出力するフィールドをカンマ区切りで設定する。未指定の場合は全フィールドを出力する。初期値:なし|

## 戻り値

|パラメータ名|タイプ|説明|
|---|---|---|
|totalResults|unsigned integer|リクエストに対する全アイテム数|
|items|ARRAY|アイテムの配列（limitで制限されるので、totalResultsとは異なる場合がある）|

## 例

### 例1

```javascript
api.listAssets(siteId, function(response) {
  if (response.error) {
    // エラー処理
    return;
  }
  
  // レスポンスデータを使った処理
});
```

### 例2

```javascript
var params = {
  search: "QUERY",
  searchFields: "label",
  fields: "label,url,createdDate"
};
api.listAssets(siteId, params, function(response) {
  if (response.error) {
    // エラー処理
    return;
  }
  
  // レスポンスデータを使った処理
});
```
