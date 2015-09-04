# timesheet hook

post-commit hook for logging time to jira

## Use

1. clone this repository
1. [update Jira server variable if not a newmedia employee](#jira_server)
1. cp the post-commit file into the .git/hooks directory of your repository
1. [make sure the file is executable](#make_executable)

### Change Jira server URL <a name="jira_server"></a>

Edit post-commit and change JIRA_SERVER to your Jira server URL.  You can also set the environment variable JIRA_SERVER to your jira instance.

### Make post-commit executable<a name="make_executable"></a>

    chmod +x /path/to/repo/.git/hooks/post-commit


After you commit code you will be asked to enter your Jira credentials if you havent done so already.  You will then need to enter time in the format
"1d 1h 1m".