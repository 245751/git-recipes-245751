# git-recipes-245751
git勉強会の講義で使うリポジトリ

## Task 2 —内部構造の探偵

### A1
#### 出力内容
6

リポジトリを作る時packとinfoというディレクトリが作られるため

### A2
#### 出力内容
```
ref: refs/heads/kitchen/245751
ae32ecf5cd4d8b7b7d5cae1c0a6411065a98b193
```

### A3
#### 出力内容
```
3657b41 Initial commit
```
```
Note: switching to '3657b41'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 3657b41 Initial commit
3657b41a38d802bcb607f8be99dae54458763bcf
```
```
Switched to a new branch 'rescue'
Switched to branch 'kitchen/245751'
Deleted branch rescue (was 3657b41).
```

## Task 3 —レシピ3つ
#### 出力内容
```
[kitchen/245751 ebcd98d] feat: add curry recipe
 1 file changed, 1 insertion(+)
 create mode 100644 recipes.txt
```

## Task 4 —散らかった料理人
#### 出力内容
結合前
```
5d51201 (HEAD -> kitchen/245751) del github
cb343b7 oops
4f4f4c8 fix
41e35b6 a
ebcd98d feat: add curry recipe
```

結合後
```
b37bde3 (HEAD -> kitchen/245751) feat: improve curry recipe
ebcd98d feat: add curry recipe
```

## Task 5 —キッチンでコンフリクト
#### 出力内容
```
*   cd4afba (HEAD -> kitchen/245751, origin/kitchen/245751) Merge pull request #1 from 245751/spicy-version
|\  
| *   44ea940 (origin/spicy-version) Merge branch 'kitchen/245751' into spicy-version
| |\  
| |/  
|/|   
* | eb2f18f add MILD
| * 45fee23 (spicy-version) add EXTRA SPICY
|/  
* b37bde3 feat: improve curry recipe
* ebcd98d feat: add curry recipe
```

## Task 6 —レシピを1つだけもらう
#### 出力内容
desert git log
```
0389607 (HEAD -> desert) add cake.txt
cd4afba (origin/kitchen/245751, kitchen/245751) Merge pull request #1 from 245751/spicy-version
44ea940 (origin/spicy-version) Merge branch 'kitchen/245751' into spicy-version
```

kitchen/245751 git log
```
e7f168b (HEAD -> kitchen/245751) add cake.txt
cd4afba (origin/kitchen/245751) Merge pull request #1 from 245751/spicy-version
44ea940 (origin/spicy-version) Merge branch 'kitchen/245751' into spicy-version
```

#### SHAが違う理由
コピーしてきたものとは別に新しくコピーしてきたブランチでコミットを作っているため