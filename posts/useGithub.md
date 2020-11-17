---
title: "勉強会_gitを使いこなそう！ "
date: "2020-08-28"
---

**基本の使い方：**<br>
リポジトリを clone: git clone <Repo の Url><br>
リポジトリ名を指定したい時：git clone <Repo の Url> <DestinationDirectory>

リモートリポジトリの最新状況を取る：git fetch<br>
最新状況を取り込む：git pull

新規ブランチ：git branch <branch_name><br>
ブランチを切り替える：git checkout <branch_name>

どのようなブランチがあるのかを確認したい時：<br>
１、ローカルのブランチを確認する：git branch<br>
２、リモートのブランチを確認する：git branch -r<br>
３、全てのブランチを確認する：git branch -a

今の変更はコミットしたい：git commit -a

**進撃の使い方：**<br>
Rebase でコミットをまとめる：git rebase -i HEAD~~

他ブラントの修正を取り込みたい：git cherry-pick <commit_ID><br>
他のリポジトリの修正を取り込みたい：<br>
１、他リポジトリを add：git remote add <name> <Repo の Url><br>
２、git cherry-pick <commit_ID><br>
３、先 add したリポジトリを削除：git remote rm <name>

修正の一次退避：git stash<br>
複数の stash を確認したい場合：git stash list<br>
stash の中身を確認したい場合：git stash show<br>
stash の内容を反映する：git stash pop<br>
stash を指定して反映する：git stash pop stash@{0}

**その他：**<br>
ローカルブランチを削除したい時：git branch -d <branch_name><br>
まだマージしていない ローカルブランチを削除したい時：git branch -D <branch_name><br>
マージ済みのローカルブランチを全て削除：git branch --merged master | grep -vE '^\*|master$|develop$' | xargs -I % git branch -d %
