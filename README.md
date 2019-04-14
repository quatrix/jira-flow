# Jira Flow 

## Example
![screen cast](http://edisdead.com/out.gif)

## Gitlab Token
go to https://gitlab.com/profile/personal_access_tokens and create a private token

```bash
git config --global --add gitlab.url https://gitlab.com
git config --global --add gitlab.token TOKEN_YOU_GOT
```

## Prerequisites
```bash
$ npm install -g jira-cmd git-lab-cli
$ jira
Jira URL: https://jira.atlassian.com/
Username: xxxxxx
Password: xxxxxx
Information stored!
```

## Installation
1. clone the jira flow repository ```git clone https://github.com/quatrix/jira-flow.git```
1. add wherever you cloned the repo to your ```$PATH```, for example: ```PATH=${PATH}:/Users/quatrix/repos/jira-flow```
1. configure your jira prefix, lets say it's VOVA: ```git config --global jira.prefix VOVA```


## Commands
You'll have the new git commands

* ```git issues``` - lists all non-done issues assigned to you
* ```git issue [issue]``` - show full description of current issue, or of [issue] if passed
* ```git workon 360 [soruce-branch]``` - start work on issue $PREFIX-360, this creates a feature branch and sets the ticket to ```IN_PROGRESS``` transition, if optinal argument source-branch supplied, it branches from source-branch instead of current branch
* ```git review <username>``` - create a merge request, assign it to ```<username>```  and set the story to code review status.
* ```git done [issue]``` - set current issue to done, or if [issue] is passed, set it to done
