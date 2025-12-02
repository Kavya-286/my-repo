# Dynamic Data Table Manager

A dynamic and customizable data table application built using **Next.js**, **Redux Toolkit**, and **Material UI (MUI)**.  
This project allows users to manage table data with features like sorting, searching, pagination, dynamic column visibility, and CSV import/export.

---

## 🚀 Features

### ✅ Core Features
- Display table with default fields: **Name, Email, Age, Role**
- **Sorting** on each column (ASC/DESC toggle)
- **Global search** across all fields
- **Client-side pagination** (10 rows per page)

### 🧩 Dynamic Columns
- “Manage Columns” modal to:
  - Add new fields dynamically (e.g., Department, Location)
  - Show / hide existing columns via checkboxes
- Column visibility is **persisted** using localStorage / Redux Persist

### 📥 CSV Import & 📤 Export
- Import CSV using **PapaParse**
- Validate format and show error feedback
- Export current table view as `.csv`
- Only visible columns are included in the export

---
Task 1: Pushing multi-folder project into private repository( Note: student take
 screenshots for upload).
 
 1. Create a Private Repository on GitHub
  Gotohttps://github.com
  ClickNew repository
  Giveit aname
  CheckPrivate
  ClickCreate repository
 
 2. Initialize Git in Your Local Project (if not already done)
 Open a terminal in the root of your multi-folder project:
 cd /path/to/your/project
 git init
 
 3. Add the Remote Repository (in bash)
 You’ll see a URL on GitHub after creating the repo. It will look as below , run this command
 in git bash:
 git remote add origin https://github.com/yourusername/your-private-repo.git
 
 4. Add and Commit Your Files(in bash)
 git add .
 git commit-m "Initial commit"
 
 5. Push to the Private Repository
 If the repo is new and empty, push like this from git bash:
 git push-u origin master
 If you're using the main branch (GitHub default):
 git push-u origin main
 You may be prompted to log in (via username/password or token).
 
 
 Task 2: Students must explore all listed git commands on the multi-folder
 project in local and remote repository.
 
 1. Git Commands:
 ●
 git version : The command git version is used to check the version of git.
 git--version
  git config: Configures Git settings. Commonly used to set up user information
 git config--global user.name "Your Name"
 git config--global user.email "youremail@example.com"
  git config--list: Displays all the Git configurations for the current user.
 
 
 2. Repository Management
  git init: Initializes a new Git repository in the current directory
 git init
  gitclone: Creates a copy of an existing Git repository from a remote source (e.g., GitHub) to your local machine
 git clone https://github.com/username/repository.git
  gitremote–v : To see the remote repository that is connected to your local repository
 git remote–v
  gitremote add : To add a new remote repository to your local repository
 git remote add origin https://github.com/username/repository.git
  Pushing Changes to Remote: To push your local commits to a remote repository:
 git push <remote_name> <branch_name>
 git push origin main
  Pulling Updates from Remote: To pull the latest changes from the remote repository
 and merge them into your local branch
 git pull <remote_name> <branch_name>
 git pull origin main
  gitremote remove: To remove a remote repository from your local configuration:
 git remote remove <remote_name>
 git remote remove origin
  RenamingaRemote: torename an existing remote:
git remote rename <old_name> <new_name>
 git remote rename origin upstream
  Fetching Updates from Remote: To fetch updates from the remote repository but
 not merge them into your local branch
 git fetch <remote_name>
  ChangingRemote URL: Tochange the URL of a remote (e.g., after changing the
 remote repository address):
 git remote set-url <remote_name> <new_url>
 git remote set-url origin https://github.com/username/new-repository.git
  Viewing the Remote Repository’s Information: to see detailed information about a
 remote repository
 git remote show <remote_name>
 git remote show origin
 
 3. Staging and Committing
  git status: Shows the status of changes in your working directory and staging area. It
 tells you which files are untracked, modified, or ready to be committed.
 git status
  gitadd: Adds changes in the working directory to the staging area.
 git add filename.txt # Adds a specific file
 git add .
 # Adds all changes in the directory
  gitcommit: Commits the staged changes to the repository with a descriptive message.
 The-m option allows you to include a commit message.
 git commit-m "Commit message describing changes"

 4. Branching and Merging
  git branch: Lists all branches or creates a new branch
 git branch
 # Lists all branches or
 ->git branch-a
 # Lists all branches
 ->git branch branch-name # Creates a new branch
 ->git branch-d <branch_name> # Deletes a branch
