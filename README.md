# 労働衛生コンサルタント 口述試験対策システム

保健衛生区分の口述試験対策用チャットボットです。

## 🎮 モード説明

| モード | 説明 | データソース |
|--------|------|--------------|
| **本編** | 基本→詳細→応用の3段階構成 | `data/questions.md` |
| **追加問題編** | 補足的な知識を補強 | `data/followup.md` |
| **カスタム問題** | 自分で追加した問題 | localStorage |
| **復習フォルダ** | 5点以下の問題を復習 | localStorage |

## 🚀 デプロイ方法

### 1. GitHubリポジトリを作成
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

### 2. GitHub Pagesを有効化
1. リポジトリの **Settings** → **Pages**
2. **Source** で `main` ブランチを選択
3. フォルダは `/ (root)` を選択
4. **Save** をクリック

### 3. アクセス
`https://YOUR_USERNAME.github.io/YOUR_REPO/`

---

## 📁 ファイル構成

```
├── index.html          # アプリ本体
├── data/
│   ├── questions.md    # 本編の問題（予想問題集）
│   └── followup.md     # 追加問題編（追加質問回答集）
└── README.md
```

---

## 📝 問題の更新方法

### 本編の問題を追加・編集
`data/questions.md` を編集してpush

```markdown
## テーマ名

**Q1（基本問題）：**
問題文

**【模範解答】**
解答文

**【この問題で試験官が見ているポイント】**
- ポイント1

**【想定される追加質問】**
- 追加質問1
```

### 追加問題を追加・編集
`data/followup.md` を編集してpush

```markdown
### Q：質問文

**A：** 回答文
```

---

## 💾 データ保存

| データ | 保存先 |
|--------|--------|
| 本編・追加問題 | GitHubのマークダウンファイル |
| カスタム問題 | ブラウザのlocalStorage |
| 復習フォルダ | ブラウザのlocalStorage |

※ カスタム問題と復習フォルダは端末・ブラウザごとに保存されます
