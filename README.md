# 拾間選物｜店面編輯與購物體驗

`Nuxt 4` · `Vue 3` · `TypeScript` · `Element Plus` · `IndexedDB`

從區塊編排到商品選購，體驗編輯器與店面同步更新的操作流程。

**[逛逛店面](https://cutecat8110.github.io/stillroom-shop-demo/)** · **[進入工作室](https://cutecat8110.github.io/stillroom-shop-demo/#/editor)**

![店面編輯](docs/images/editor.png)

| 入口 | 代表操作 |
| --- | --- |
| [店面編輯](https://cutecat8110.github.io/stillroom-shop-demo/#/editor) | 區塊排序、文字與圖片調整、復原重做、版型保存 |
| [商品選購](https://cutecat8110.github.io/stillroom-shop-demo/#/collection) | 分類搜尋、價格排序、規格與庫存 |
| [購物車](https://cutecat8110.github.io/stillroom-shop-demo/#/carts) | 數量調整、商品移除、運費試算 |
| 客服對話 | 快速提問、文字訊息、對話保存 |

**試用順序：** 逛店面 → 登入工作室 → 編排並儲存 → 返回店面選購。
登入頁的鑰匙按鈕可帶入帳密。

![選物店面](docs/images/storefront.png)
![購物與對話](docs/images/shopping.png)

## 實作重點

- 編輯器與店面共用版面元件，支援桌面、平板與手機預覽。
- 型別化資料操作、交易寫入與版本檢查，避免跨分頁覆蓋。
- WebP 圖片、非首屏延後載入，編輯與對話元件分開載入。

## 體驗說明

商品、帳號與對話均為展示資料。內容只保存在目前瀏覽器，沒有付款、出貨或真人客服；登入為展示操作，並非後端驗證。

重新整理會保留已存內容；工作室選單的「重設資料」可恢復初始狀態。圖片上傳僅在瀏覽器內處理。
