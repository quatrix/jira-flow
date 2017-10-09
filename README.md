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
* ```git issue 360``` - show full description of an issue $PREFIX-360, if no ticket number provided tries to figure out from current branch
* ```git workon 360``` - start work on issue $PREFIX-360, this creates a feature branch and sets the ticket to ```IN_PROGRESS``` transition
* ```git review username``` - adds a comment to the currently worked on ticket, that asks ```username``` to review your code
* ```git done``` - sets the currently worked on ticket to done.
* ```git users``` - lists all available users
