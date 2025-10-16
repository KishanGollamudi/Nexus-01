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
13. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/e55b61e4-df5c-4baf-81d4-00ce6fbad487" />
14. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/dc61cd43-c9a1-405a-90ab-258978d4cb0c" />
15. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/bc0a71bb-aae1-47ce-a2f7-4cc6928db39b" />
16. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/2d136761-a3f1-41b9-9fb0-c2eededc3a7b" />

```bash
cs src/main/webapp/
cd src/main/webapp/
cp index.jsp /tmp/
```
17. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/48387953-b530-46e7-92a6-5f8233fa41c4" />
18. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/c8f74afb-ee28-406f-947f-4849aa4cb4f2" />
19. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/79bfd8f4-f582-44ce-9588-65b3428ee4b9" />
20. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/0d02a1e5-87b6-463b-bf7c-17424ae54754" />

```bash
cd Java-Web-Calculator-App/
>pom.xml
sudo vi pom.xml
tree
cd src/main/webapp/
```
21. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/f089f7cb-2d63-4d23-b7ef-865facc16d30" />
22. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/7a45f525-5425-4eab-8b9a-b0f704199b83" />
23. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/46bce731-f6d1-4d61-b0dd-7581a9b12cd5" />
24. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/91e2d469-d3bc-4136-820c-209c9f1a2cb1" />

```bash
sudo vi index.jsp
mvn package
cd target/
```
25. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/78502d37-866d-40f6-b5cc-a5163340ef56" />
26. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/3910f556-26ae-4f0d-a288-7260dc2539bc" />
27. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/c4ec9ec8-b4a2-4730-b7f0-d654a95243bb" />
28. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/d0df5c6c-152b-452d-8261-63f85b229ac9" />

```bash
cd Java-Web-Calculator-App/
ls
sudo vi pom.xml
cd /etc/maven/
sudo vi settings.xml
```
29. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/4844bebe-3fd6-445c-9ab4-587973f1c677" />
30. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/8de7093f-fb37-4521-91e6-c67cf1d2af77" />
31. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/5cc69fa8-4158-4b03-89a3-a74adbfa394f" />
32. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/c019f95a-93fc-41cd-bcd1-c20c22b5287c" />

```bash
cd Java-Web-Calculator-App/
mvn clean
mvn package
mvn deploy
mvn clean
```
33. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/8d9df744-f989-4baa-b4a3-d2c18c33a357" />
34. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/8219dac4-ce8b-48a5-a788-12eba8e2493c" />
35. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/f6954123-7709-4573-a501-a9f3a2dae254" />
36. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/cad9a408-bec2-4031-ae2c-3bb561dbb0f3" />

```bash
cd src/main/webapp/
cp /tmp/index.jsp /Java-Web-Calculator-App/src/main/webapp/
cp /tmp/index.jsp .
sudo vi index.jsp
```
37. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/12295e1e-4432-440e-a206-23debdd7fd19" />
38. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/aa9ced9a-aa9d-4d7f-a2f0-1f7d65eb5ef0" />
39. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/eaa3a33f-b5bd-4103-935e-e5b293ff8194" />
40. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/e761fbcd-7552-4e68-b896-34f28da8272e" />

```bash
sudo vi pom.xml
mvn package
cd target/
```
41. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/10553d9f-4fd3-4754-94ea-161b07fa5cbc" />
42. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/ed76f39f-44c7-4c82-8eae-f09024d21660" />
43. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/ac379b2e-632c-47f6-8205-98a7310b22db" />
44. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/57441b07-1d50-4288-a2bd-87c1e80e9b0f" />

```bash
mvn deploy
mvn clean
sudo vi pom.xml
cd src/main/webapp/
```
45. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/d23b06f3-4f96-4275-8759-f721a2b84a7c" />
46. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/1d7b4353-8707-4b05-9536-3d06b9826e84" />
47. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/1a2485c5-b64f-4601-be74-2dc7a9ba38a2" />
48. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/0693f66a-b615-4655-bff0-045c7b63f9a2" />

```bash
cp /tmp/index.jsp .
sudo vi index.jsp
mvn package
mvn deploy
```
49. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/8ab88613-3baf-4414-a565-6c7189f07c8d" />
50. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/1142fc9c-79a2-47d3-8223-9d7defccadfb" />
51. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/a653adb5-cb66-4144-8409-f2a6fd38cbae" />
52. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/a0d6ee09-edbe-461a-9069-d023cfdad611" />

```bash
cd target/
cd Java-Web-Calculator-App/
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
```
53. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/699c0113-10a4-442b-ac3f-69d21f68d6b5" />
54. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/569b9775-0795-4af9-bec8-e853f07947a3" />
55. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/a8dc3814-1179-41ee-ac72-2bf5a22d39dd" />
56. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/36c12d1a-74eb-4413-ad6a-9718ef94436c" />
```bash
tar -xvzf nexus-3.85.0-03-linux-x86_64.tar.gz
cd nexus-3.85.0-03/
cd bin/
./nexus start
./nexus status
```

```bash
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
57. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/7ab18383-ff1e-4ddd-b672-1c4c17066859" />
58. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/16361cda-01b2-46bc-849a-d5a891f6a3e2" />
59. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/f2dcfc41-1463-4348-83d2-c7b53f173542" />

**📍 Access URL:**  
`http://<NEXUS_PUBLIC_IP>:8081`

60. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/89a84f90-c972-48da-83c5-9f5012b2f5a1" />
61. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/09d09364-7e04-4db2-a6bd-27a2c8c2925d" />
62. <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/526b87e5-bfe0-4d5b-bad1-f99c63eadf4c" />
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
