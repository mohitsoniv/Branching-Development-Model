# Branching-Development-Model by Mohit Soni (mohitsoniv)
### 1. Start with the Production branch (main branch), and then create a HotFix  and Integration branch
1.1. Check the current branch
```
git branch
```
1.2. Create Hotfix branch 
```
git branch hotfix
```
1.3. Create Integratin branch 
```
git branch integration 
```
### 2. Subsequently, create Feature 1 and 2 branches that integrate to the Integration branch.
2.1. Switch to Integration branch 
```
git checkout integration
```
2.2. Create Feature1 & Feature2 branch 
```
git branch feature1
```
```
git branch feature2
``` 
### 3. Commit some changes in the Feature 2 branch and merge it into the Integration branch. Delete this branch once merging is complete.
3.1. Create a feature2.txt file in feature 2 branch & commet the changes

3.2. Switch to Integration branch  & merge the feature2 branch with Integration branch 
```
git checkout intergration
```
```
git merge feature2
```
3.3. Delete the Feature2 branch 
```
git branch -D feature2
```
### 4. Commit some changes in the Feature 1 branch and rebase it to the Integration branch.
4.1. Switch to Feature 1 branch & create feature1.txt file and commit the changes
```
git checkout feature1
```
4.2. Checkout to Integration file & rebase the Feature1 branch with Integration branch
```
git checkout integration
```
```
git rebase feature1
```
### 5. Merge the Integration branch into Hotfix and Production (main) branch to update these branches.
5.1. Switch to Hotfix branch & merge Integration branch
```
git checkout hotfix
```
```
git merge integration
```
5.2. Switch to Production (main) branch 
```
git checkout production (main)
```
```
git merge integration
```
### 6. Commit some changes in Feature 1 branch, and then merge it into Integration, Hotfix, and Production branch. Delete this branch once merging is complete.
6.1. Delete Feature 1 branch 
```
git branch -D feature1
```
### 7. Commit some changes in the Hotfix branch and merge it into the Production (main) as well as the Integration branch.
7.1. Switch to Hotfix branch & create hotfix.txt file & commit the changes 
```
git checkout hotfix
```
7.2. Switch to Integration branch & merge with hotfix branch 
```
git checkout integration
```
```
git merge hotfix
```
7.3. Switch to Production (main) branch & merge with hotfix branch 
```
git checkout production (main)
```
```
git merge hotfix
```
