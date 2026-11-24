# 平安住・客戶表單

客人填寫用的公開表單，網址：https://yuengshih-work.github.io/forms/

| 檔案 | 用途 |
|---|---|
| `index.html` | 表單入口（官網、LINE、名片 QR code 都連這裡） |
| `leak.html` | 漏水評估申請（照片＋地點＋狀況，欄位同官網「預約報價」頁） |
| `reno.html` | 裝潢需求思考清單（可存成 PDF，也可直接傳給平安住） |
| `assets/logo.png` | 平安住 LOGO |

## 資料去哪裡

送出後直接進「平安住專案管理系統」的後端（yuengshih@gmail.com 部署的 Apps Script）：

- 試算表「平安住・專案管理系統」→ `forms` 分頁
- 照片 → 雲端資料夾「平安住・專案管理系統檔案／客戶表單／編號_姓名」
- 每張新表單會寄 Email 通知（預設寄給 yuengshih@gmail.com；要改收件人，在 Apps Script「指令碼屬性」加 `NOTIFY_EMAIL`，多個用逗號分隔）
- 專案管理總覽 → 「客戶表單」可以查看、改狀態、開案；開案時同一支電話的表單會一起連結到案場頁

編號規則：裝潢需求 `R年月日-序號`、漏水評估 `L年月日-序號`。

## 後端網址

三個 html 檔最下方的 `const API = '…/exec'`，要和 `projects/assets/common.js` 的 `API` 相同。
