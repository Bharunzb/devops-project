echo "#Devops Sample Project"
# 🚀 DevOps Project – Task 4  
**Build a Version-Controlled DevOps Project with Git**  

---

## 📌 Objective  
To manage a DevOps project using **Git best practices**: branching, pull requests, tagging, and documentation.  

---

## 🔧 Tools Used  
- Git  
- GitHub  
- AWS EC2   

---

## 🛠️ Step-by-Step Process  

### 1️⃣ Launch Instance  
- Go to **AWS EC2 → Launch Instance**.  
- Choose ** Amazon Linux **.  
- Select **t3.micro** (Free tier).  
- Allow SSH (22) in security group.  
- Connect to instance:  
<img width="1633" height="266" alt="Screenshot 2025-09-26 152748" src="https://github.com/user-attachments/assets/954c611e-d84a-458b-862f-da7fe2e92ea7" />

yum install git -y
git --version or git -v
git init
<img width="822" height="323" alt="Screenshot 2025-09-26 153304" src="https://github.com/user-attachments/assets/2cd86b1d-6bc9-48fd-8682-c070fd4f6ed5" />


git config  user.name "Your Name"
git config  user.email "your@email.com"
<img width="452" height="149" alt="Screenshot 2025-09-26 153900" src="https://github.com/user-attachments/assets/354296dd-f6b9-4202-90ca-d71c4ca7392b" />


mkdir devops-project && cd devops-project
echo "# DevOps Sample Project" > README.md
echo "node_modules/" > .gitignore
mkdir app
echo 'print("Hello from DevOps Project")' > app/main.py
git init
git add .
git commit -m "Initial commit - project setup"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
<img width="1919" height="1079" alt="Screenshot 2025-09-26 135602" src="https://github.com/user-attachments/assets/43dc74e9-5a34-44e4-b139-45df9bca54d7" />


# Development branch
git checkout -b dev
git push -u origin dev
<img width="750" height="315" alt="Screenshot 2025-09-26 141809" src="https://github.com/user-attachments/assets/2836f34e-4611-4594-8a20-33eaec67eca4" />


# Feature branch
git checkout -b feature-hello
echo 'print("Hello World Feature")' >> app/main.py
git add .
git commit -m "feat: added hello world feature"
<img width="973" height="539" alt="Screenshot 2025-09-26 144529" src="https://github.com/user-attachments/assets/c6fbed84-329a-4a38-afbc-96846c7ee46a" />


git push -u origin feature-hello
<img width="1104" height="444" alt="Screenshot 2025-09-26 144803" src="https://github.com/user-attachments/assets/5ed3dffa-66ca-421c-8f7e-a852b05288d3" />

### Create Pull Requests
On GitHub → Click Compare & Pull Request.
Merge feature-hello → dev.
<img width="1919" height="950" alt="Screenshot 2025-09-26 150323" src="https://github.com/user-attachments/assets/67e4b2a7-f865-4a35-984d-3df1c6eb8e4e" />


Later merge dev → main.
<img width="1908" height="926" alt="Screenshot 2025-09-26 151738" src="https://github.com/user-attachments/assets/44c7f995-1561-4bc4-8319-d42d070e021c" />


git checkout main
git pull origin main
git tag -a v1.0 -m "First stable release"
git push origin v1.0
<img width="713" height="317" alt="Screenshot 2025-09-26 152109" src="https://github.com/user-attachments/assets/1ab19090-2807-48d5-ab0a-53f26bd7fd0d" />