Use-D to force-delete if it hasn't been merged.
  Listing All Remote Branches : To you want to list all branches on the remote
 repository
 ->git branch–r
  gitcheckout: Switches to a different branch
 git checkout branch-name # Switches to an existing branch
 git checkout-b new-branch # Creates and switches to a new branch
  Pruning Deleted Remotes : If a branch was deleted on the remote but still shows up
 locally.
 git remote prune origin
 
 =>When someone deletes a branch on the remote, your local Git doesn’t automatically
 remove the corresponding remote-tracking branch (like origin/old-feature).
 git remote prune origin removes these outdated references.

  Fetching a Specific Remote Branch: To fetch a specific branch from a remote.
 git fetch <remote_name> <branch_name>
 git fetch origin feature-branch
  Setting the Upstream Branch for Pushing : When pushing for the first time and
 want to set the remote branch you are pushing to:
 git push--set-upstream <remote_name> <branch_name>
 git push--set-upstream origin feature-branch
 git merge: Merges the specified branch into the current branch. This command
 integrates the changes from the feature branch into the main branch.
 git checkout main
 
 # Switch to the main branch
 ->git merge branch-name # Merge branch-name into main
  Rebasing a Local Branch onto a Remote Branch: If you want to rebase your local
 branch onto a remote branch (this can be useful to keep your history linear)
 ->git fetch <remote_name>
 ->git rebase <remote_name>/<branch_name>

 Example:
 git fetch origin
 git rebase origin/main
 
 5.
 Undoing Changes

 git reset : Removes the specified file from the staging area but leaves the working
 directory unchanged. git reset--hard can also reset the working directory and staging
 area to the last commit.
 git reset <file>:
  git revert: Creates a new commit that undoes the changes from a specified commit,
 leaving the history intact.
 
 =>git revert <commit>:
 Viewing History
  gitlog: Shows a history of commits in the repository, including commit hashes,
 messages, and timestamps. Use git log--oneline for a more concise view.
 ->git log
  git diff: Displays differences between various commits, the working directory, and the
 staging area. git diff without arguments shows changes not yet staged.
 git diff:
  git show: Shows the details of a specific commit, including the changes made and the
 commit message.
 git show <commit>
 
 To undo the changes made to file before staging it.
  gitrestore filename
 To correct committed with the wrong message
  gitcommit--amend-m "Corrected commit message"
 
 9. Recovering deleted branches
  gitreflog
  gitcheckout-b feature-ui <commit_hash>
 
 10. To download the latest changes from the remote without merging
  gitfetch origin

 11. To remove accidentally committed sensitive file from Git history.
  gitfilter-branch--force--index-filter \
  "gitrm--cached--ignore-unmatch secrets.txt" \
 --prune-empty--tag-name-filter cat----all
 
 12. To merge changes from another branch
 First switch to branch where changes are to applied and then merge another-branch
 gitcheckout previous-branch
  gitmerge another-branch

 13. To resolve a merge conflict manually
 You tried to merge two branches and Git reported a conflict in x.js. Then for conflict
 resolution do:
 1. Openx.js and resolve/remove the conflict markers (<<<<<<<,
 =======, >>>>>>>)
 2. After resolving:
  gitaddapp.js
  gitcommit #IfGit didn’t auto-create a merge commit
 14. The .gitignore
 The .gitignore file is used to tell Git which files or directories to ignore in your project. It's a
 useful way to avoid committing unnecessary files like log files, build outputs, and IDE
 configurations.
 a. Create a .gitignore File
 In the root directory of your Git project, create a file called .gitignore
 touch .gitignore
 b. AddRules to .gitignore
 Inside the .gitignore file, you add patterns for the files and directories you want Git to ignore.
 Each pattern should be written on a new line.
 Here are some common examples:
  Ignore all .log files: *.log
  Ignore a specific file: secret_file.txt
  Ignore all files in a temp/ directory:
 temp/
  Ignore all files except important_file.txt inside a folder:
 folder/*
 !folder/important_file.txt
  Ignore files with a specific extension: *.bak
 15. To see who changed a particular line in a file
  gitblame script.py
16. Git stash
 # You modified files A and B, but not committed them.
 git stash
 # saves changes and reverts to clean state
 git switch another-branch
 # dosomething else...
 git switch main
 git stash apply
 # brings back your changes
 17. To check branch is merge
  gitbranch–merged
 If branch not merged then displays its name
 18. To Delete multiple local branches at once
  gitbranch–d branc1 branch2 branch3

----------------------------------------------------------------------------------

1. Collaborative Coding – HOW TO DO
A. Collaboration Using an ORGANIZATION
Step 1: Create Organization

Login → GitHub

Click New Organization → Create a free organization

Step 2: Set Up Organization

Enter Organization name

Add email, verification details
Click Next

Step 3: Add Members

Add team members

Invitations go to others → They must accept

Then complete setup

Set Member Permissions

Go to:

Settings → Member privileges → Base permissions → Write
Projects → Base permissions → Write

Step 4: Create Repository Inside Organization

Create a repo inside the organization

Set it as Private (recommended)

Now all members can contribute based on permissions.

B. Collaboration Using Shared Repository
✔ Steps for Collaborator 1 (Owner)

Go to:

Settings → Collaborators → Add people


Add collaborator

They receive an invitation → They accept

✔ Steps for Collaborator 2
Step 1: Configure Git
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

Step 2: Clone Shared Repo

Copy repo URL → then:

git clone https://github.com/username/repo.git
cd repo

Step 3: Create Your Branch
git checkout -b feature/my-task

Step 4: Make Changes

After editing:

git add .
git commit -m "Meaningful commit message"

Step 5: Push Branch
git push origin feature/my-task

Step 6: Keep Your Branch Updated
git checkout main
git pull origin main
git checkout feature/my-task
git merge main

🚀 Exercise on FORK – HOW TO DO
✔ If you want to contribute to someone's public repo
Step 1: Fork Repo

Open:
https://github.com/Person1/project-name
Click Fork → repo becomes:
https://github.com/Person2/project-name

Step 2: Clone Your Fork
git clone https://github.com/Person2/project-name
cd project-name

Step 3: Make Changes, Commit, Push
git add .
git commit -m "My update"
git push origin main

Step 4: Open Pull Request

GitHub → Pull Request → Create PR

✔ Steps for Original Owner (Person 1)

Go to Pull Requests

Review → Merge Pull Request

Confirm merge

✅ 2. Resolving Merge Conflicts – HOW TO DO

Conflicts happen when two people edit the same line.

Step 1: Check Which Files Have Conflicts
git status


You will see:

both modified: f1.txt

Step 2: Open the File

Git adds conflict markers:

<<<<<<< HEAD
print("Hello from collaborator 1")
=======
print("Hello from collaborator 2")
>>>>>>> feature/branch2

Step 3: Fix the Conflict

Either keep one version OR combine:

print("Hello from collaborator 1")
print("Hello from collaborator 2")


Remove all:

<<<<<<<
=======
>>>>>>>

Step 4: Mark Conflict as Resolved
git add f1.txt

Step 5: Complete Merge
git commit

⚠️ To abort merge:
git merge --abort

🚨 Example of Real Conflict Scenario

Collaborator 2 adds a line → pushes → no conflict

Collaborator 1 adds a line at SAME PLACE → pushes → conflict

Collaborator 2 runs:

git pull


Opens README → sees markers → resolves → pushes

✅ 3. Creating and Applying Patch – HOW TO DO

A patch is a file that contains the changes (diff) of your commit.

A. How to CREATE Patch
Step 1: Clone the Public Repo
git clone https://github.com/Person1/project.git
cd project

Step 2: Edit File & Commit
git add .
git commit -m "Updated feature"

Step 3: Get Commit Hash
git log


Copy hash: abc1234

Step 4: Create Patch File
git format-patch -1 abc1234


This generates:

0001-your-commit-message.patch

B. How to SEND Patch

Send .patch file via email/WhatsApp.

C. How to APPLY Patch (Owner)

Place patch in the repo folder.

✔ Option 1 — Apply only changes (NO commit)
git apply 0001-file.patch
git add .
git commit -m "Applied patch"
----------------------------------------------------------------------------------------------------------------
Creating a Multi-Module Maven Project:

Open eclipse-> file-> new -> other -> Maven -> MavenProject ->click on next.
Check the first option: Create a Simple project(skip archetype selection) and click on next.
Give groupID: KMIT, artifact ID: MultiModule, in the packaging tab select the drop down and opt for pom.

Give Name: Multimodule creation and Description: Sample multimodule with parent child hierarchy and click on next.
Now the Multimodule folder is created and displayed in the project explorer on the left. Right click on the folder and opt new -> mavenModule

Check the option Create a Simple project(skip archetype selection, give the artifactID: MultiModuleChild1 and click on next and finish.

Now you can see, the module1 we created is displayed in the project explorer with a separate pom.xml file.
 
. Right click on the MultiModule folder in the project explorer and opt new -> mavenModule
Give the artifactID: MultiModuleChild2 and click on next.


In filters search for maven-archetype-webapp, select the version 1.1/1.5 and click on next.

Now click on finish, and confirm with a Y in the console.

Now you can watch the new child is been added to the parent project.

Note:Childs or Modules can be added to the projects who have the packaging type as pom. If we try to create a module within child1 it is not possible since its packaging is opted to JAR.

////////////////////////////////////////////////////////////////////////////////////////////
=>Linking two modules in a Parent Project:

Go to the module u want to connect. And add a dependency to other module on which the current module depends. For example if my child2 is dependent on child1. I have to change the dependencies in the pom.xml by adding a new dependency of child1.
Steps to add dependency:
Goto pom.xml of child2.

Navigate to dependencies tag. Update the dependencies with child1 dependency as given below, and save pom.xml after update.
<dependency>
		<groupId>KMIT</groupId>
			<artifactId>MultimoduleChild1</artifactId>
			<version>0.0.1-SNAPSHOT</version>
	</dependency>


Now build the child2 by right clicking it and opting run as->maven build.
The build will be a failure. Because we haven’t build the parent project and the child project. Child1 is dependent on parent. And Child2 is dependent on child2. SO we have to build ass the previous module first and then build the current child2.
After building parent and child1, build child2 now the build will be a Success




Executable JARs

Add to pom.xml:

<build>
<plugins>
<plugin>
<groupId>org.apache.maven.plugins</groupId>
<artifactId>maven-jar-plugin</artifactId>
<configuration>
<archive>
<manifest>
<mainClass>com.example.Main</mainClass>
</manifest>
</archive>
</configuration>
</plugin>
</plugins>
</build>


Run:
mvn package

java -jar target/myapp.jar

Building a WAR File
Create a Maven web project with structure:
src/main/webapp/
 └── WEB-INF/web.xml 


Add:
<packaging>war</packaging>
Command:
mvn package
Generates target/mywebapp.war → deploy on Tomcat server.
-----------------------------------------------------------------------------------------
4. Create Maven Java Project (Eclipse)

Open Eclipse → File → New → Project

Select Maven Project

Choose archetype:
maven-archetype-quickstart (1.4)

Enter:

Group ID → com.example

Artifact ID → my-maven-project

Finish → Project creates with pom.xml

Run Maven Tasks

Right-click project ➝ Run As →

✔ Maven Clean
✔ Maven Install
✔ Maven Test
✔ Maven Build → Goals → clean install test

Run program:
➡ Right-click App.java → Run As → Java Application
Output: Hello World

5. Create Maven Web Project (WAR)

File → New → Maven Project

Archetype → maven-archetype-webapp

Enter GroupId/ArtifactId

Add Servlet Dependency in pom.xml

<dependency>
    <groupId>javax.servlet</groupId>
    <artifactId>javax.servlet-api</artifactId>
    <version>4.0.1</version>
    <scope>provided</scope>
</dependency>

Configure Tomcat
Window → Show View → Servers → Add → Tomcat v9


Modify tomcat-users.xml → Add users & roles.

Build & Run Web Application

✔ mvn clean install
✔ Right-click index.jsp → Run on Server

Output → Webpage displayed in browser

💡 WAR creation:

<packaging>war</packaging>


Build command:

mvn package → target/*.war

6. Java Version Setup in POM
<plugin>
  <groupId>org.apache.maven.plugins</groupId>
  <artifactId>maven-compiler-plugin</artifactId>
  <version>3.11.0</version>
  <configuration>
    <source>17</source>
    <target>17</target>
  </configuration>
</plugin>


Verify:

mvn package
jar tf target/app.jar

7. JUnit Testing

📂 Place inside → src/test/java

public class AppTest {
    @Test
    public void testSum() {
        assertEquals(5, 2 + 3);
    }
}


Run:

mvn test


Reports generated:

target/surefire-reports/

8. Adding Resource Files

📂 Place inside:

src/main/resources/config.properties


Read in code:

InputStream input = getClass().getClassLoader().getResourceAsStream("config.properties");


After build → check:

target/classes/

9. Multi-Module Maven Project
parent/
 ├── pom.xml (packaging: pom)
 ├── core/
 │    └── pom.xml
 └── web/
      └── pom.xml


✔ Parent pom manages dependencies
✔ Modules build individually to their target/ folders

10. Creating Executable JAR

Add to pom.xml:

<build>
  <plugins>
    <plugin>
      <groupId>org.apache.maven.plugins</groupId>
      <artifactId>maven-jar-plugin</artifactId>
      <configuration>
        <archive>
          <manifest>
            <mainClass>com.example.Main</mainClass>
          </manifest>
        </archive>
      </configuration>
    </plugin>
  </plugins>
</build>


Build & Run:

mvn package
java -jar target/app.jar

----------------------------------------------------------------------------------
Maven java and web project and pushing into GITHUB

Creation of Maven Java Project Procedure Steps:
Step1: Open Eclipse IDE for Enterprise JAVA and WEB developers.

Step2: Click on File->New->Maven Project

Step3: Type quickstart in Filter and wait for artifacts to load.

Step4: Select org.apache.maven.archetypes   maven-archetype-quickstart 1.4 and click on next

Step5: Mention TeamID: as SE, ArtifactID: MavenJava and click on next

Step6: Now in Console we can see all the artifacts are grouped and console is waiting as Y: Now click Y and finally SE.MavenJava gets ready by combining all the artifacts.

Step7: We can see our MavenJava project ready with its own pom.xml file in the Project Explorer tool bar menu present at the left side.

Step8: Now click on src/main/java->SE.MavenJava->App.java where we can find a code sample for HELLO WORLD.

Step9: Now right click on App.java->Run as->Maven Clean

Step10: Now right click on App.java->Run as->Maven Install

Step11: Now right click on App.java->Run as->Maven Test

Step12: Now right click on App.java->Run as->Maven Build

Step13: In Goals, Type “clean install test”, click on apply next click on Run, for building the MavenJava project.

Step14: Every phase is checked and BUILD SUCCESS message can be seen in the console. 

Step15: Now right click on App.java->Run as->Java Application, click on OK.

Step16: Hello world is shown as output for MavenJava Project.

=>Creation of Maven Web Project Procedure Steps:

Step1: Open Eclipse IDE for Enterprise JAVA and WEB developers.

Step2: Click on File->New->Maven Project

Step3: Type webapp in Filter and wait for artifacts to load.

Step4: Select org.apache.maven.archetypes   maven-archetype-webapp 1.4 and click on next

Step5: Mention TeamID: as SE, ArtifactID: MavenWeb and click on next

Step6: Now in Console we can see all the artifacts are grouped and console is waiting as Y: Now click Y and finally SE.MavenWeb gets ready by combining all the artifacts.

Step7: We can see our MavenWeb project ready with its own pom.xml file in the Project Explorer tool bar menu present at the left side.

Step8: Now click on MavenWeb->src->main->Webapp->index.jsp where we can find a code sample for HELLO WORLD.

Step9: Now open browser and open mvnrepository.com

Step10: Search for JAVA servlet API and click on the latest version.

Step11: Copy the dependency code of the servlet. And paste it in MavenWeb’s pom.xml under target folder.

Step12: Now click on window in the menu bar, click on showview->servers.

Step13: Add servers by clicking on “No servers available”.

Step14: Select Tomcat v9.0 server/ Tomcat v11.0 server in the server type Click on next, select Apache Tomcat v9.0(optional), Click Apply and close.

Step15: Now we can find tomcat server attached to the project in server menu of the console. Duble click on it where the tomcat configuaration page appears.

Step16: select “Use Tomcat Installation”(which Is 2nd option) in Server locations, and modify the port numbers to “0” for admin port and “8085” for Https/1.1 and close the tab.

Step17: Double click “servers” folder present at the left side in project explorer, click on Tomcat v9.0 server at localhost-config->tomcat-users.xml, scroll to the end and paste the following exactly above </tomcat-users> tag and close the tab.

role rolename="admin-gui,manager-gui ,manager-script,manager-jmx,manager-status"/><user password="1234" roles="manager-gui, admin-gui ,manager-script" username="admin"/> 

Step18: Now right click on index.jsp ->Run as->Maven Clean

Step19: Now right click on index.jsp ->Run as->Maven Install

Step20: Now right click on index.jsp ->Run as->Maven Test

Step21: Now right click on index.jsp ->Run as->Maven Build

Step22: In Goals, Type “clean install test”, click on apply next click on Run, for building the MavenWeb project.

Step23: Every phase is checked and BUILD SUCCESS message can be seen in the console. 

Step24: Now right click on index.jsp ->Run as->Run on server, click on OK.

Step25: Select choose an existing server and click on finish.

Step26: Hello world Webpage is shown as output for MavenWeb Project.

=>Steps to Push the Maven Projects to GIT:
Java Project Push Procedure Steps:

Step1: Create two repositories for MavenJava and MavenWeb projects in your GitHUB account.

Step2: In eclipse right click on MavenJava folder present in project explorer and select show in local terminal option->GitBash.

Step3: execute: git init-> git branch –M main.

Step4: Now add your repository to the MavenJava using, git remote add origin <git java repository url> command.

Step5: execute: git add . -> git commit –m “Maven java push” -> git push –u origin main

Step6: Now refresh your GitHub account and we can see our MavenJava files are pushed to MavenJava repository in your GitHub account.
Web Project Push Procedure Steps:
   Step1: In eclipse right click on MavenWeb folder present in project explorer and select show in local terminal option->GitBash.
   Step2: execute: git init-> git branch –M main.
   Step3: Now add your repository to the MavenWeb using, git remote add origin <git Web repository url> command.
   Step4: Push your web project same as Java to GitHub. 
   Step5: Now refresh your GitHub account and we can see our MavenWeb files are pushed to MaveWeb repository in your GitHub account.

Conclusion: we have learnt creation of Java and Web project through Maven and pushing them to GitHub.

A. Deploying to Tomcat from Eclipse
1️⃣ Add Tomcat to Eclipse

Download & extract Tomcat (if not already):

Tomcat 9 or 10 is fine (zip for Windows).

In Eclipse:

Go to Window → Preferences → Server → Runtime Environments

Click Add…

Choose Apache → Tomcat v9.0 (or whichever you installed)

Click Next

For Tomcat installation directory, browse to your Tomcat folder (where bin, webapps, etc. are).

Finish.

2️⃣ Add your project to the Tomcat server

Open the Servers view:

Window → Show View → Servers

In the Servers panel:

Right-click → New → Server

Select Tomcat v9.0 Server (or your version).

Click Next

In the list of projects, select my-exam-webapp and click Add >

Finish.

3️⃣ Start Tomcat from Eclipse

In Servers view, right-click your Tomcat server → Start

Eclipse will build and publish your app to Tomcat automatically.

Open a browser and hit:

http://localhost:8080/my-exam-webapp


The context path is usually the <finalName> from your pom.xml → my-exam-webapp.

If you have a index.jsp in src/main/webapp, it should load.

B. Deploying manually using the WAR

If you want to do it outside Eclipse:

1️⃣ Build the WAR with Maven

In your project directory (where pom.xml is):

mvn clean package


This will create:

target/my-exam-webapp.war

2️⃣ Copy WAR to Tomcat

Go to your Tomcat folder → webapps

Copy my-exam-webapp.war into webapps/

Start Tomcat:

On Windows: double-click bin/startup.bat

Or run from cmd:

cd C:\path\to\tomcat\bin
startup.bat


Tomcat will automatically unpack the WAR into webapps/my-exam-webapp/.

3️⃣ Access the app

Open browser:

http://localhost:8080/my-exam-webapp

-----------------------------------------------------------------------

Here is a **clean, well-structured Lab Action Plan for Week 5 – Docker with Redis & Dockerfile**, simplified for notes and easy execution during lab.

---

# 📘 **WEEK-5 LAB ACTION PLAN – Docker**

---

## **Part 1 – Working with Docker CLI using Redis**

### 🔹 Step-1 — Pull Redis Image

bash
docker pull redis

Downloads Redis image from Docker Hub.

### 🔹 Step-2 — Run Redis Container

bash
docker run --name my-redis -d redis

* Creates and starts a container named **my-redis**
* `-d` → runs container in background

### 🔹 Step-3 — Check Running Containers

bash
docker ps

docker-compose.yaml :--

version: "3.9"
services:
  web:
    image: nginx:latest
    ports:
      - "8080:80"

  db:
    image: postgres:15
    environment:
      POSTGRES_USER: demo
      POSTGRES_PASSWORD: demo
      POSTGRES_DB: demo_db

Shows only *active* containers.

### 🔹 Step-4 — Access Redis CLI inside Container

bash
docker exec -it my-redis redis-cli

Now run commands like:

SET name "Alice"
GET name

### 🔹 Step-5 — Stop Container

bash
docker stop my-redis


### 🔹 Step-6 — Start Container Again

bash
docker start my-redis

### 🔹 Step-7 — Remove Container

bash
docker rm my-redis

### 🔹 Step-8 — Remove Redis Image

bash
docker rmi redis
---
Run the setup:

docker compose up -d

III. Open your browser and visit: http://localhost:8080.

IV. Expected Output:

Nginx welcome page is displayed.
db container runs in the background.

2.Write and interpret docker-compose.yml files
Task:
Modify docker-compose.yml to add a Redis cache:

  redis:
    image: redis:alpine

II. Add a depends_on so web waits for Redis:
  web:
    image: nginx:latest
    ports:
      - "8080:80"
    depends_on:
      - redis

III. Restart the setup:
docker compose up -d
docker compose ps

IV. Expected Output:

Three services (web, db, redis) are listed as running.

3.Deploy across different machines
Task:
Zip your compose-lab folder.

Transfer it to another machine with Docker Compose installed.

II. Run:
docker compose up -d

Check that Nginx and Postgres work there as well.

III. Expected Output:
The same services run on the new machine without changes.

4.Networking and persistent storage
Task:
Update your docker-compose.yml to add a custom network and volume:

networks:
  app-net:

volumes:
  db-data:

services:
  web:
    image: nginx:latest
    ports:
      - "8080:80"
    networks:
      - app-net
    depends_on:
      - db

  db:
    image: postgres:15
    environment:
      POSTGRES_USER: demo
      POSTGRES_PASSWORD: demo
      POSTGRES_DB: demo_db
    volumes:
      - db-data:/var/lib/postgresql/data
    networks:
      - app-net

II. Run:
docker compose up -d
III. Insert some data into Postgres (optional with psql).
IV. Remove containers:
docker compose down
V. Start again:
docker compose up -d
VI. Expected Output:
Database data persists across restarts.
Services communicate via the app-net network using service names.

5.Faster iteration during development
Task: 
Create a simple Flask app in app.py:

from flask import Flask
app = Flask(__name__)
@app.route("/")
def home():
    return "Hello from Flask + Docker!"
if __name__ == "__main__":
    app.run(host="0.0.0.0", port=5000)

II. Add a Dockerfile in the same folder:

FROM python:3.10-slim
WORKDIR /app
COPY app.py /app/
RUN pip install flask
CMD ["python", "app.py"]

III. Update docker-compose.yml:
  web:
    build: .
    ports:
      - "5000:5000"
    depends_on:
      - db
IV. Run:
docker compose up --build
Visit http://localhost:5000.
Change the return text in app.py (e.g., "Hello Docker Compose!").
V. Rebuild:
docker compose up --build
VI. Expected Output:
New message appears instantly after rebuild.
---

## **Part 2 – Working with Dockerfile**

### 📁 Step-1 — Create Project Directory

Windows:

bash
mkdir C:\DockerProjects\Redis
cd C:\DockerProjects\Redis


Mac/Linux:

bash
mkdir ~/DockerProjects/Redis
cd ~/DockerProjects/Redis

### 📄 Step-2 — Create `Dockerfile`

FROM redis:latest
CMD ["redis-server"]


---

### 🏗 BUILD IMAGE

bash
docker build -t redisnew .

Creates image named **redisnew**

### ▶ RUN CONTAINER

bash
docker run --name myredisnew -d redisnew

### CHECK CONTAINERS

bash
docker ps
docker ps -a   # includes stopped containers

### STOP CONTAINER

bash
docker stop myredisnew

---

---

## **PART 3 – Docker Hub Operations**

### 🔐 Login

bash
docker login

### 📌 Commit & Create Image From Container

bash
docker commit <container_ID> budarajumadhurika/redis1


### 📥 View Images

bash
docker images

### 📤 Push to Docker Hub

bash
docker push budarajumadhurika/redis1

### ❌ Delete Container

bash
docker rm <container_ID>

### ❌ Remove Image

bash
docker rmi budarajumadhurika/redis1

---

---

## **Part-4 — Pull Again & Run from Docker Hub**

### 📥 Pull Image from Hub

bash
docker pull budarajumadhurika/redis1


### ▶ Run Redis from Hub Image

bash
docker run --name myredis -d budarajumadhurika/redis1


### 🔗 Enter Redis CLI

bash
docker exec -it myredis redis-cli


Inside Redis:


SET name "Abcdef"
GET name
exit


### Stop & Remove Container & Image

bash
docker stop myredis
docker rm <container_ID>
docker images
docker rmi budarajumadhurika/redis1

---

## **Optional: Logout**

bash
docker logout

---

------------------------------------------------------------------------------------------------------
Here is a **clean, exam-ready, easy-to-remember** version of the steps you provided.
I rewrote everything in a **simple structured format**, removing confusion while keeping all important points.

---

# ✅ **Maven Java Automation — Jenkins Steps (Clean Notes for Exam)**

---

## **Step 1: Open Jenkins**

* Open browser → `localhost:8080`
* Click **New Item** → choose **Freestyle Project**
* Enter name: **MavenJava_Build**
* Click **OK**

---

## **Step 2: Configure MavenJava_Build**

### **Project Setup**

* **Description:** Java Build demo
* **Source Code Management (SCM):**

  * Git Repo URL → *Git Maven Java Project URL*
  * Branch → */main* or */master*

