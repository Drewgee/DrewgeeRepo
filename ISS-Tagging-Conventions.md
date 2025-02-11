# Tagging Convention
A configuration manager or administrator may tag for a baseline or milestone using git to emphasize a significant event. Below are the naming convention for all ISS GitHub repositories.
## Baseline Tag

**Naming convention**: ISS-rel-**\<version number>**

**Tag command:**
git tag -a ISS-rel-**\<release>** -m "\<long description> + \<JIRA merge task number>"

Example:
`git tag -a ISS-rel-2.5.0 -m "Baseline release for 2.5.0, ISS-897"`


## Milestone Tag
Tags as intermediary events to be tracked for the configuration managers purpose.

Branches, except for release and main follow the below naming convention.
**Tag Template**:

        **\<branch>**-**\<release>**-**\<environment>**-**\<iteration>**

Release branch. **Tag Template**:

        **\<branch>**-**\<environment>**-**\<iteration>**


| Tag Element   | Definition    |
| ------------- |-------------|
| **`<branch>`**| Branch the tag resides on, except for **main** or **master**|
| **`<release>`**| Application acronym and ssematic version|
| **`<environment>`**| Optional, taget environment the code build is to be deployed to|
| **`<iteration>`**| Optional, when a branch has multiple tags|

**Tag command:**
git tag -a **\<branch>**-**\<release>**-**\<environment>**-**\<iteration>** -m "\<long description> + \<JIRA merge task number>"

Example: `git tag -a develop-2.5.0-sqa-2 -m "share the release branch 2.5.0 wip code ISS-850"`
