# Tahap 1: Gunakan image Nginx versi alpine yang sangat ringan
FROM nginx:alpine

# Tahap 2: Hapus file default Nginx yang tidak diperlukan
RUN rm -rf /usr/share/nginx/html/*

# Tahap 3: Salin seluruh isi folder proyek ke folder publik Nginx
# Ini akan menyalin index.html, style.css, script.js, dan folder asset/img
COPY . /usr/share/nginx/html

# Tahap 4: Ekspos port 80 agar bisa diakses oleh Dokploy
EXPOSE 80

# Jalankan Nginx secara otomatis
CMD ["nginx", "-g", "daemon off;"]