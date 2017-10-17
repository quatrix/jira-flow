# Jira Flow 

Jira integration with git, working on tickets creates a feature branch and you can assign code review even if you can't convince your boss to add a ```IN_REVIEW``` transition by using comments.

## Example
![screen cast](http://edisdead.com/out.gif)

## Prerequisites
```bash
$ npm install -g git+https://github.com/quatrix/jira-cmd.git
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
* ```git review <username> <merge request link>``` - adds a comment to the currently worked on ticket, that asks ```username``` to review your code
* ```git done [issue]``` - set current issue to done, or if [issue] is passed, set it to done
* ```git users``` - lists all available users
