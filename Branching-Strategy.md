# Branching Strategy

The VSA team has implemented the progressive stability model branching strategy. In the strategy, branches host the source code at different stages of development, allows for concurrent development and isolated branches for designated Agile issue. 

### **Branch Structure**

The standard branch hierarchy for the code repository is shown below. DevOps code is promoted up as it progresses through its development lifecycle.
- ---
:closed_lock_with_key: :infinity: **main** (aka Prod)- current version of code deployed to production, formerly “master”
- ---
:lock: :infinity: **release/** - represents the candidate release code that is currently being promoted thru to production
    
  **Naming convention**: release/\<release number>
   
      example: release/2.5.1
- ---
:lock_with_ink_pen: :stopwatch: ***development branch*** - associated to sprint teams release efforts as per the program increment

   **Naming convention**: dev/\<release number>
   
      example: dev/2.5.1
---
:unlock: :hourglass_flowing_sand: ***feature branch*** each branch represent a single effort to resolve an Agile issue, and is an unrestrained workspace for the developers
  
   **Naming convention**: ISS-\<Jira Issue Number\>-\<optional text\>
   
      example: ISS-29881-SHarris   

---
### **Working with Branches**
Feature branches are the unrestricted workspaces for development. There are no constraint to making source code changes. Users have the option to work directly in Bitbucket.com to edit files or work on a local copy of the git branch with a TRM approved code editor or IDE. Using the feature branch naming convention is helpful when creating a “smart commit” to reference the Jira issue.

# Code Change Management
## :heavy_exclamation_mark: Smart Commits & Pull Requests (PR's) :heavy_exclamation_mark: 
ISS utilizes the smart commit webhook from Bitbucket to Jira allowing for traceability of all branches, pull requests and commits. All Jira issues are associated to a specific release/sprints and the changes made to the code in Bitbucket. This traceability enables the planning activities and coordination to be managed with Jira records, and is the basis to the Version Description Document (VDD), bill of materials (BOM) and release traceability matrix (RTM).

## :heavy_exclamation_mark: Smart Commit Convention :heavy_exclamation_mark:
When creating the commit message or pull request title in git/Bitbucket, you must construct the message following the syntax below. 

**Naming convention**: **\<Jira Key>** **\<Jira summary\>** or **\<Summary or the effort\>**

    Example:
    ISS-123456 Enhanced the automation deployment for PPD

**`Note:`** Separate the Jira Key comnponent from the summary with a <space>. The space is used to parse out the Jira Key for metrics and reporting

:information_source: Best practice incorporate the Jira Key in the name of the feature branch and copy and paste in the commit message
