# listAssets

アイテムの一覧を取得します

https://www.movabletype.jp/developers/data-api/v3-reference.html#assets-assets-get

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
