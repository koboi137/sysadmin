# Security guide for sysadmin

Hal hal penting yang harus di perhatikan dalam mengelola server ( Masih acak )

1. Selalu update system operasi yang sedang di gunakan
2. Sembunyikan versi PHP, apache, dll di header
3. Non aktifkan fungsi execute command seperti exec, passthru, php-cgi kalo tidak di perlukan
4. Blok trafic masuk ICMP
5. Nonaktifkan DNS di /etc/resolv.conf
6. Batasi koneksi outgoing menggunakan iptables
7. Segala hal yang berhubungan dengan password harus di bedakan
8. Selalu cek log aktivitas server (monitoring)
9. Blok IP yang di sinyalir membahayakan server dengan iptables
10. Batasi jumlah trafik masuk pada server. Misal 2MB koneksi yang di izinkan masuk ke server
11. Non aktifkan directory listing di webserver
12. Ganti port default ssh menjadi port random
13. Gunakan private key yang di password untuk login ke ssh
14. Jangan izinkan user root masuk ke dalam ssh atau gunakan user biasa untuk login ke ssh
15. Batasi pengecekan password yang salah dengan fail2ban
16. Jangan buka port database ke publik
17. Tutup port yang tidak di perlukan
18. Gunakan ssl di dalam webserver
19. Usahakan password yang di gunakan tidak mudah di tebak
20. Jangan simpan private key di dalam server
21. Batasi ukuran file yang di upload
22. Jangan simpan file backup di dokumen publik webserver
23. Rubah alamat phpmyadmin jadi alamat acak
24. Rubah alamat login admin jadi alamat acak
25. Pasang alamat admin palsu (honeypot)
26. Disable shell pada user web server "www-data" di /etc/passwd
27. Cek cronjob atau crontab setiap waktu
28. Cek setiap service yang berjalan agar tidak terjadi misconfigurasi
29. Hanya izinkan port yang terbuka saja yang bisa di akses publik menggunakan ufw/iptables
30. Enkripsi setiap script config database yang di gunakan di server atau pindahkan ke folder yang tidak biasanya
31. Di history command jangan tertinggal password apapun
