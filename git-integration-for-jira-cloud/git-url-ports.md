---

title: Git URL Ports
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
If your Git servers are running through a firewall, configure the firewall to allow access using the URL schemes for git repositories. For authentication issues, make sure to check first the correct port for its connection.

Below are the default ports for common git URL protocols:

|     |     |
| --- | --- |
| **Protocol** | **Default Port** |
| ssh:// | port 22 |
| git:// | port 9418 |
| http:// | port 80 |
| https:// | port 443 |

Test git connection and repository URL by doing the following:

1.  Install git client (_or run_ `sudo apt-get install git`)

2.  Place your ssh key into `~/.ssh`

3.  Clone the repository (or run `git clone <your_repository_url>`)


The Git Integration for Jira app will run successfully if the above connection test ran without errors.


For detailed information on whitelisting your Git server, see [Allow list (whitelist) BigBrassBand Cloud](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud/).