### **Build Steps**

1. **Invoke top-level Maven targets**

   * Maven Version: **MAVEN_HOME**
   * Goals: **clean**

2. **Invoke top-level Maven targets**

   * Maven Version: **MAVEN_HOME**
   * Goals: **install**

### **Post-build Actions**

* **Archive artifacts**

  * Files: `**/*`
* **Build other projects**

  * Next Project: **MavenJava_Test**
  * Trigger: **Only if build is stable**
* Click **Apply** → **Save**

---

## **Step 3: Create MavenJava_Test Project**

* New Item → **MavenJava_Test**
* Click **OK**

### **Configure MavenJava_Test**

* **Description:** Test demo
* **Build Environment:**

  * Tick → *Delete workspace before build starts*

### **Build Steps**

1. **Copy artifacts from another project**

   * From project: **MavenJava_Build**
   * Build: *Stable build only*
   * Artifacts: `**/*`

2. **Invoke top-level Maven targets**

   * Maven Version: **MAVEN_HOME**
   * Goals: **test**

### **Post-build Actions**

* Archive artifacts → `**/*`
* Save

---

## **Step 4: Create Pipeline View**

* Dashboard → click **+** beside "All"
* View name: **MavenJava_Pipeline**
* Select **Build Pipeline View**
* **Initial job:** MavenJava_Build
* Save

