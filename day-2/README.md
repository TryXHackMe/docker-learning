# 🐳 Day 2: Dockerfile
**Tujuan Hari Ini:**
- Membuat custom image
- Menginstall custom image dan menjalankannya 
---
**Spesifikasi Lingkungan:**
- OS : Linux Ubuntu 24.04
- Docker : 28.3.2
- User Privileges : Root Access
---
**Perintah yang digunakan:**
```bash
# membuat image baru dengan nama static-web
docker build -t static-web .
```
```bash
# menjalankan image static-web yang telah dibuat
docker run -d -p 9080:80 static-web
```
```bash
# memberhentikan container 
docker stop [container-id]
```
---
**Dockerfile**
```dockerfile
# Pakai base nginx:alpine
FROM nginx:alpine

# copy file dari host ke dalam container
COPY ./html /usr/share/nginx/html

# jalankan di port 80 container
EXPOSE 80

# jalankan nginx default setting
CMD ["nginx", "-g", "daemon off;"]
```
---
**Hasil Output**
![Hello-World](https://raw.githubusercontent.com/TryXHackMe/docker-learning/refs/heads/main/day-2/Screenshot_2025-07-18_09-45-35.png)

Status : Selsai
