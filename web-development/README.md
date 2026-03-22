# 🌐 網頁開發：三種語言的分工

網頁是由三種語言合作完成的，就像蓋房子需要不同工種：

```
HTML  →  骨架（決定有什麼）
CSS   →  外觀（決定長什麼樣子）
JS    →  行為（決定怎麼動起來）
```

| 語言 | 比喻 | 負責的事 |
|------|------|----------|
| HTML | 人在哪裡 | 標題、圖片、按鈕、清單... |
| CSS | 穿什麼衣服 | 顏色、字體、間距、圓角... |
| JavaScript | 做什麼動作 | 點擊、彈窗、動畫、驗證... |
> 🌐 [點我直接在瀏覽器操作示範](https://simonlifestyles-glitch.github.io/learning-notes/web-development/web-demo.html)

> 🌐 [流程圖](https://simonlifestyles-glitch.github.io/learning-notes/web-development/Flowchart-builder.html)

---

## 📝 HTML 範例

> HTML 用「標籤」把內容包起來，告訴瀏覽器這頁有什麼東西。

```html
<html>

  <head>
    <!-- head 是給瀏覽器看的設定，不會顯示在頁面上 -->
    <title>我的第一個網頁</title>
  </head>

  <body>
    <!-- body 裡面的東西才會顯示在頁面上 -->

    <h1>嗨，我是小明 👋</h1>

    <p>我正在學習寫網頁。</p>
    <p>我喜歡打籃球和聽音樂。</p>

    <h2>我的興趣</h2>
    <ul>
      <li>籃球</li>
      <li>聽音樂</li>
      <li>學程式</li>
    </ul>

    <a href="https://www.google.com">點我去 Google</a>

  </body>

</html>
```

### 常用標籤速查

| 標籤 | 用途 |
|------|------|
| `<h1>` `<h2>` | 大標題、中標題 |
| `<p>` | 一段文字 |
| `<ul>` + `<li>` | 清單 |
| `<img>` | 圖片 |
| `<a href="...">` | 超連結 |
| `<button>` | 按鈕 |

---

## 🎨 CSS 範例

> CSS 選擇某個元素，然後設定它的外觀。格式是：`選誰 { 改什麼: 改成怎樣; }`

```css
/* 整個頁面的背景顏色 */
body {
  background-color: #FFF8F0;  /* 米色背景 */
}

/* 大標題的樣式 */
h1 {
  color: #993C1D;     /* 深橘紅色文字 */
  font-size: 36px;    /* 字體大小 */
}

/* 按鈕的樣式 */
button {
  background-color: #D85A30;  /* 橘色背景 */
  color: white;               /* 白色文字 */
  border-radius: 20px;        /* 圓角 */
  padding: 10px 24px;         /* 內部留白：上下 10px，左右 24px */
}
```

### 常用屬性速查

| 屬性 | 功能 |
|------|------|
| `color` | 文字顏色 |
| `font-size` | 字體大小 |
| `background-color` | 背景顏色 |
| `border-radius` | 圓角程度 |
| `padding` | 內部留白 |
| `margin` | 外部間距 |

> 💡 把 CSS 寫在 HTML 的 `<head>` 裡，用 `<style>` 標籤包起來就可以套用。

---

## ⚡ JavaScript 範例

> JavaScript 監聽使用者的動作，然後改變頁面。這就是「讓網頁動起來」的本質。

```html
<body>

  <button onclick="handleClick()">按我</button>
  <p id="訊息區"></p>

  <script>
    // 「//」開頭是註解，給人看的，電腦不執行

    // 定義一個函式 — 就是一組等待執行的指令
    function handleClick() {

      // 找到頁面上 id 叫「訊息區」的元素
      let 訊息 = document.getElementById("訊息區");

      // 把那個元素的文字內容改掉
      訊息.textContent = "你按到我了！🎉";
    }

    // 按鈕上的 onclick="handleClick()"
    // 意思是：「按下去的時候，執行這個函式」
  </script>

</body>
```

### JavaScript 能做的事

| 觸發條件 | 可以做的事 |
|----------|------------|
| 按鈕點擊 | 顯示訊息、送出資料 |
| 表單送出 | 驗證內容是否正確 |
| 計時器 | 每隔幾秒自動更新 |
| 鍵盤輸入 | 即時搜尋、字數計算 |
| 滑鼠移動 | 觸發動畫效果 |

---

## 🗺️ 我的學習路線

- [x] 認識程式設計的五大領域
- [x] 了解網頁的三種語言：HTML / CSS / JavaScript
- [x] 寫出第一個 HTML 頁面
- [ ] 學會用 CSS 美化頁面
- [ ] 學會用 JavaScript 加入互動
- [ ] 做出第一個完整的個人網頁

---

*筆記持續更新中...*
