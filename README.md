
### Git Usage

* Branch master deploy to production

* Branch dev deploy to development

* Release/1.1.0 [num version] : archives des versions stables

* Feature/[feature_name] : nouvelles fonctionnalités

* Fix/[fix_name] : corrections


### Examples : 

##### Deploy dev to master and create release version  

* Git commit & push origin dev 

* Git checkout -b release/1.2.x dev

* git commit and push release 

* git checkout master 

* git merge dev master 


#####  Create and deploy feature 

* git checkout -b /features/[feature_name]

* [Coding]

* git commit feature/[feature_name] dev

* git checkout dev

* git merge --no-ff feature/[feature_name] dev 

* git commit & push dev 

* Release Version 

* git branch -d fix/[fix_name]

##### Fix bug  on dev 

* git checkout -b /fix/[fix_name] dev

* [Coding]

* git commit fix/[fix_name]

* git checkout dev

* git merge --no-ff fix/[fix_name] dev 

* git commit & push dev 

* Release Version 

* git branch -d fix/[fix_name]


##### Hotfix bug on prod 


* git checkout -b hotfix[hotfix_name] master 

* [coding]

* git checkout master 

* git merge hotfix/[hotfix_name] master 

* git commit and pull master 

* git checkout dev

* git merge master 

* git commit and push dev 

* Release Version 

* git branch -d hotfix[hotfix_name]


That's all 















