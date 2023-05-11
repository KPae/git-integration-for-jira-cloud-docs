---

title: Git user Identity
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

A git user can identify himself on his local computer using the following commands:

```bash
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```


Or, for specific repository:

```bash
$ git config user.name "John Doe"
$ git config user.email johndoe@example.com
```


Then every commit is supported by the configured user information.

Hosting services _(like GitHub and BitBucket, for example)_ try to match these data in commits with a particular account:

*   **If the email is unknown, it just displays the name from the commit.**
    If there is no Jira user associated with the email, the Git Integration for Jira app will use the author's name from the commit and displays this name without any associated links.

    ![](/wp-content/uploads/gij-git-user-non-matching-email.png)

*   **If an email is configured in the local repository, the account is detected and will be displayed.**
    The Git Integration for Jira app will use the email from a commit and will search for a Jira user using this email. If the Jira user is found, the associated link to his Jira profile is displayed with the accompanying Jira avatar beside the name.

    ![](/wp-content/uploads/git-user-matching-email.png)

&nbsp;
* * *

[**Prev:** Viewing commit code diffs](/git-integration-for-jira-cloud/viewing-commit-code-diffs-gij-cloud)

[**Next:** Jira user information card](/git-integration-for-jira-cloud/jira-user-information-card-gij-cloud)

