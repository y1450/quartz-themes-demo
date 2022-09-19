```
  hugo new site mynotes
  cd mynotes
  git init
  git submodule add https://github.com/jackyzha0/quartz.git themes/quartz
  mkdir assets
  cd assets 
  mkdir indices
  cd ../../
  cp -r themes/quartz/content ./
  ln -s themes/quartz/Makefile ./
```
```
  # to pull changes just go to theme directory and pull changes
  cd themes/quartz
  git pull origin hugo
```
## Vercel setup
just use other as an temp
set root directory as public
