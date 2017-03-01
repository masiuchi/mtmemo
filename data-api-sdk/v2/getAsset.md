# getAsset

アイテムのデータを取得します。

https://www.movabletype.jp/developers/data-api/v3-reference.html#assets-assets-get-4

## 例

### 例1

```javascript
api.getAsset(siteId, assetId, function(response) {
  if (response.error) {
    // エラー処理
    return;
  }

  // レスポンスデータを使った処理
});
```

### 例2

```javascript
var param = {
  fields: "label,url"
};
api.getAsset(siteId, assetId, function(response) {
  if (response.error) {
    // エラー処理
    return;
  }

  // レスポンスデータを使った処理
});
```
