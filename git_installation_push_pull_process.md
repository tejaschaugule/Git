Git Setup and Basic Usage Guide
1. Install Git
On Linux (CentOS/RHEL)

Update the system:

yum update -y

Install Git:

yum install git -y

Configure Git user details:

git config --global user.name "tejas"
git config --global user.email "tejaschaugule#@gmail.com"

Verify configuration:

git config --list
Push Code to GitHub
Scenario:

User (e.g., working from Mumbai) creates code locally and wants to push it to GitHub.

1. Create a directory
mkdir mumbai
2. Change into the directory
cd mumbai
3. Initialize a Git repository
git init
4. Create files and write code
5. Check Git status
git status
6. Move files to staging
git add .
7. Check status again
git status
8. Commit the changes
git commit -m "My first commit from Mumbai"
9. View commit log
git log
10. View content of a commit
git show <commit-id>
11. Create a new repository on GitHub
12. Link local repository to GitHub
git remote add origin https://github.com/tejaschaugule/testgit.git
13. Push code to GitHub
git push -u origin master

Enter GitHub username and token when prompted.

14. Code is now updated on GitHub.
Change or Check Remote Repository
Check which remote repository is set:
git remote -v
Change the remote URL
git remote set-url origin https://github.com/tejaschaugule/test.git
Pull Code from GitHub
Fresh Clone (Recommended)

If pulling a project for the first time:

git clone https://github.com/tejaschaugule/dubai.git

This automatically:

Creates a new folder

Initializes Git

Sets origin remote

Downloads all files

Pull Updates (Repo Already Cloned)
Scenario:

Another developer (e.g., working from Dubai) pushes changes to GitHub, and you want to fetch them locally.

1. Go to your project directory:
cd /path/to/your/project
2. Verify remote:
git remote -v
3. Pull latest changes:

If the branch name is master:

git pull origin master

If using main:

git pull origin main
4. Local repository is now updated.
Important Notes

Use git pull only when the repository is already cloned.

Commit your local changes before pulling to avoid conflicts.

git clone is the simplest option when starting fresh.

End of Document
