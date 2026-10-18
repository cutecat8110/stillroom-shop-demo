# 商店編輯器

![Nuxt](https://img.shields.io/badge/Nuxt-v4-00DC82)
![Vue.js](https://img.shields.io/badge/Vue.js-v3-42b883)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6)
![Element Plus](https://img.shields.io/badge/Element_Plus-409EFF)

> 店面編排、商品選購與組合／贈品核對，支援文字及圖片對話。

![店面編排與即時預覽](docs/images/editor.png)

## 📋 專案概述

編輯器與店面共用區塊元件，支援圖文調整、排序與多尺寸預覽。選購流程涵蓋商品規格、購物車及組合／贈品核對，搭配文字與圖片對話。

**[體驗店面編輯](https://cutecat8110.github.io/stillroom-shop-demo/#/editor)** · **[逛逛店面](https://cutecat8110.github.io/stillroom-shop-demo/)**

## 功能入口

| 入口 | 代表操作 |
| --- | --- |
| [店面編輯](https://cutecat8110.github.io/stillroom-shop-demo/#/editor) | 區塊排序、圖文調整、復原重做與版型保存 |
| [商品選購](https://cutecat8110.github.io/stillroom-shop-demo/#/collection) | 分類搜尋、價格排序、規格與庫存 |
| [購物車](https://cutecat8110.github.io/stillroom-shop-demo/#/carts) | 數量、運費及單品／組合／贈品核對 |
| 右下角「聊聊」 | 文字與圖片、送出前預覽、放大查看 |

## 🔨 核心技術

| 技術 | 用途 |
| --- | --- |
| Nuxt 4 / Vue 3 | 店面與編輯器共用元件 |
| TypeScript | 區塊設定與購物車資料模型 |
| IndexedDB | 版型、圖片與購物車儲存 |

## 🛠️ 擴展套件

| 技術 | 用途 |
| --- | --- |
| Element Plus | 編輯控制、彈窗與操作回饋 |
| Element Plus Icons | 編排與操作圖示 |

<details>
<summary>店面與選物確認</summary>

![目前選物店面](docs/images/storefront.png)
![單品、組合內含與贈品](docs/images/shopping.png)

</details>

<details>
<summary>實作重點</summary>

編輯器與店面共用版面元件，支援桌面、平板與手機預覽。WebP 圖片及非首屏延後載入；IndexedDB 交易與版本檢查避免跨分頁覆蓋。

</details>

<details>
<summary>使用說明</summary>

**試用：** 點鑰匙帶入帳密 → 登入編輯器 → 編排並儲存 → 選購商品 → 確認選物 → 圖片對話。

商品、帳號與對話為展示資料，保存在目前瀏覽器。確認選物不建立實際訂單，沒有付款、出貨或真人客服；登入並非後端驗證。

重新整理保留已存內容，選物需重新確認。「重設資料」恢復初始狀態。圖片僅在瀏覽器處理，支援 PNG、JPEG、WebP，單張上限 2 MB。

</details>