---

## **Step 5: Run Pipeline**

* Click **Run** icon
* Open console (black box) → check logs
* If both builds → green color → pipeline successful

---

# ✅ **Maven Web Automation — Jenkins Steps (Clean Notes)**

---

## **Step 1: Create MavenWeb_Build**

* New Item → **MavenWeb_Build**
* Description: Web Build demo
* SCM:

  * Git URL: *Git Maven Web repo URL*
  * Branch: */main* or */master*

### **Build Steps**

* Maven → clean
* Maven → install

### **Post-build Actions**

* Archive artifacts → `**/*`
* Build other projects → **MavenWeb_Test**

  * Trigger: Only if stable
* Save

---

## **Step 2: Create MavenWeb_Test**

* Description: Test demo
* Build Environment: Delete workspace before build

### **Build Steps**

1. Copy Artifacts

   * From project: **MavenWeb_Build**
   * Stable build only
   * Artifacts: `**/*`

2. Maven Goals → **test**

### **Post-Build**

* Archive artifacts → `**/*`
* Build other projects → **MavenWeb_Deploy**
* Save

---

## **Step 3: Create MavenWeb_Deploy**

* Description: Web Code Deployment
* Build Environment → Delete workspace before build

### **Build Steps**

* Copy artifacts

  * From: MavenWeb_Test
  * Stable build only
  * Artifacts: `**/*`

