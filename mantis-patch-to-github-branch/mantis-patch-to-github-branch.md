# Create a Github branch for patches posted in Mantis

### Ideas 

i would start by doing it by hand, but taking notes on what we are doing, step by step... so that we can automate what can be automated.

- ~~We want to have a Github branch for each patch that is added to the Mantis bug tracker~~
  - ~~travis-ci that will be an automatic tester for us: that could be feedback enough for the author to refactor the patch~~
  - ~~perhaps make a script that auto-logs in to mantis and gives a result from the travis-ci test!!
- ~~We can test it with an ad hoc repository in the impagina github account~~
- it's unlikely that a fully automated script will do the right thing in most casees:
  - sometimes (depending on the programmer often) you have to try a few time before you get the patch to apply.
  - sometimes you have to apply several patches at once. sometimes one of the patches is the old one, the other the new one.
-  we should probably have a workflow where one person create the branch and everybody else can just check it out.
- a web form?
  - where you put the name of the new branch and the link to one or more patches in mantis...
  - and it uses the github API to create the new branch

### Workflow
* Patch is posted to MantisBT (the Scribus bugtracker)
* Tester decides to test patch
* Pull .patch from MantisBT
  - [ ] Automation: trigger a script to pull .patch from mantis
  - [ ] Manually download
* Push .patch to Github [Sandbox](https://github.com/impagina/scribus-sandbox)
  - [ ] Automation: script continues to trigger Github API to open a new branch on Sandbox as the patch name
  - [ ] Manually create a new branch on Sandbox and upload PR to new branch
* PR triggers Travis-CI test
* Travis-CI test returns results 
* Result reported back to MantisBT
  - [ ] Automation: automagically post results of test back to MantisBT
    *  script that auto-logs in to mantis and gives a result from the travis-ci test
  - [ ] Manually report results back to MantisBT



## TODO
- [x] Create sandbox repo (https://github.com/impagina/scribus-sandbox)
- [x] Register impagina/scribus-sandbox on travis-ci
- [ ] Build a workflow

### Backend
1. ```git clone git://github.com/scribusproject/scribus```
2. ```cd scribus/```
3. ```git add remote git://github.com/impagina/scribus-sandbox```
4. 
