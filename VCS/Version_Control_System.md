
# VERSION CONTROL SYSTEM

**Version Control System (VCS):** Record changes and modifications to files for recording purposes.

**Centralized Version Control System (CVCS):**
1. In CVCS, there is a central repository that stores the entire history and versions of the files.
2. Developers have a local copy of the files on their machines, but the central repository is the authoritative source.
3. To make changes, developers need to lock the files they are working on to prevent conflicts with others.
4. Communication with the central repository is necessary for most operations, including committing changes, viewing history, and branching.

**Distributed Version Control System (DVCS):**
1. In DVCS, each developer has a complete copy of the repository, including the entire history and versions of the files.
2. Developers can make changes and commit them to their local repository without requiring immediate interaction with a central server.
3. Branching and merging operations are easier and more efficient in DVCS since they can be done locally without relying on a central server.
4. Developers can work offline and commit changes to their local repository, and later synchronize with remote repositories when connected.



**Repository:** Where source code and files are stored.

**Goal of VCS:** Keep tracks of changes, provide access to the history, and revert and roll back the previous state.
Types of changes: Adding, Modifying/Updating and Deleting Files.

**Benefits of Version Control:** 
1.	Revision History: record of all changes in a project.
2.	Identity: changes are recorded with the identity.
3.	Collaboration
4.	Automation
5.	Efficiency

**Development Operations (DevOps):** 
•	Set of practices, philosophies and tools.
•	Increase ability.
•	Deliver applications
•	High quality
•	Velocity

**Monolithic Repository (Monorepo):** Software development strategy where all the code and project are stored in a single and centralized repository.

**Git:**  Version control system that track changes to the project.

**Benefits of Git:** Fast, Reliable, open-source and accessible.

**Hash ID:** Unique identifier for a git object such as Commit, Tree or Blob.

**HTTPS (Hypertext Transfer Protocol Secure):** It is a protocol to secure communication over the internet, used encrypting and decrypting data exchanged between web servers and web clients. (Such as web browser)

### GitHub
**What is GitHub?**
Web-based hosting service that allows developers to store, manage and collaborate on code repository.
Some of the key features are:
1.	**Version Control:** allow developers to track changes to their code, collaborate with others, and manage multiple versions of their project.
2.	**Code Review:** Code reviews, including pull request and code comments, which allow developers to review and discuss changes.
3.	**Issue Tracking:** Provide tools for tracking issues and bugs.
4.	**Project Management:** Provides project management tools, including project boards, milestones and task lists.
5.	**Collaboration:** Provides tools for collaborations, including team management, notifications and social media features.

### GitHub Hacks
**?:** Press question mark to show the short keys.
**Git.io :** Shorten the link of GitHub.
**Click the lines:** By clicking the lines of code then copy the URL and send it your boss for checking the specific function of code.
**Blame:** Allow you the check that who and when the changes were made.
**Commit Messages:** Important to give a proper messge while commiting.

**Branch:** a lightweight pointer to specific commit, represent an independent line of development that is separate from the main codebase, allowing developer to work on different features or bug fixes simultaneously without interfering with each other work. 

**Types of VCS:**
1.	Subversion
2.	Perforce
3.	AWS Code commit
4.	Mercurial
5.	Git

**Work Flow:**
Common work flow using the Git Version Control System:
1.	**Continuous Integration (CI):** Continuous building and testing code changes as they are made, in order to detect and resolve issues early in the development process.
2.	**Continuous Delivery (CD):** Automating the entire delivery process, from building and testing to deployment and release.
3.	**Continuous Deployment:** Strategy commonly involves automatically deploying to a test environment first to validate the deployment package and software changes.


### SOFTWARE DEVELOPMENT LIFECYCLE AND DEPLOYMENT BEST PRACTICES:

* **Development environments:** In which, software developers write, build, test, and debug code. The main purpose of this flow is to find any potential issues that may arise due to changes or new feature being added to the codebase. 
* **Stagging:** The environment should mimic your production environment, The reason for this is because you want to test the code in an environment that matches what you have in production.
* **New Features:** Developers submitting new features along with features flags for turning them on and off, should always do testing in stagging environment.
* **Testing:** The type of testing covered will be unit testing, integration testing and performance testing. All except performance testing can also be carried out in production.
* **Migration:** The process of moving an application or data from one environment or system to another. Stagging is the best place to test and verify data migrations.
* **Configuration Changes:** Having a stagging environment will allow you to spot any potential issues and bottlenecks.
* **Production:** Live and operation environment in which a software application or system is deployed and available for end-users to access and interact with.
* **Downtime:** Refers to a period of time when a software application, system or service is not available or cannot be used. Downtime for any service especially customer facing will most likely to be revenue impacting.
* **Vulnerabilities:** Cyber-security should also play a big role in what get released in production. Any changes to the latest version should also be checked and verified.
* **Reputation:** Downtime or issues in production is damaging for the company as it does not instill confidence to the end-users.
* **Interact:** Exchange information or send and receive information.