### **Post-build Actions**

* Deploy WAR/EAR to Container

  * WAR File: `**/*.war`
  * Context path: **webpath**
  * Add container: **Tomcat 9.x Remote**

    * Username: admin
    * Password: 1234
    * Tomcat URL: `http://localhost:8085/`

* Save

---

## **Step 4: Create Pipeline View**

* Dashboard → "+"
* View name: **MavenWeb_Pipeline**
* Select: **Build Pipeline View**
* Initial Job → MavenWeb_Build
* Save

---

## **Step 5: Run & Verify**

* Click **Run**
* Check green status
* Open Tomcat → `http://localhost:8085/`
* Open `/webpath`
* Enter Tomcat credentials
* Application should load

---


_________________________________________________
JENKINS PIPELINE (GENERAL CONFIGURATION)

(Simple & Clean for Exams)

1. Description

In this section, we enter a brief explanation about the project.
Example:
“This project demonstrates automated build, test, and package using Jenkins Pipeline.”

2. Build Triggers

In this section, we can select triggers such as:

Build periodically
* * * * *

(Choose based on requirement.)

3. Advanced Project Options

Under this section:

Go to Definition

Select Pipeline Script

This enables us to write a full scripted pipeline directly inside Jenkins.

4. Pipeline Script Section

pipeline {
    agent any
    tools{
        jdk 'JAVA_HOME'
        maven 'MAVEN_HOME'
    }
    stages {
        stage('git repo & clean') {
            steps {
                bat "rmdir /s /q Harshitha_Jenkins_Maven || exit 0"
                bat "git clone https://github.com/Harshitha-Macha/Harshitha_Jenkins_Maven.git"
                bat "mvn clean -f Harshitha_Jenkins_Maven/pom.xml"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f Harshitha_Jenkins_Maven/pom.xml" 
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f Harshitha_Jenkins_Maven/pom.xml"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f Harshitha_Jenkins_Maven/pom.xml"
            }
        }
    }
}
5. Save Configuration

