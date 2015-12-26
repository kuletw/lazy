Kule Lazy 3
=============

版本：3.0.151226

使用說明請看：http://www.kule.tw/doc.html

## 前言
這是一個純CSS的Framework，目前不包含 Javascript，但未來陸續會新增 Javascript 的處理、Icon的繪製、更多模組。

#### 載入檔案

將依照您的路徑連結您使用的檔案，例如：

```html
<link href="你的資料夾路徑/kule-lazy-full.min.css" />
```

在使用 Kule Lazy 之前，建議載入 [urBrowser](http://urbrowser.kule.tw)，它能夠幫助你針對不同平台或瀏覽器進行除錯，如果你有使用 kule-grid-ie.min.css 的話，那麼它會是**必須載入**的 Javascript 檔案，例如：


```html
<link href="你的資料夾路徑/kule-grid.min.css" />
<script src="你的資料夾路徑/kule-urbrowser.min.js" />
```

##### 建議載入的順序

載入順序可參照上方表格的順序

###### 使用全部效果：

```html
<link href="你的資料夾路徑/kule-lazy-full.min.css" />
<link href="你的資料夾路徑/kule-effects.min.css" />
<link href="你的資料夾路徑/kule-animates.min.css" />
<link href="你的資料夾路徑/kule-jquery-ui.min.css" />
<script src="你的資料夾路徑/kule-urbrowser.min.js" />
```

###### 單獨使用 Grid System：

```html
<link href="你的資料夾路徑/kule-grid.min.css" />
<script src="你的資料夾路徑/kule-urbrowser.min.js" />
```

###### 只要使用基本樣式：

```html
<link href="你的資料夾路徑/kule-base.min.css" />
<script src="你的資料夾路徑/kule-urbrowser.min.js" />
```

###### 使用基本樣式與組件：

```html
<link href="你的資料夾路徑/kule-lazy.min.css" />
<script src="你的資料夾路徑/kule-urbrowser.min.js" />
```

###### 使用基本樣式與組件搭配附加模組：

```html
<link href="你的資料夾路徑/kule-lazy.min.css" />
<link href="你的資料夾路徑/kule-addons.min.css" />
<script src="你的資料夾路徑/kule-urbrowser.min.js" />
```

---

## 全域規則

在你使用 Lazy 之前，請先初步了解基本規則，這樣會幫助你更簡單使用 Lazy。

#### 配色與狀態

以下為Lazy的配色與狀態顏色，使用配色時請以 `.color-` 為開頭並搭配以下配色名稱，例如：`.color-primary`

```html
<a class="btn color-primary">按鈕</a>
<a class="btn color-suceess">按鈕</a>
<a class="btn color-warning">按鈕</a>
<a class="btn color-error">按鈕</a>
```

還有一種情況也能使用配色，當給予父層標籤時，所有內容都會套上顏色，例如：

```html
<div class="btn-grp color-primary">
  <a class="btn">按鈕</a>
  <a class="btn">按鈕</a>
  <a class="btn">按鈕</a>
  <a class="btn">按鈕</a>
</div>
```

---

#### 尺寸大小

除了原本的預設大小之外，大部分的元素或組件都有其他四種尺寸變化，包含

```html
<a class="btn size-xs">按鈕</a>
<a class="btn size-sm">按鈕</a>
<a class="btn size-lg">按鈕</a>
<a class="btn size-xl">按鈕</a>
```

當然這也與配色一樣可以直接給予父層讓所有元素有著相同尺寸

```html
<div class="btn-grp size-sm">
  <a class="btn">按鈕</a>
  <a class="btn">按鈕</a>
  <a class="btn">按鈕</a>
  <a class="btn">按鈕</a>
</div>
```

---

#### Disabled

只要使用到 `disabled` 屬性或是 `.disabled` 時，該區塊或是元件就會無法點選並且加上透明度。

```html
<input type="text" class="ctrl-input" disabled />
<div class="btn-grp disabled">
  <a class="btn">按鈕</a>
  <a class="btn">按鈕</a>
  <a class="btn">按鈕</a>
  <a class="btn">按鈕</a>
</div>
```

---

## 瀏覽器與裝置

#### 各平台上的瀏覽器支援

基本上市面主流系統與瀏覽器都有支援，但Opera的版本煩亂就沒有刻意去處理，至於 IE 瀏覽器主要支援 IE 9以上版本，當然如果本身CSS 3屬性完全不支援的情況下就無法支援。至於微軟最新的 Edge 瀏覽器採用的是 Webkit 核心，所以支援度應該與 Chrome 差不了太多。根據[維基百科](https://zh.wikipedia.org/zh-tw/Microsoft_Edge)指出：『Microsoft Edge 使用了名為 EdgeHTML 的瀏覽器引擎，該引擎是 Trident 的一個分支。』但從 userAgent 來看，的確是顯示 Webkit。(Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/42.0.2311.135 Safari/537.36 Edge/12.10240)</span>

我自己專案的瀏覽器支援度通常是最新版號-1。

|   |Chrome|Firefox|Edge|IE|Safari|Opera|
|---|---|---|---|---|---|---|
|Windows|支援|支援|支援|局部支援<br />請見下方表格|不存在|支援|
|Mac OS|支援|支援|不存在|不存在|支援|支援|
|iOS|支援|支援|不存在|不存在|支援|不支援|
|Android|支援|支援|不存在|不存在|不存在|不支援|

---

#### IE 瀏覽器支援度

使用有關動畫效果如 Effects, Animates時，請先注意 IE 支援度是否符合你的專案。

|   |6, 7|8|9|10|11|
|---|---|---|---|---|---|
|Lazy|不支援|局部支援|局部支援|支援|支援|
|Grid System|不支援|局部支援<br />支援 Grid<br />但不含 Responsive|支援|支援|支援|
|Animates|不支援|不支援|不支援|支援|支援|
|jQuery UI Theme|不支援|支援|支援|支援|支援|

---

### Hacks
Hack 基本上是針對 IE 瀏覽器，尤其是 IE 8，因為部分模組有使用 @media query，因此另外寫 Hack 給 IE 8，所以請記得載入 [urBrowser](http://urBrowser.kule.tw)，Hack 才能生效。

---

## 使用授權
Kule Lazy 使用 [MIT 授權](https://github.com/keicheng/kule.lazy/blob/master/LICENSE)。
完全免費，真是佛心來著。其實當初只是用不慣其他 CSS Frameworks，所以把以前寫過的東西拿出來整理，然後自己刻了一套。

---

## 問題與回報
目前處於 beta 版本中，但大致上都已完成，主要剩下 IE Hack 以及 Mobile 上的測試。當然如果你有發現任何疑問或是 bug，歡迎隨時到 [Facebook](https://www.facebook.com/kule.tw) 上告訴我，謝謝你。
