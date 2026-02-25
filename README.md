# 観音台第二自治会 公開情報ページ

**公開URL**: https://kannondai.github.io/jichikai-2-pub/

---

## このリポジトリの位置づけ

観音台地域の情報は、以下の3リポジトリで管理しています。

| リポジトリ | 公開/非公開 | 内容 |
|---|---|---|
| [kannondai-community](https://github.com/kannondai/kannondai-community) | 公開 | 観音台地域全体の情報（第一・第二自治会共通） |
| [jichikai-2-pub](https://github.com/kannondai/jichikai-2-pub)（このリポジトリ） | 公開 | 観音台**第二**自治会固有の公開情報（回覧・お知らせ等） |
| [jichikai-2-priv](https://github.com/kannondai/jichikai-2-priv) | 非公開 | 観音台第二自治会の内部文書・作業資料 |

### 第一自治会のページを追加するには

第一自治会の担当者が公開情報ページを設ける場合、同様に `jichikai-1-pub` リポジトリを作成し、
上の表に行を追加する形で管理を分担できます。

---

## ディレクトリ構成

```
docs/                   # GitHub Pages 公開ルート
  index.html            # トップページ
  community/            # 回覧・お知らせ類
    202602/             # 2026年2月分
    ...
  styles/               # CSS
```

---

## 開発・運用

- GitHub Pages: `docs/` ブランチを公開
- CSS は [kannondai-community](https://github.com/kannondai/kannondai-community) と共通スタイルを使用
- ファイル管理方針: `.gitignore` にて `*.docx`（印刷用ファイル）は管理外
