# timesheet hook

post-commit hook for logging time to jira

## post-commit use

1. clone this repository
1. update Jira server variable if not a newmedia employee
1. cp the post-commit file into the .git/hooks directory of the repo you want to track time for
1. make sure the file is executable

### Change Jira server URL

Edit post-commit and change JIRA_SERVER to your Jira server URL.  You can also set the environment variable JIRA_SERVER to your jira instance.

### Make post-commit executable

    chmod +x /path/to/repo/.git/hooks/post-commit


**Note**: This post-commit hook will only take effect when your branch matches a JIRA ticket issue pattern. eg. ADMIN-2 or TESTING-23

After you commit code you will be asked to enter your Jira credentials if you havent done so already.  You will then need to enter time in the format
"1d 1h 1m".

