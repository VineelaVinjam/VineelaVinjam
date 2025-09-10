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
