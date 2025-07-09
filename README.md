# IFALAB

本平台用於管理實驗室的研究專案程式碼、資料處理流程，以及協作規範。

---

## 📁 組織結構說明

| 類型 | 說明 |
|------|------|
| `semantic-search` | 使用向量資料庫與語意檢索技術之專案 |
| `rag-pipeline` | RAG + PDF 文件分析流程 |
| `sd-stock-ranking` | 股票兩兩支配比較與 GPU 加速研究 |
| `lab-handbook` | 本說明文件與共用規則 |
| `utils-shared` | 各專案共用的前處理、可視化模組等工具 |

---

## 👥 成員加入流程

1. 接受 GitHub 組織邀請
2. 將共用 Google Drive `ifaf_shared_data` 加入「我的雲端硬碟」
3. Clone 專案並遵循 Git 操作流程進行開發

---

## ⚙️ Git 協作流程

```bash
# 第一次 clone 專案
git clone https://github.com/ncu-ifaf-lab/project_name.git
cd project_name

# 建立新分支開發功能
git checkout -b feature/your_name_功能名稱

# 修改後提交
git add .
git commit -m "新增模組 by your_name"
git push origin feature/your_name_功能名稱

# 發 Pull Request 合併到 main 分支
```

請勿直接推送到 `main` 分支，請使用分支 + PR 工作流。

---

## 🧪 Google Drive 整合說明

在 Colab 或本機可掛載 Google Drive：

```python
from google.colab import drive
drive.mount('/content/drive')

# 路徑建議統一為
data_root = "/content/drive/MyDrive/ifaf_shared_data"
```

> 大型資料（PDF, FAISS, JSONL）請放 Google Drive，避免上傳 GitHub。

---

## 📬 聯絡

- 指導老師：邱信瑜老師（hsin-yu.chiu [@] ncu.edu.tw）
- 實驗室成員請使用 GitHub Issues 提出問題
