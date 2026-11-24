# 先期技轉金系統：網站外框

用 GitHub Pages 提供一個 iframe 外框頁，內嵌先期技轉金系統的 Google Apps Script 網頁應用程式。後端原始碼與搬遷文件在 [nycu-rd-rp/yck-system](https://github.com/nycu-rd-rp/yck-system)。

## 檔案

| 檔案 | 用途 |
| --- | --- |
| `index.html` | 外框頁，iframe 指向 Apps Script 的 `/exec` |
| `icon.png` | 網站圖示 |

內容從舊外框 repo `emmaho0803/YCK_project` 複製而來，只把 iframe 換成接手帳號的新部署：

```
https://script.google.com/macros/s/AKfycby7H3NP831PEd0a_uxYkRu6P096bT3ydZfrDN4MAKo4SvXk9B9CM21OJjA02BayYTeH/exec
```

## 網域

正式網址 `ord.transferfee.nycu.edu.tw` 目前仍綁在舊 repo 的 GitHub Pages。這個 repo **刻意不放 `CNAME`**，測試期間只用 `https://nycu-rd-rp.github.io/yck-web/`。

切換正式網域時：

1. 從舊 repo 的 Settings → Pages 移除自訂網域。
2. 在本 repo 的 Settings → Pages 設定自訂網域 `ord.transferfee.nycu.edu.tw`，GitHub 會自動新增 `CNAME`。
3. 請 DNS 管理者把 CNAME 改指到 `nycu-rd-rp.github.io`。
4. 等憑證核發完成後，勾選 Enforce HTTPS。

在第 1 步到第 4 步完成之前，正式網址會短暫無法使用，應安排在離峰時段進行。