_______
DEPLOYMENT OF index.html USING EC2 INSTANCE IN AWS Step 1: Login to AWS / Canvas Account

Open the Course Invitation Mail → click Start.

AWS Academy opens → Select Student Login → enter email & password.

Click Modules.

Scroll down → select Launch AWS Academy Lab.

Click Start Lab and wait until the AWS icon turns Red → Green.

Click AWS to enter the console.

Step 2: Create an EC2 Instance

In the AWS Console → search for EC2 → click it.

Click Launch Instance.

Stage 1: Name

Give instance name: ubuntu.

Stage 2: Select AMI

Select Ubuntu Server (Free Tier Eligible).

Stage 3: Architecture

Ensure 64-bit (x86) is selected.

Stage 4: Instance Type

Choose t2.micro (1 CPU, 1 GB RAM, free tier).

Stage 5: Create Key Pair

Click Create New Key Pair.

Enter keypair name.

Download the .pem file.

Save it safely (example: Desktop → AWS folder).

Stage 6: Network Settings – Security Group

Enable:

HTTP (80)

HTTPS (443)

SSH (22)

(These are required to access the webpage.)

Stage 7: Storage

Default storage: 8 GB (root volume).

Stage 8: Launch

Click Launch Instance.

Go to Instances page.

Wait until instance shows:

