# gitbootcamp20180713

## 1. git add
- 追加されたファイルなどをバージョン管理の対象として追加するコマンド。  
ワーキング・ツリーの中のファイルをインデックス（ステージ）に追加する。
- オプションでファイル名やディレクトリを指定すると指定したファイルやディレクトリ配下のファイルが対象になる。


## 2.git commit
ファイルの変更した部分を保存しておくコマンド


## 3
- git commit
- ○


## 5. git branch fix/42 を実行
- 正常に処理される場合、実行後は何も表示されない。
- git branch と打つと、以下が表示される

```
fix/42
* master
```


## 6．git checkout -b fix/42;git commit
- fix/42というブランチを作成し、コミットを分岐させる。


## 7. git checkout -b fix/42
- fix/42という名前のブランチを作成し、そこに移動するコマンド。
- オプション -bは新規にブランチを作成します。-bをつけない場合は指定したブランチに移動するだけ。


## 8. git reset --hard master
- ローカルのツリーとインデックスの変更内容はすべて消える。実行時は要注意です。
- git statusで必ず状態を確認しましょう。


## 11. 凡例
- 青はcommitの実行、緑はaddの実行


## 12．git checkout fix/42
- fix/42という名前のブランチに切り替える。


## 13. git rebase master
- 今いるブランチをmasterのブランチに付け替えるコマンド。
- 現在のブランチの指す先をリベース先のブランチと同じコミットに移動させ、そして先ほどの変更を順に適用していく。
- rebaseすると元のコミットとはコミットIDが変わってしまう。


## 18. git pull
- リモートリポジトリの変更点をローカルリポジトリに取り込む。


## 19. git pull --rebase
- git pullは fetch + mergeですが、--rebaseオプションをつけるとfetch + rebaseとなる。
- マージコミットを作りたくないときに使う。ただしrebaseすると元のコミットとはコミットIDが変わってしまう。


## 23. git clone
- 既にあるリモートリポジトリをローカルリポジトリに持ってくる。


## other. test
- git push までを練習中です。すみません。


## other ローカルブランチ(fix/42)をローカルのmasterとマージ
- $ git checkout fix/42  
fix/42ブランチへの切り替え
- $ git merge master  
fix/42は何も記述がないファイルのため、masterの情報に更新

## git rebase -i
- pullしたり、mergeしてから自分がcommitした履歴が表示される
- pick [commit id] [commit comment] で記述されている。
- pick を適宜変更し、内容を保存。エディタを閉じる。
- 再度エディタが開くので、コミットコメントを改めて記述する。
- 記述が終わったら保存。エディタを閉じると、以下のメッセージが表示される。
 - 実行結果(例)
```
[detached HEAD 2a30600] git rebase -i を練習し、その方法を残す
 Date: Fri Jul 13 15:55:01 2018 +0900
 1 file changed, 7 insertions(+), 4 deletions(-)
Successfully rebased and updated refs/heads/master.
```
