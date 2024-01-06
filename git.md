- Reset last commit

  ```
    git reset HEAD~
  ```

- Change Remote orign
  ```
    git remote set-url origin https://git-repo/new-repository.git
  ```

- Lấy git log online

  ```
    git log --online
    git log --online --no-merges
  ```

- Checkout/ Switch to branch with $logId - $commitId

  ```
    git checkout -b branch_test $logId
  ```

- Git stash

  - Git stash cùng mới một message kèm theo

  ```
    git stash save "Toi dang Code cai gi the nay"
  ```

  - Git stash loại bỏ những files không được theo dõi

  ```
    git stash save -u
    or
    git stash save --include-untracked
  ```

  - Lấy danh sách

  ```
    git stash list
  ```

  - Apply(lấy stash gần nhất - cuối cùng)

  ```
    git stash apply
  ```

  - Pop (giống apply nhưng sẽ xóa stash)

  ```
    git stash pop
    or
    git stash pop stash@{1}
  ```

  - clear

  ```
    git stash clear
  ```

  - drop

  ```
    git stash drop
    git stash drop stash@{1}
  ```

- Git cherry pick: Lấy code từ commitId trừ các merge commit

```
  git cherry-pick commitId
  git cherry-pick commitId1 commitId2 ...
  git cherry-pick --abort //loại bỏ hành động trước đó
  git cherry-pick commitId^..commitIdn // cherry-pick range
  git cherry-pick -m 1 --no-commit commitId^..commitIdn // cho phép các commit merge, không commit
```
