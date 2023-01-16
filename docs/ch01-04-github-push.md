# GitHubにpush
実際にGitHubを使って、開発を行っていく。

## リポジトリの作成
- GitHubにアクセスし、リポジトリを新規作成する。
- GitHubでは、プロジェクトを「リポジトリ」という単位で扱う。
- １つのリポジトリに様々なファイルやフォルダが存在する。

## ディレクトリの変更とリポジトリのクローン
まず、ターミナルで現在のディレクトリを変更する必要がある。
ダウンロードしたいディレクトリに移動し、以下のコマンドでリポジトリをダウンロードする。

```bash title="bash"
cd ~/Documents
git clone https://github.com/***/*****.git
```

ここで、`***`にはユーザー名、`*****`にはリポジトリ名が入る。

例えば、以下のコマンドを実行した場合、

```bash title="bash"
cd ~/Documents
git clone https://github.com/hello/hello_project.git
```

ローカルPCには、`Documents/hello_project`というフォルダが作成される。


## ファイルのadd
今回は練習のため、適当にファイルを作成する。
ディレクトリを移動し、テキストファイルを作成する。

```bash title="bash"
cd ~/Documents/hello_project
touch README.txt
```

`README.txt`が作成されたら、テキストエディターで適当に文字を追加する。
編集し終えたら、再びターミナルに戻り、以下のコマンドを打つ。

```bash title="bash"
# hello_projectフォルダにいない場合は、下記のコマンドを打つ
cd ~/Documents/hello_project

git add .
```

`add`コマンドは、バージョン管理の対象ファイルを登録するコマンド。
addの次に続くピリオド`.`は、「フォルダ内のすべてのファイルを管理対象にする」という意味。

## ファイルのcommit
続いて、ファイルのバージョンを記録する。
記録するには、`commit`コマンドを用いる。

```bash title="bash"
git commit -m "コミットメッセージを入力する"
```

`-m`は`message`オプションと呼ばれる。編集した内容が一言でわかるように記述する。
例えば、READMEを追加した場合は、

```bash title="bash"
git commit -m "[add] READMEファイルを追加"
```
と入力すると良い。


## ファイルをpush

実際にGithubにファイルをアップロードするときは、`push`コマンドを実行する。
この段階でGithubにコードが追加される。


