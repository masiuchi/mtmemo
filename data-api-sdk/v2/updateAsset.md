# updateAsset

アイテムを更新します。

https://www.movabletype.jp/developers/data-api/v3-reference.html#assets-assets-put

## 例

### 例1

```javascript

api.authenticate(authenticateParams, function(response) {
  if (response.error) {
    // 認証エラー処理
    return;
  }
  
  api.updateAsset(siteId, assetId, assetData, function(response) {
    if (response.error) {
      // 更新エラー処理
      return;
    }

    // レスポンスデータを使った処理
  });
});

```
