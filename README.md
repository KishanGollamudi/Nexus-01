# ⚙️ Java Web Calculator CI/CD Pipeline (Maven + Nexus + Tomcat)

This project demonstrates a **3-tier CI/CD setup** for a Java-based web calculator application using:
- **Maven (Build Server)** for building and packaging the app  
- **Nexus Repository (Repo Server)** for hosting artifacts  
- **Apache Tomcat (Deploy Server)** for deployment

---

## 🏗️ 1️⃣ Build Server Setup — Maven + OpenJDK

**Server Hostname:** `Build`  
**Purpose:** Compile and deploy the Java web app to Nexus Repository.
1. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/5e4eb1ac-7220-4173-8010-6e6ca1f3f0e6" />

### 🔧 Commands Executed
```bash
sudo hostnamectl set-hostname Build
sudo apt update -y
java --version
```
4. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/10d26972-8103-4689-ae99-4febb646349e" />
5. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/531d7c66-4e34-4ac8-9d0f-3bc22e377476" />
6. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/adc0a814-8954-4eff-acca-da64063e39fe" />
7. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/5e6abfd0-437c-4452-aca4-796036dadbdc" />
8. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/f02d5c40-f301-4cb4-97df-6cc8b8a8de62" />
```bash
sudo apt install openjdk-17-jre-headless -y
sudo apt install maven -y
sudo init 6
git clone https://github.com/mrtechreddy/Java-Web-Calculator-App.git
```
9. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/fbc4b5ba-edeb-4b7f-9a9a-0c4cff7bb10d" />
10. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/11791670-c660-4b13-bce5-12fa09f0c0f9" />
11. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/6b6fdf7c-ac9c-482e-a5e2-91c9ede36dba" />
12. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/b0d3bc90-d50b-4d8b-b675-61bccc3b820d" />
```bash
cd Java-Web-Calculator-App/
ls
sudo apt install tree
tree
```

```bash
cs src/main/webapp/
cd src/main/webapp/
cp index.jsp /tmp/
```
```bash
cd Java-Web-Calculator-App/
>pom.xml
sudo vi pom.xml
tree
cd src/main/webapp/
```
```bash
sudo vi index.jsp
mvn package
cd target/
```
```bash
cd Java-Web-Calculator-App/
ls
sudo vi pom.xml
cd
cd /etc/maven/
ls
sudo vi settings.xml
cd
cd Java-Web-Calculator-App/
ls
mvn clean
ls
mvn package
mvn deploy
mvn clean
ls
cd src/main/webapp/
ls
cp /tmp/index.jsp /Java-Web-Calculator-App/src/main/webapp/
cp /tmp/index.jsp .
ls
sudo vi index.jsp
cd ../../..
ls
sudo vi pom.xml
ls
mvn package
ls
cd target/
ls
cd ..
mvn deploy
ls
mvn clean
ls
sudo vi pom.xml
cd src/main/webapp/
ls
cp /tmp/index.jsp .
sudo vi index.jsp
cd ../..
cd ..
ls
mvn package
mvn deploy
ls
cd target/
ls
ls
cd Java-Web-Calculator-App/
ls
history
```

---

## 📦 2️⃣ Nexus Repository Setup — Artifact Management

**Server Hostname:** `Nexus-Repo`  
**Purpose:** Store and manage versioned artifacts (WAR files) pushed from the build server.

### 🔧 Commands Executed
```bash
sudo hostnamectl set-hostname Nexus-Repo
sudo apt update -y
wget https://download.sonatype.com/nexus/3/nexus-3.85.0-03-linux-x86_64.tar.gz
sudo init 6
ls
tar -xvzf nexus-3.85.0-03-linux-x86_64.tar.gz
ls
cd nexus-3.85.0-03/
ls
cd bin/
ls
./nexus start
./nexus status
cd ../..
ls
sudo apt install -y net-tools
sudo netstat
sudo netstat -tulnp | grep 8081
ls
cd sonatype-work/
ls
cd nexus3/
ls
cd log/
ls
tail -n10 nexus.log
cd
sudo cat sonatype-work/nexus3/admin.password
ls
cd nexus-3.85.0-03/
ls
cd bin/
ls
./nexus
./nexus start
cd
history
```

**📍 Access URL:**  
`http://<NEXUS_PUBLIC_IP>:8081`

---

## 🚀 3️⃣ Deploy Server Setup — Apache Tomcat 9

**Server Hostname:** `Deploy`  
**Purpose:** Deploy and serve WAR files fetched from Nexus Repository.

### 🔧 Commands Executed
```bash
sudo hostnamectl set-hostname Deploy
sudo apt update -y
wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.111/bin/apache-tomcat-9.0.111.tar.gz
ls
tar -xvzf apache-tomcat-9.0.111.tar.gz
sudo init 6
ls
cd apache-tomcat-9.0.111/
ls
cd webapps/
ls
wget http://admin:admin123@3.90.104.89:8081/repository/java-cal-app/com/web/cal/webapp-add/0.1/webapp-add-0.1.war
wget http://admin:admin123@3.90.104.89:8081/repository/java-cal-app/com/web/cal/webapp-add-sub/0.2/webapp-add-sub-0.2.war
wget http://admin:admin123@3.90.104.89:8081/repository/java-cal-app/com/web/cal/webapp-add-sub-mul/0.3/webapp-add-sub-mul-0.3.war
ls
cd ..
cd bin/
./startup.sh
cd
java --version
sudo apt install openjdk-17-jre-headless -y
ls
cd apache-tomcat-9.0.111/
ls
cd bin/
./startup.sh
sudo find -name context.xml
cd ..
sudo find -name context.xml
sudo vi ./webapps/manager/META-INF/context.xml
sudo vi ./webapps/host-manager/META-INF/context.xml
sudo find -name tomcat-users.xml
sudo vi ./conf/tomcat-users.xml
history
```

**📍 Access URLs:**
- **Tomcat Manager:** `http://<DEPLOY_PUBLIC_IP>:8080/manager/html`
- **Deployed App:** `http://<DEPLOY_PUBLIC_IP>:8080/webapp-add`

---

## 🧩 CI/CD Pipeline Overview

```text
[ Build Server ]
   |-- Maven compiles source
   |-- Generates WAR file
   |-- Deploys to Nexus Repo
         ↓
[ Nexus Repository ]
   |-- Hosts versioned artifacts
         ↓
[ Deploy Server ]
   |-- Fetches WAR files from Nexus
   |-- Deploys to Apache Tomcat
```

---

## ✅ Results

- ✔️ Nexus 3 configured and running on port 8081  
- ✔️ Maven builds and uploads WAR artifacts successfully  
- ✔️ Tomcat deploys WARs automatically from Nexus  
- ✔️ End-to-end CI/CD pipeline functional across 3 servers  

---

## 🧠 Tech Stack

| Component | Tool / Version |
|------------|----------------|
| Language | Java 17 |
| Build Tool | Apache Maven |
| Artifact Repository | Sonatype Nexus 3.85.0-03 |
| Application Server | Apache Tomcat 9.0.111 |
| OS | Ubuntu 22.04 LTS |

---
Snapshot:
