


```
git config --global user.email "hello@gmail.com"
git config --global user.name "YOUR_NAME"
```


# 設計

## 大切なこと
- mainブランチは必ず動く状態にする
- developブランチで編集

- ブランチは線路のようなもの

## 流れ
- GitHubアカウントの作成
- GitHubでリポジトリの作成
- すでにローカルにファイルがある場合
- GitHub上にファイルがある場合
- .gitignore
- branch

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

```