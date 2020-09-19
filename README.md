# Git & Github-The-complete-Handbook
This repo covers all the core concepts and commands for Git and Github with relevant use cases.

## WHAT USE-CASE GIT FOLLOW? WHY WE NEED GIT?
- (problem) Developer write some code in any language and store that program file in a folder(workspace). Sometimes dev did some changes which were logically correct but the output wasn't as expected OR your dev did some chnages coz of which code got corrupted. So we want older version of code back. Maybe code can be of economical website or app connecting millions of people. So if code got corrupted customers won't be able to connect and that's a huge business loss. ( So its not good practice to change code of live real world apps pr website)

-(solutions) So we want older version of code back. One solution can be to always make 2 copies of code before writing new code to restore changes. Not efficient coz 1000 copies banana and store krna is not a good idea. Waste time and resources. So other way is if we can create internally a timeline of file and using that timeline we can retrieve at what point in time and at what day, what changes were made in the file, who made those changes. So in other words we make multiple versions of program file, so that at any point if our code crashes we can rollback to previous version of file. So we can see different views of our data by managing the timeline just like Facebook manages our timeline. Similarly we want  to create a timeline of our data.

- (optimal solution) So to maintain versions of any file so that in future, we can rollback to any previous version, for that we need to create a system (VCS). Git is one such tool using which we can maintain VCS of any file. Latest version of file is called HEAD.

- Although VCS is used for any file but it is mainly used for Source code file or program file. So Git is a tool, which works on version control system, and used for source code management.

- GIT works on DVCS (Decentralized VCS) but other tools work on CVCS (centralized VCS)

- To install git version 2:

```
  yum list git    // Redhat DVD has git V1 as default
  
  rpm -q epel-release   // download software from internet but version is git V1
  
  rpm -ivh endpoint-repo-1-7-1X.rpm
  
  yum install git   // install git v2 from internet

```

## Delta vs Snapshot vs Backup:

Git is mainly used for source code management. So if V1 (100MB) and V2 (1KB) and V3 (1MB).
In git , while making versions, for the first time complete data is copied (Full backup) but after that only the part which is changed or added (Delta) is copied in the next version(snapshot). This saves time and space consumption.

Pure Backup: Every time complete data is copied.

Snapshot: Only delta part is copied.

So when Git make versions then technically in the background it takes snapshots.

- The place where git stores its versions is called GIT Repository. So we have to create a repository for GIT(workspace).

```
mkdir /myprojects

cd /myprojects

git status // see nothing

git init // to initialize current folder as git repository

git status // to see current repository is git repository
```

**NOTE: Git repository is not per OS, not per user, not per Application. It is per folder or per directory. 
So if its a git repository, then git is tracking every folder and file of that repository. Git is tracking evey activity**

```
# git status  // to confirm what new files were added or modified

```
