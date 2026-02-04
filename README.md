# 🧰 **Jenkins Introduction**

## 🚀 Overview

**Jenkins** is an open-source automation server written in Java ☕.
It helps automate parts of the software development process like **building**, **testing**, and **deploying** — making it an essential tool for **DevOps** and **Continuous Integration/Continuous Deployment (CI/CD)**.

With Jenkins, you can:

* 🏗️ Automatically build and test your code whenever you push changes 
* 🔁 Integrate tools like Git, Docker, AWS, and Kubernetes
* 🚀 Deploy applications to different environments with ease
* 👷‍♂️ Create automated pipelines for end-to-end workflows

---

## ⚙️ **Key Features**

| 🌟 Feature              | 🧩 Description                                     |
| ----------------------- | -------------------------------------------------- |
| 🧱 **CI/CD Automation** | Automate build, test, and deployment processes     |
| 🔌 **Plugin Ecosystem** | 1,800+ plugins for integration with popular tools  |
| 🧠 **Pipeline as Code** | Define automation logic in a `Jenkinsfile`         |
| 📊 **Extensibility**    | Works with Docker, Kubernetes, GitHub, Maven, etc. |
| 💬 **Notifications**    | Integrate with Slack, Teams, or email for alerts   |
| 🏗️ **Scalability**     | Distributed builds using Jenkins agents/slaves     |

---

## 🐳 **Running Jenkins Using Docker**

Jenkins requires **Java** to run — but the official **Docker image** already includes it!
So you can skip the manual Java installation 👌

### 🪜 **Steps to Install Jenkins via Docker**

```bash
# 1️⃣ Pull the official Jenkins LTS image
docker pull jenkins/jenkins:lts

# 2️⃣ Run Jenkins container
docker run -d -p 8080:8080 -p 50000:50000 --name jenkins jenkins/jenkins:lts

# 3️⃣ Get the admin password
docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword
```

Then open 👉 `http://localhost:8080`
Paste the admin password to unlock Jenkins 🔓
Install the suggested plugins → Create an admin user → Jenkins is ready 🎉

---

## 📘 **Hello Jenkins Pipeline Example**

Once Jenkins is running, you can create a simple **pipeline** to understand how it works.

### 🧩 **Jenkinsfile Example**

```groovy
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo '🏗️ Building the application...'
            }
        }
        stage('Test') {
            steps {
                echo '🧪 Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                echo '🚀 Deploying the application...'
            }
        }
    }
}
```

### 🖥️ **Run Steps**

1. Open Jenkins Dashboard → Click **New Item**
2. Choose **Pipeline**, name it (e.g., `hello-jenkins`)
3. Paste the above script into the **Pipeline Script** field
4. Click **Save** → **Build Now** ▶️

🧠 **Output Example:**

```
🏗️ Building the application...
🧪 Running tests...
🚀 Deploying the application...
✅ Pipeline completed successfully!
```

---

## 🌳 **Jenkins Workflow Overview**

```
🌳 Jenkins Pipeline
│
├── 🧩 Source Code (GitHub, GitLab, Bitbucket)
│
├── 🏗️ Build Stage
│   └── Compile / Package code
│
├── 🧪 Test Stage
│   └── Run automated tests
│
├── 🚀 Deploy Stage
│   └── Push to staging or production
│
└── 📊 Monitor & Notify
     └── Slack / Email alerts
```

---

## 🧠 **Real-World Use Cases**

| 🧱 Use Case                 | 💡 Example                                        |
| --------------------------- | ------------------------------------------------- |
| 🧪 Continuous Integration   | Automatically build & test code after each commit |
| 🚀 Continuous Deployment    | Deploy app to AWS after successful build          |
| 🐳 Docker Integration       | Build Docker images & push to Docker Hub          |
| ⚙️ Configuration Management | Automate Ansible or Terraform playbooks           |
| 🔗 GitHub Integration       | Trigger builds on pull requests or commits        |

---

## 🧰 **Common Jenkins Commands (Docker)**

| 🧩 Command               | 🔍 Description               |
| ------------------------ | ---------------------------- |
| `docker start jenkins`   | Start the Jenkins container  |
| `docker stop jenkins`    | Stop the Jenkins container   |
| `docker restart jenkins` | Restart Jenkins              |
| `docker ps -a`           | List all containers          |
| `docker logs -f jenkins` | View Jenkins logs            |
| `docker rm -f jenkins`   | Remove the Jenkins container |

---

## 🧱 **Architecture Overview**

```
+----------------------+
|      Developer       |
|   (Commits code)     |
+----------+-----------+
           |
           v
+----------------------+
|     Source Control   |
|   (GitHub / GitLab)  |
+----------+-----------+
           |
           v
+----------------------+
|       Jenkins        |
|  (Builds & Tests)    |
+----------+-----------+
           |
           v
+----------------------+
|    Deployment Env    |
| (AWS, Docker, K8s)   |
+----------------------+
```

---

## 🧩 **Advantages of Jenkins**

✅ Open-source and free
✅ Supports all major operating systems
✅ Highly customizable via plugins
✅ Huge active community
✅ Easy integration with CI/CD tools

---

## 💬 **Example Output: Hello Jenkins!**

After running your first pipeline:

```
[Pipeline] echo
👋 Hello Jenkins World!
[Pipeline] End of Pipeline
Finished: SUCCESS
```

---

## 🏁 **Summary**

| ✅ Task                        | 📘 Description                         |
| ----------------------------- | -------------------------------------- |
| 🧱 Install Jenkins via Docker | No manual Java setup needed            |
| 🔑 Unlock Jenkins             | Use initial admin password             |
| ⚙️ Configure Jenkins          | Install suggested plugins              |
| 🧩 Create Pipeline            | Use Jenkinsfile to define steps        |
| 🚀 Run Pipeline               | Automate build → test → deploy         |
| 👏 Celebrate!                 | Jenkins up and running successfully 🎉 |

---

## 🧭 **Next Steps**

Now that Jenkins is running, try:

* 🔗 Integrating **GitHub** for automated builds
* 🧪 Adding real test commands in pipelines
* 🐳 Using **Docker Agents**
* ☁️ Deploying to **AWS / Kubernetes**
* 📈 Monitoring pipelines via Slack notifications

---

## 🧑‍💻 **Maintainer**

👤 **Your Name**
📧 **[you@example.com](mailto:you@example.com)**
📍 **DevOps Engineer | Automation Enthusiast**

---