## Using Bash on Windows
----------------------------------------------

### COMMANDS

**‘cd ~’:** Change current directory to home directory. 
**‘ls’:** Display a list of files and directories in current directory.
**Some common options used with ‘ls’ commands:**

1.	**‘-l’:** Long format display show, show files or directories permission, owner size, modification, date and time, and name.
2.	**‘-a’:** Shows all files including hidden files.
3.	**‘-la’:** Shows the files and directories in long format and with hidden format.
4.	**‘-h’:** Human readable format.
5.	**‘-r’:** Reverse the order of the list.
6.	**‘-t’:**  Sort the list by modification of time.
7.	**‘pwd’:** Print Working Directory.

### COMMANDS

**Vim (Vi Improved):** A text editor, which has different modes for different tasks, such as navigating text, editing text, and entering text.

**‘vim’:** for using the vim in git bash.

**‘I’:** Set insert mode.

**echo "Hello World":** tells the operating system to use bash shell to execute the command.

**ESC:** to get out of the insert mode.

**‘:wq!’:** Save the file.

**-rw-r-:** Read, write file.

**‘chmod’:** Change the permission of file or directory in Unix-like operating system.

**‘chmod 755 “Your File Name”’:** Allow users to read, write and execute the file.

**‘./testshell.sh’:** Runs the shell script.

**-rwxr-:** Read, Write and executable file.

**.sh:** indicate the shell script file.  

**‘mkdir’:** Create new directory.

**‘mkdir -p dir2/dir3’:** In this case two directories will be created, and “dir3” being nested inside the “dir3”.

**‘touch “File Name”’:** Create new in current directory.

**‘cd ..’:** Change current working directory to the parent directory.

**‘clear’:** Clear the terminal screen.

**‘mv “Directory 2” “Directory 1”’:** Used to move the directories or files.  In this example “Directory 2” will be moved in “Directory 1”.

**‘cat “Your File Name’:** Display the content of one or files.

**‘wc -l’:**  count number of lines in the file.

**‘wc -c’:** Count number of character.

**‘wc -w’:** Count number of words.

**‘|’ (Pipe):** Connect output of one command to the input of another command.

### Redirection 
Control where the input and output command go. In Bash there are three types of Redirections:

1.	**Standard Input (stdin-0):** 
	a. **‘<’:** Redirect the standard input of a command from a file on another command.
	b. **‘cat < FileName’:** This will add the text but overwriting the file.
	c. **‘echo “Your Text” >> FileName’:** This will add the text without overwriting the file.
2.	**Standard Output (stdout-1)** 
	a. **‘>’:** Redirect the standard output of command to a file or another command but overwrite the file.
	b. **‘>>’:** Redirect the standard output of command to a file or another command but without overwrite the file.
3.	**Standard Error (stderr) ‘2>’:** Redirect the stderr to the file or another command.

### COMMANDS

**‘grep’:** (Global Regular Expression Print) Used for searching file and folder as well as content of files.

**‘grep Sam “FileName’:** Return the list of names that begins with “Sam” but with the case sensitivity.

**‘grep -i sam “FileName’:**  Return the list of name including the “sam” and ignore case sensitivity.

**‘grep -w “FileName”’:** Search whole word instead of partial matches.

**‘git rm –cached “FileName”’:** Remove from tracking but still exist in local machine.

**‘git branch’:** List all branches with in a repository and ‘*’ indicate the current branch.

**‘git branch “BranchName”’:** Create new branch.

**‘git branch -d “BranchName”’:** Delete a branch.

**‘git branch -m “OldBranchName” “NewBranchName”’:** Rename the branch.

**‘git checkout’:** Switch between branches in a git repository.

**‘git checkout -b “BranchName”’:** Create new branch and switch to it.

**‘git push “Remote” “Branch”’:** Upload your local commit to a remote repository.

**‘git remote add “Name” “URL”:** Add new remote repository.

**‘git remote’:** List all the remote repository associated with machine.

**‘git remote’:** List all the remote repository associated with URL in your local machine.

**‘git remote get-url “RemoteName”’:** Display the URL of the specific repository.

**‘git push -u “RemoteName” “BranchName”’:** Push the changes from local repository to remote repository.

**‘git push -d “RemoteName” “BranchName”’:** Delete a branch from a remote repository.

**‘git remote remove “RemoteName”’:** Remove the remote repository from your local repository.

**‘git merge “Source Branch”’:** Combine changes from one branch to another branch.

**‘git commit -a -m’: **Create a commit that include all modifies/tracked file in the working directory and stagging. (Direct Commit and skip the stagging area.)

**‘git pull’:** Used to fetch and download changes from the remote repository and integrate them into local branch.

**‘git diff’:** Make comparison on your local repository.

**‘git diff HEAD “FileName”’:** Compare the changes with most recent states with the last commit in the branch.

**‘git blame FileName’:** Display information about who last modified each line of file, along with commit hash, author, and timestamp of the modification.


