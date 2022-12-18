# 2章の流れ
- GitHubアカウントの作成
- GitHubでリポジトリの作成
- すでにローカルにファイルがある場合
- GitHub上にファイルがある場合
- .gitignore
- branch

# 大切なこと
- mainブランチは必ず動く状態にする
- developブランチで編集
- ブランチは線路のようなもの

# GitHubセットアップ
GitHubのセットアップは以下のYouTubeがわかりやすいです．

[【わかりやすい！Git操作】初心者向けのGitの基本 〜 30分で入門！](https://youtu.be/6SLMB7BPG9E)

# ユーザーの追加
Gitを始めて使用する際は，自分のPCのターミナルで以下のコマンドを実行してください．
`hello@gmail.com`や`YOUR_NAME`の部分は自分のメールアドレス，自分の名前に変更してください．

```
git config --global user.email "hello@gmail.com"
git config --global user.name "YOUR_NAME"
```

# GitHubでリポジトリ作成
1. GitHubにログイン
1. Repositoryページを開く
1. `New Repository`という緑のボタンを押し，リポジトリを作成する


# リポジトリの初期化
自分のPC上でフォルダを作成し，以下のコマンドを実行する．

```
git init
```

# コミット
addの後ろのドットは，全てのファイルをコミット対象にしてください，という意味．

```
git add .
git commit -m "YOUR_COMMIT_MESSAGE"
# *** = YOUR_USERNAME
# ***** = YOUR_REPOSITORY_NAME
git remote add origin https://github.com/***/*****.git
git push origin main  # git push origin master
```



## GitHubについて
- issues
- Pull request
- GitHub actions

```bash title="bash"

git clone https://github.com/***/*****.git

git init
git add .
git commit -m "YOUR_COMMIT_MESSAGE"

git log 
git status


# *** = YOUR_USERNAME
# ***** = YOUR_REPOSITORY_NAME
git remote add origin https://github.com/***/*****.git
git push origin main  # git push origin master

git remote rm origin
git remote -v

#########BRANCH
git branch                          # show all branch
git checkout -b NEW_BRANCH_NAME
git checkout main                   # or git checkout master
git branch -d DELETE_BRANCH_NAME    # delete a branch


########PULL
git pull origin main            # pull where desired branch

######## データを戻す
git log     # 戻したい地点のコミットIDを検索
git reset --hart COMMIT_ID


######## commitを取り消す
git revert COMMIT_ID

### キャッシュファイルを削除
git rm -r --cached .        # ファイル全体のキャッシュを削除

```