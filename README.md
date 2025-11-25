# GitHub Merge Conflict Demonstration Project  
### Cloud & DevOps Assignment

This project is a simple JavaScript-based Greeting App created to demonstrate essential Git and GitHub version control concepts, including branching, merging, and resolving an intentional merge conflict.

---

## 📌 Project Overview
The goal of this assignment was to:

- Initialize a Git repository  
- Create multiple branches  
- Make independent changes in those branches  
- Produce a merge conflict by modifying the same line in two branches  
- Resolve the conflict manually  
- Push all branches and the final merged code to GitHub  

A small JavaScript app was used to keep the focus on Git operations.

---

## 📁 Project Files

index.html
script.js
README.md

pgsql
Copy code

- **index.html** – Displays the greeting message  
- **script.js** – Contains the function where the intentional merge conflict was created  
- **README.md** – Documentation of the workflow  

---

## 🛠️ Git Workflow Followed

### **1. Repository Setup**
git init
git branch -M main
git add .
git commit -m "Initial commit"
git remote add origin <repo-url>
git push -u origin main

yaml
Copy code

---

### **2. Created First Branch: feature-addition**
git checkout -b feature-addition

kotlin
Copy code
Updated the message inside `script.js`:
```javascript
return "Hello from Feature Addition branch!";
Then:

sql
Copy code
git add .
git commit -m "Updated message in feature-addition"
git push -u origin feature-addition
3. Created Second Branch: feature-update-message
css
Copy code
git checkout main
git checkout -b feature-update-message
Updated the SAME line differently:

javascript
Copy code
return "Hello from Update Message branch!";
Then:

sql
Copy code
git add .
git commit -m "Updated message in feature-update-message"
git push -u origin feature-update-message
4. Merged First Branch Into Main (No Conflict)
css
Copy code
git checkout main
git merge feature-addition
git push
5. Merged Second Branch Into Main (Conflict Occurred)
sql
Copy code
git merge feature-update-message
Git produced a merge conflict in script.js.

Conflict markers appeared:

python-repl
Copy code
<<<<<<< HEAD
...
=======
...
>>>>>>> feature-update-message
6. Resolved the Merge Conflict
Manually edited the file, removed conflict markers, and set a final message:

javascript
Copy code
function getMessage() {
    return "Final merged message after conflict resolution!";
}
Then:

sql
Copy code
git add script.js
git commit -m "Resolved merge conflict"
git push
✔️ Final Outcome
Both branches were successfully merged

Conflict was resolved manually

All commits and branches are visible on GitHub

The final code runs correctly in the browser

🎓 Learning Summary
Through this exercise, I learned:

How merge conflicts occur when two branches modify the same line

How to read and resolve Git conflict markers

How to use git status, git diff, and proper commit workflow

The importance of clear branch management in DevOps practices

This assignment provided hands-on experience with distributed version control using Git and GitHub.