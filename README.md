# hh_git_1

repoA: git init

repoA: git add -A

repoA: git commit -m "First commit"

repoA: git branch branch1

git clone ./repoA ./repoB

repoB: git checkout branch1

repoB: git add fileC

repoB: git commit -m "Second commit"

repoB: git push origin branch1

repoA: git checkout branch1 

repoA: git commit -a -m "Third commit"

repoB: git commit -a -m "Third commit"

repoB: git fetch origin 

repoB: git merge origin/branch1

repoB: git commit -a -m "Merge"

repoA: git remote add repoB ../repoB

repoA: git fetch repoB 

repoA: git merge repoB/branch1 

