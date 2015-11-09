# Create a Github branch for patches posted in Mantis

i would start by doing it by hand, but taking notes on what we are doing, step by step... so that we can automate what can be automated.

- We want to have a Github branch for each patch that is added to the Mantis bug tracker
  - travis-ci that will be an automatic tester for us: that could be feedback enough for the author to refactor the patch
  - perhaps make a script that auto-logs in to mantis and gives a result from the travis-ci test
- We can test it with an ad hoc repository in the impagina github account
- it's unlikely that a fully automated script will do the right thing in most casees:
  - sometimes (depending on the programmer often) you have to try a few time before you get the patch to apply.
  - sometimes you have to apply several patches at once. sometimes one of the patches is the old one, the other the new one.
-  we should probably have a workflow where one person create the branch and everybody else can just check it out.
- a web form?
  - where you put the name of the new branch and the link to one or more patches in mantis...
  - and it uses the github API to create the new branch
