<!-- AI Context Standard v0.8.8 - Adopted: 2026-05-02 -->
# AI Assistant Initialization Guide — jichikai-2-pub (観音台第二自治会 公開情報)

**Purpose**: Initialize AI context for working with this repository

> **On every session start**: Read [`PROJECT_STATUS.md`](../PROJECT_STATUS.md) to get the current task and recent context before responding.

---

## 📚 Core Documents to Read

After reading this file, refer to:
- **PROJECT_STATUS.md** - Current work state and history
- **README.md** - Project overview and repository structure

---

## 🎯 Repository Context

**Project**: 観音台第二自治会 公開情報ページ  
**Website**: https://kannondai.github.io/jichikai-2-pub/  
**Repository**: https://github.com/kannondai/jichikai-2-pub  

**Mission**: 観音台第二自治会の回覧・お知らせ類を公開するサイト（公開リポジトリ）。

**Relationship to other repos**:
| リポジトリ | 内容 |
|---|---|
| [kannondai-community](https://github.com/kannondai/kannondai-community) | 観音台地域全体の情報（公開） |
| [jichikai-2-pub](https://github.com/kannondai/jichikai-2-pub)（このリポジトリ） | 第二自治会固有の公開情報（回覧等） |
| [jichikai-2-priv](https://github.com/kannondai/jichikai-2-priv) | 第二自治会の内部文書・作業資料（非公開） |

**Primary language**: Japanese (content), English (code/docs)

---

## 📂 Repository Structure

```
docs/
  index.html              # トップページ
  circulars/              # 回覧・お知らせ類
    fy2025/               # 2025年度（2025年4月〜2026年3月）
    fy2026/               # 2026年度（2026年4月〜2027年3月）
  styles/                 # CSS
```

---

## 🔑 Working Conventions

### 1. サイトは静的HTML

ビルドシステムやフレームワークなし。HTMLファイルを直接編集する。

### 2. 回覧・お知らせの管理方針

- 年度ごとにディレクトリを分ける（`fy2025/`, `fy2026/` 等）
- PDFファイルは `.gitignore` で管理外（印刷用ファイル）
- HTMLの回覧ページは公開用として作成・管理

### 3. 文字エンコーディング

常にUTF-8。日本語コンテンツが主。

### 4. CSSスタイル

`docs/styles/` 内のCSSを使用。kannondai-community と共通スタイルを採用。

---

## 💡 Quick Tips for AI Assistants

- **Primary task type**: 回覧HTMLページの作成、お知らせページの更新、インデックス更新
- **Site is static HTML**: No build system — edit HTML files directly
- **Character encoding**: Always UTF-8
- **Current work**: Check PROJECT_STATUS.md for latest tasks

---

## 🤖 AI Operating Conventions (from AI Context Standard v0.8.8)

### Failure Recovery

When the same operation fails 3+ times, stop and explain to the user. Propose alternatives. Do not silently retry 15+ times.

### PowerShell Multi-repo Git

Always use `git -C <path>` instead of `cd <path>; git ...`.  
The terminal tool may silently strip `cd` from chained commands.

```powershell
# ❌ Unreliable
cd C:\path\to\repo; git commit -m "..."

# ✅ Reliable
git -C C:\path\to\repo commit -m "..."
```
