# YULON Intern Operating System (YIOS)

復古終端機風格的互動式實習生介紹網站。

## 本機預覽

直接用瀏覽器開啟 `index.html`，或用簡易伺服器：

```bash
npx serve .
```

## 修改成員資料

編輯 `index.html` 裡的 `MEMBERS` 物件：

```javascript
member1: {
  name: "Oliver",
  hobby: "play lego",
  photo: "images/oliver.png"   // 正方形照片路徑，沒有就留 ""
}
```

有填的欄位才會顯示；之後要加 `department`、`skills` 等直接加在物件裡即可。

## 插入照片

1. 建議使用 **正方形圖片（1:1 比例）**，例如 400×400 或 600×600 px
2. 放到 `images/` 資料夾（例如 `images/oliver.png`）
3. 在對應成員的 `photo` 欄位填上路徑
4. 選擇 profile 時，照片會出現在**文字右側**（手機版改為文字下方置中）

非正方形的圖會自動以 `object-fit: cover` 裁切成正方形顯示。

## 部署到 GitHub Pages

```bash
git init
git add .
git commit -m "Add YIOS intern intro site"
git branch -M main
git remote add origin https://github.com/你的帳號/你的-repo名稱.git
git push -u origin main
```

在 GitHub repo：**Settings → Pages → Build and deployment → Source** 選 **Deploy from a branch**，Branch 選 `main` / `/ (root)`，儲存。

幾分鐘後網址會是：`https://你的帳號.github.io/你的-repo名稱/`

## 檔案結構

```
├── index.html      # 主網站（HTML + CSS + JS）
├── images/         # 成員照片放這裡
└── README.md
```
