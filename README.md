# 公開先URL
https://SHIO777.github.io/git-book

# 参考
- [ゼロから学ぶC++](https://github.com/rinatz/cpp-book)
- [MkDocsによるドキュメント作成](https://zenn.dev/mebiusbox/articles/81d977a72cee01)

# mkdocsのインストール
```
pip install mkdocs
```
# プロジェクトのインストール
git-bookというフォルダが作られ、そのフォルダ内に初期ファイルが作成される。

```
mkdocs new git-book
```

# テーマの変更
`mkdocs.yml`の中身を以下のように変更

```
site_name: Git Book
theme:
  name: material
```

# ビルド
git-bookプロジェクト内で以下を実行。
ビルドが成功されると、`site`フォルダが作成される。`site`フォルダにはhtmlファイルが作成される。

```
mkdocs build
```

# ローカルでビルドした内容を確認
以下のコマンドを実行する。

```
mkdocs serve
```
`localhost:8000`にアクセスすると、ページを確認することができる。

