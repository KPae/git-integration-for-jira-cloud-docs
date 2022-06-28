---

title: Git tags
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
The Git Integration for Jira app supports both lightweight and annotated tags. The tags are loaded separately from the rest of the Git Source Code.

## Introduction

Git tags identify specific release versions of your code in a particular branch and do not change when the branch moves on. A tag is an alias for a commit hash, much like symbolic names for a given revision. It is typically used to mark a particular point in the commit. It is like a branch with a read-only attribute. The git tags are accessible in the developer panel.

The git tags refers to merged, released work.

Having more than one tag with the same name across different branches can become difficult to maintain.


Tags cannot be moved since it is linked to a specific commit and are not pushed by default. 

Create a branch to start working from it if a tag is checked out.

The Git for Jira app supports two types of git tags:

*   **lightweight**  –  shows only the commit object

*   **annotated**  –  shows the message, author and the tag object followed by the commit


A lightweight tag can be use for marking a version or some specific commits that you will need to use later on  —  like a temporary object label. It does not contain extra information.

Annotated tags can contain a message, author and date different than the commit that they are pointing to  —  like describing a release without making a release commit.

## Getting started

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025983/gitcloud-devpanel-git-tags.png?version=1&modificationDate=1635944871358&cacheVersion=1&api=v2&width=340&height=141)

The Git Integration for Jira app will show the last 3 and first tags if no filter is set. If the filter is set, the Git Integration for Jira app will use it and will display the tags sorted in ascending order by date.

If there are several git tags listed, click the **more...** label link to expand the list in increments of five tags.

Click the adjacent icons to the right of the tags to open this tag in your git host service portal or in GitKraken git client app.

**Notification**
If loading of tags on a Jira issue takes longer than 60 seconds, the Git Integration app will notify the user about it and aborts the operation. This could happen if the Jira issue contains several hundreds of git tags or more.

**Cached Tags**
Git tags and branches are cached for the most recently viewed 1000 Jira issues (across all Jira projects). The cache is reset each time a new change in any repository is detected. The cache is built the first time an issue with a tag and/or branch is loaded by a user. Thus, subsequent loading of Jira issues with tag or branch information will utilize cached values.

The tag calculation timeout is **86400** seconds.

## Tag information

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025983/gitcloud-devpanel-git-tags-hover.png?version=1&modificationDate=1635945003233&cacheVersion=1&api=v2&width=340&height=139)

Move the mouse pointer over the tag to display the following tooltip information:

*   Repository Name

*   Commit author name and email address (if available)

*   Date / Time

*   Message (if any)


## Tag associations

Tags are only associated with the Jira issue by Jira keys that are specified in commits that belong to the tag. Specifying a Jira key in the name of a tag does not associate this tag with the mentioned ticket.

If some commits relate only to tags, these commits will not be displayed. For more information, see the [related known issue](/git-integration-for-jira-cloud/known-issues-gij-cloud).
