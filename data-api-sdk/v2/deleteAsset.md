# deleteAsset

アイテムを削除します。

https://www.movabletype.jp/developers/data-api/v3-reference.html#assets-assets-delete

## 例

### 例1

```javascript

api.authenticate(authenticateParams, function(response) {
  if (response.error) {
    // 認証エラー処理
    return;
  }

  api.deleteAsset(siteId, assetId, function(response) {
    if (response.error) {
      // 更新エラー処理
      return;
    }

    // レスポンスデータを使った処理
  });
});

```
