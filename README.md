# timesheet hook

post-commit hook for logging time to jira

## post-commit use

1. clone this repository
1. update Jira server variable if not a newmedia employee
1. cp the post-commit file into the .git/hooks directory of your repository
1. make sure the file is executable

### Change Jira server URL

Edit post-commit and change JIRA_SERVER to your Jira server URL.  You can also set the environment variable JIRA_SERVER to your jira instance.

### Make post-commit executable

    chmod +x /path/to/repo/.git/hooks/post-commit


After you commit code you will be asked to enter your Jira credentials if you havent done so already.  You will then need to enter time in the format
"1d 1h 1m".

## commit-msg use

Note: use of this hook will negate the post-commit hook

1. clone this repository
1. cp the commit-msg file into the .git/hooks directory of your repository
1. make sure the file is executable

On commit this script will check for #time in the commit message and prompt user for time if it doesn't exist.
