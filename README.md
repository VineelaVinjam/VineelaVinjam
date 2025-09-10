## Hi there 👋
 I'm Vineela
 �� I’m passionate about Full Stack Development
Cybersecurity- �� Currently learning: Spring Boot, MongoDB, and GitHub Actions
�� Fun Fact: I once debugged a 50-line error just by adding a semicolon
## ��️ Skills &amp; Tools
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-
badge&amp;logo=java&amp;logoColor=white)
![Spring Boot](https://img.shields.io/badge/SpringBoot-6DB33F?style=for-the-
badge&amp;logo=spring-boot&amp;logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4DB33D?style=for-the-
badge&amp;logo=mongodb&amp;logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-
badge&amp;logo=git&amp;logoColor=white)
## �� GitHub Stats
![GitHub Stats](https://github-readme-
stats.vercel.app/api?username=renukacsit&amp;show_icons=true&amp;theme=radical)
![Top Languages](https://github-readme-stats.vercel.app/api/top-
langs/?username=renukacsit&amp;layout=compact)
![GitHub Stats](https://github-readme-
stats.vercel.app/api?username=renuka1163&amp;show_icons=true)
 
 Connect with Me- ✉️ Email: vvineela_cse2305k0@mgit.ac.in- �� LinkedIn: [Vineela Vinjam](https://www.linkedin.com/in/vineela-vinjam-9781b9379/)
 Source Code Management using Git &amp; GitHub –
Command Summary
Part A: Local Git Operations (Basic)
 Initialize Repository:
mkdir git-basics
cd git-basics
git init
 Create a File &amp; Commit:
echo &quot;Your Name - Course Info&quot; &gt; intro.txt
git add intro.txt
git commit -m &quot;Initial commit&quot;
Part B: Branching &amp; Merging
 Create &amp; Switch Branch:
git checkout -b bio-update
echo -e &quot;\nHobby1\nHobby2\nHobby3&quot; &gt;&gt; intro.txt
git add intro.txt
git commit -m &quot;Added 3 hobbies&quot;
 Merge Branch to Main:
git checkout main
git merge bio-update
 Delete Branch:
git branch -d bio-update

Part C: Remote Operations with GitHub
 Push Local Repo to GitHub:
git remote add origin https://github.com/yourusername/scm-
practice.git
git branch -M main
git push -u origin main
 Push a Feature Branch:
git checkout -b skills-section
echo -e &quot;Skill1\nSkill2\nSkill3&quot; &gt; skills.txt
git add skills.txt
git commit -m &quot;Added top 3 skills&quot;
git push -u origin skills-section
Part D: Merge Conflicts &amp; Resolution
 Create a Conflict and Resolve:
# Modify intro.txt differently on both branches
# On main branch
git checkout main
echo &quot;Main update line&quot; &gt;&gt; intro.txt
git commit -am &quot;Main branch update to intro.txt&quot;
# On skills-section branch
git checkout skills-section
echo &quot;Skills branch update line&quot; &gt;&gt; intro.txt
git commit -am &quot;Skills section update to intro.txt&quot;
# Try to merge

git checkout main
git merge skills-section
# Resolve conflict manually in intro.txt, then:
git add intro.txt
git commit -m &quot;Resolved merge conflict in intro.txt&quot;
Part E: Collaboration (Optional)
 Clone and Contribute:
git clone https://github.com/classmateusername/scm-practice.git
cd scm-practice
git checkout -b contribution
echo &quot;Your Name&quot; &gt; contributor.txt
git add contributor.txt
git commit -m &quot;Added contributor info&quot;
git push -u origin contribution
Final Step
 Miscellaneous Useful Commands:
git branch -a
git log --oneline --graph --all
///////////////////////////////////////////////////////////////////////////////
Jenkins Freestyle Project - Practical Tasks

Task 1: Create a Simple Hello World Project
• Create a new Freestyle project called HelloWorldJob.
• Add a Windows batch command or Shell command (Linux) to print 'Hello, Jenkins!'.
• Run the job and check the Console Output.
Solution:
Windows:
echo Hello, Jenkins!
Linux:
echo "Hello, Jenkins!"

Task 2: Use Workspace Variable
• Create a project called WorkspaceJob.
• Add a build step that prints the WORKSPACE environment variable.
• Verify in the console output that the path to the workspace is correct.
Solution:
Windows:
echo The workspace path is: %WORKSPACE%
Linux:
echo "The workspace path is: $WORKSPACE"

Task 3: File Creation and Copy
• Create a project FileCopyJob.
• Add a batch command that creates a file test.txt in the workspace and copies it to a folder.
• Verify the file is copied.
Solution:
Windows:
echo Hello from Jenkins > %WORKSPACE%\test.txt
copy %WORKSPACE%\test.txt C:\inetpub\wwwroot\Devops\
Linux:
echo "Hello from Jenkins" > $WORKSPACE/test.txt
cp $WORKSPACE/test.txt /var/www/devops/

Task 4: Parameterized Build
• Create a project ParameterizedJob.
• Add a String Parameter called USERNAME.
• In the build step, print Hello, $USERNAME.
• Build the job multiple times with different values and check the output.
Solution:
Windows:

echo Hello, %USERNAME%
Linux:
echo "Hello, $USERNAME"

Task 5: Schedule Builds
• Create a project ScheduledJob.
• Configure it to run every 2 minutes (H/2 * * * *).
• In the build step, echo the current date and time.
• Verify multiple builds are triggered automatically.
Solution:
Windows:
echo Current date and time: %date% %time%
Linux:
echo "Current date and time: $(date)"

Task 6: Trigger by SCM (Git)
• Create a project GitJob.
• Connect it to a GitHub repository.
• Configure to pull the latest code.
• In the build step, print the last commit message.
• Verify Jenkins fetches and displays commits.
Solution:
Linux/Windows (Git Bash):
git log -1 --pretty=%B
/////////////////////////////////////////////////////////////////////////////////////
Jenkins Pipeline Project Tasks - Step by Step
Solutions

Task 1: Simple Echo Pipeline
1. Create a new pipeline job in Jenkins named **EchoPipeline**.
2. Use the following Declarative pipeline script:
```
pipeline {
agent any
stages {
stage('Echo') {
steps {
echo 'Hello, Jenkins Pipeline!'
}
}
}
}
```
3. Run the job → Check console output → You should see `Hello, Jenkins Pipeline!`.
Task 2: Multi-Stage Pipeline
1. Create a pipeline job called **BuildTestPipeline**.
2. Use the following script:
```
pipeline {
agent any
stages {
stage('Build') {
steps { echo 'Building the project...' }
}
stage('Test') {
steps { echo 'Running tests...' }
}
stage('Deploy') {
steps { echo 'Deploying application...' }
}
}
}
```
3. Run the job → Stage view will show Build, Test, and Deploy stages.

Task 3: Workspace File Handling
1. Create a pipeline job called **FilePipeline**.
2. Script:
```

pipeline {
agent any
stages {
stage('Create File') {
steps {
writeFile file: 'pipeline.txt', text: 'Created by Jenkins Pipeline'
}
}
stage('Show File') {
steps {
powershell 'Get-Content pipeline.txt' // use 'cat' for Linux
}
}
}
}
```
3. Run job → Console output will display file content.

Task 4: Parameterized Pipeline
1. Create a pipeline job called **UserPipeline**.
2. Add a **String Parameter** named `USERNAME`.
3. Script:
```
pipeline {
agent any
parameters {
string(name: 'USERNAME', defaultValue: 'User', description: 'Enter your name')
}
stages {
stage('Greet') {
steps {
echo "Hello, ${params.USERNAME}!"
}
}
}
}
```
4. Run builds with different USERNAME values.

Task 5: Scheduled Pipeline
1. Create a job called **ScheduledPipeline**.
2. Configure build triggers → Add `H/5 * * * *` (every 5 minutes).
3. Script:
```
pipeline {
agent any
triggers {
cron('H/5 * * * *')
}
stages {

stage('Show Time') {
steps {
powershell 'Get-Date' // use 'date' for Linux
}
}
}
}
```
4. Jenkins will trigger the job automatically every 5 minutes.
Task 6: Git-Integrated Pipeline
1. Create a job called **GitPipeline**.
2. Configure it with your GitHub repo URL.
3. Script:
```
pipeline {
agent any
stages {
stage('Checkout') {
steps {
git branch: 'main', url: 'https://github.com/your-repo.git'
}
}
stage('Build') {
steps {
echo 'Compiling code...'
}
}
stage('Commit Info') {
steps {
powershell 'git log -1 --pretty=%B' // use 'sh' on Linux
}
}
}
}
```
4. Run → Jenkins will pull code, simulate build, and show last commit message.
<!--
**VineelaVinjam/VineelaVinjam** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.
![GitHub Stats](https://github-readme-
stats.vercel.app/api?username=renuka1163&amp;show_icons=true)

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
