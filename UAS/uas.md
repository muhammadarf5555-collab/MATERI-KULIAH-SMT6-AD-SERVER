# TechNime Blog & CV Statis - UAS Cloud Native & CI/CD
Aplikasi Web Multi-Kontainer dengan GitHub Actions CI/CD & AWS Deployment

---
* **Nama:** Muhammad Arif Rizky
* **NIM:** 2388010017
* **Mata Kuliah:** Administrasi Server
* **Instansi:** UIN Siber Syekh Nurjati Cirebon

1. membuat instance baru
![alt text](image.png)
2. membuat repositori baru di docker yaitu repo buat wb dininamis dan repositori buat web statis
![alt text](image-1.png)
![alt text](image-2.png)
3. membuat code php untuk web dinamis  
![alt text](image-4.png)

### 4. Install Docker 
    "sudo apt update"
    "sudo apt install -y ca-certificates curl gnupg"
    "sudo install -m 0755 -d /etc/apt/keyrings"
    "curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg"
    "sudo chmod a+r /etc/apt/keyrings/docker.gpg"
    ". /etc/os-release"
    "echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download docker.com/linux/ubuntu ${VERSION_CODENAME} stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/ null"
    "sudo apt update"
    "sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin"

    LALU CEK APAKAH DOCKER BERHASIL DIINSTALL
    "docker --version"
    "docker compose version"

![alt text](image-3.png)
 5.  LALU JALANKAN DOCKER COMPOSE
    "cd ~/uas"
    "docker compose config"
    "docker compose up -d --build"

    LALU CEK CONTAINER
    "docker compose ps"
![alt text](image-5.png)
7. Set Up Github Action
    ".github/workflows/deploy-static.yml"
    ".github/workflows/deploy-dynamic.yml"

    COMMIT & PUSH WORKFLOW
    "git status"
    "git add .github/workflows/deploy-static.yml .github/workflows/deploy-dynamic.yml"
    "git commit -m "Add GitHub Actions deployment workflows""
    "git push origin main"
![alt text](image-6.png)
8.  BUAT ACCESS TOKEN DOCKER HUB
    "Account Settings -> Personal access tokens -> Generate new token"
![alt text](image-7.png)
9.  DOCKERHUB_USERNAME=muharifrizky0225pohv
    DOCKERHUB_TOKEN=token_dockerhub_kamu
    EC2_HOST=47.128.217.195
    EC2_USER=ubuntu
    EC2_SSH_KEY=isi_private_key_pem
    DB_NAME=uas_2388010017
    DB_USER=uas_user
    DB_PASSWORD=arif1234567891123
![alt text](image-8.png)
 10. Live Test Zero Touch
![alt text](image-6.png)
11. mengekill web yang sedang jalan agar tidak eror
![alt text](image-9.png)
12. web statis
![alt text](image-10.png)
13. tampilan web dinamis halaman home
![alt text](image-11.png)
14. tampilan halaman admin
![alt text](image-12.png)
![alt text](image-13.png)
![alt text](image-14.png)