Running

Status Checks = 2/2 passed

Connect

Tick the instance → click Connect → open SSH Client tab.

Copy the ssh -i command for later use.

Step 3: Connect Local System to EC2 (SSH) Step a:

Copy the path where the .pem file is saved. Example: D:\SUNNY\SELABWEB\AWS

Step b:

Open PowerShell (Run as Administrator). Navigate to the key file path:

cd

Step c:

From AWS, copy the SSH command under “SSH Client”.

Step d:

Paste and run the SSH command in PowerShell:

ssh -i ".pem" ubuntu@

Step 4: Install Required Software in Ubuntu

Run the following commands:

Update packages sudo apt update

Install Docker sudo apt-get install docker.io

Install Git sudo apt install git

Install Nano (Text Editor) sudo apt install nano

Step 5: Create Web Application and Push to GitHub Step a:

Create an index.html file (Example folder).

Step b:

Open Git Bash in that folder.

Step c:

Initialize Git:

git init git add . git commit -m "first commit"

Step d:

Create a new GitHub repository (example: AWS).

Step e:

Run commands (copied from GitHub):

git branch -M main git remote add origin git push -u origin main

Step f:

Refresh GitHub → confirm index.html uploaded.

Step 6: Clone Repository in EC2 Server Step g:

Copy the repository HTTPS link.

Step h:

Clone it inside EC2:

git clone

Step i:

Navigate into folder:

cd AWS ls

Step 7: Create Dockerfile and Build Image Step j:

Create Dockerfile:

nano Dockerfile

Step k:

Add the following content:

FROM nginx:latest COPY . /usr/share/nginx/html

Save:

Ctrl + O → Enter

Ctrl + X (exit)

Step L: Build Docker Image sudo docker build -t mywebapp .

Step m: Run Docker Container sudo docker run -d -p 80:80 mywebapp

Step 8: Test the Deployment Step n:

Open EC2 → Instances.

Step o:

Copy Public IPv4 Address.

Step p:

Open a browser → paste the IP:

http://

If HTTPS doesn’t work, use HTTP. The index.html page should load.

Step 9: Stop and Terminate Resources Step Q: Stop Container sudo docker ps sudo docker stop

Terminate EC2 Instance

Go to Instances

Click Instance State → Terminate

End Lab

Click End Lab in AWS Academy.
---------------------------------------------------------------------------------------------------------------------------------------------
JENKINS PIPELINE SCRIPT

pipeline {
    agent any
    tools {
        maven 'MAVEN_HOME'
    }
    stages {
        stage('Clone Repo & Clean') {
            steps {
                bat "git clone https://github.com/Kavya-286/web-app"
                bat "mvn -f web-app/pom.xml clean"
            }
        }
        stage('Install') {
            steps {
                bat "mvn -f web-app/pom.xml install"
            }
        }
        stage('Test') {
            steps {
                bat "mvn -f web-app/pom.xml test"
            }
        }
        stage('Package') {
            steps {
                bat "mvn -f web-app/pom.xml package"
            }
        }
    }
}

============================================
minikube commands :
minikube start --driver=hyperv

minikube start --driver=docker

minikube status

minikube kubectl -- get pods -A
minikube dashboard
Minikube version
kubectl version –client
minikube logs
minikube update-check
minikube update

Minikube Automation Steps
Step 1: Start Minikube Cluster
Open your terminal and run the command:
minikube start

