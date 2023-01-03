## Motivation 
I have two reasons to use [Quartz](https://github.com/jackyzha0/quartz) as submodule,

1. Keep my changes separate from Quartz. Better Maintability.
2. Keep history of my notes private. I don't want notes github repo to be public.
  I use vercel to deploy because Github doesn't free deployments of private repos on github pages.

This setup makes following changes to  [Quartz](https://github.com/jackyzha0/quartz)

- The Github Action is no longer used as we don't deploy on github pages.
- we intialized the Quartz repo as a submodule, rather than cloning the original Quartz repo.


### Instructions

#### Hugo Setup
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
#### Vercel setup

In the dashboard create a new project and import from the github repository
![image](https://user-images.githubusercontent.com/107429941/210136617-cb22eba5-292c-4528-a0d2-3a245d8ef788.png)
![image](https://user-images.githubusercontent.com/107429941/210136635-c70d2383-6346-4ccd-9a6a-d2e1ff848c7e.png)

![image](https://user-images.githubusercontent.com/107429941/210136703-42ee8069-cbf4-4f1f-b86e-900357d77b69.png)