Step 2: Create and Manage Deployment
Create  an application in Kubernetes:

Command:
kubectl create deployment mynginx --image=nginx
kubectl set image deployment/myngnix nginx=nginx:latest
kubectl get deployments
kubectl get pods
kubectl describe pods
kubectl expose deployment mynginx --type=NodePort --port=80 --target-port=80

Step 3: Scale the Deployment
Command:Scales the Nginx deployment to 4 replicas (pods).
kubectl scale deployment mynginx --replicas=4
kubectl get service mynginx

Step 4: Access the Nginx App
Using Port Forwarding:
Command:
kubectl port-forward svc/mynginx 8081:80
Access the app via http://localhost:8081.
If Error, use this option, Using Minikube Tunnel:
Start the tunnel:
command: minikube tunnel
etrieve the service URL:
command:minikube service mynginx --url
Open the provided URL in your browser.
Open the kubernets dashboard
Open the minikube dashboard	
command : Minikube dashboard

kubectl delete deployment mynginx
kubectl delete service mynginx

Nagios Automation Steps
Step 1: Pull the Nagios Docker Image
Open a terminal and run:
docker pull jasonrivers/nagios:latest

Step 2: Run Nagios
Command:
docker run --name nagiosdemo -p 8888:80 jasonrivers/nagios:latest

Step 3: Access Nagios Dashboard
Open your browser and navigate to:
http://localhost:8888
Login Credentials:
Username: nagiosadmin
Password: nagios

to Delete the Container:
Command:
docker rm nagiosdemo

to Delete the Nagios image:
docker rmijasonrivers/nagios:latest

=======================================================================================

Setting Up  Jenkins CI------using GitHub Webhook with Jenkins 

Step 1: Configure Webhook in GitHub
Go to your GitHub repository
step 2:Navigate to Settings → Webhooks.
step 3:Click “Add webhook”.
step 4:In the Payload URL field:
Enter the Jenkins webhook URL in the format:
http://<jenkins-server-url>/github-webhook/
Note: If Jenkins is running on localhost, GitHub cannot access it directly.
Use ngrok to expose your local Jenkins to the internet:

ngrok.exe http <Jenkins local host:8080>
Use the generated ngrok URL, e.g.:
http://abc123.ngrok.io/github-webhook/
step 5:Set Content type to:
application/json
step 6:Under “Which events would you like to trigger this webhook?”, select:
 Just the push event
step 7:Click “Add webhook” to save.



 Step 2: Configure Jenkins to Accept GitHub Webhooks
1 Open Jenkins Dashboard.

2 Select the job (freestyle or pipeline) you’ve already created

3 Click Configure.

4 Scroll down to the Build Triggers section.

5 Check the box: ✅GitHub hook trigger for GITScm polling

6 Click Save.

Step 3: Test the Setup
1 Make any code update in your local repo and push it to GitHub

2 Once pushed, GitHub will trigger the webhook.
3 Jenkins will automatically detect the change and start the build pipeline


Setting Up   Jenkins Email Notification Setup (Using Gmail with App Password)
Creation of app password
1. Gmail: Enable App Password (for 2-Step Verification)
i. Go to: https://myaccount.google.com

ii. Enable 2-Step Verification
Navigate to:
Security → 2-Step Verification

Turn it ON
Complete the OTP verification process (via phone/email)

iii. Generate App Password for Jenkins
Go to:
Security → App passwords

Select:
App: Other (Custom name)
Name: Jenkins-Demo
Click Generate
Copy the 16-digit app password
Save it in a secure location (e.g., Notepad)

 2.  Jenkins Plugin Installation
i. Open Jenkins Dashboard
ii. Navigate to:
Manage Jenkins → Manage Plugins
iii. Install Plugin:
Search for and install:
Email Extension Plugin


3. Configure Jenkins Global Email Settings
i. Go to:
Manage Jenkins → Configure System

A. E-mail Notification Section
Field
Value
SMTP Server
smtp.gmail.com
Use SMTP Auth
✅ Enabled
User Name
Your Gmail ID (e.g., archanareddykmit@gmail.com)
Password
Paste the 16-digit App Password
Use SSL
✅ Enabled
SMTP Port
465
Reply-To Address
Your Gmail ID (same as above)
➤ Test Configuration
Click: Test configuration by sending test e-mail
Provide a valid email address to receive a test mail
✅ Should receive email from Jenkins

B. Extended E-mail Notification Section
Field
Value
SMTP Server
smtp.gmail.com
SMTP Port
465
Use SSL
✅ Enabled
Credentials
Add Gmail ID and App Password as Jenkins credentials
Default Content Type
text/html or leave default
Default Recipients
Leave empty or provide default emails
Triggers
Select as per needs (e.g., Failure)


4.  Configure Email Notifications for a Jenkins Job
i. Go to:
Jenkins → Select a Job → Configure

ii. In the Post-build Actions section:
Click: Add post-build action → Editable Email Notification
A. Fill in the fields:
Field
Value
Project Recipient List
Add recipient email addresses (comma-separated)
Content Type
Default (text/plain) or text/html
Triggers
Select events (e.g., Failure, Success, etc.)
Attachments
(Optional) Add logs, reports, etc.


iii. Click Save

 Now your Jenkins job is set up to send email notifications based on the build status!

==========================================================================================================================
AWS :::

 sudo apt update 
sudo apt-get install docker.io
 sudo apt install git
sudo apt install nano

 git clone <paste the github link of maven-web-java project>
 Step 4:-  nano Dockerfile 
 Step 1:- build your image 
	docker build –t <imagename> .(dot)
Step 2:- check for images
Step 3:- run image
	docker  run –d  --name app-demo –p 6060:8080 <image name> 

 then use public ip and paste in chrome
 
 
### 1. Clone Repository
bash
git clone https://github.com/your-username/dynamic-data-table-manager.git
cd dynamic-data-table-manager

========================================================================================================================
