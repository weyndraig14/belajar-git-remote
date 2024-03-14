GIT REMOTE 

1. POIN UTAMA :

   A. Apa itu GIT REMOTE?

       Git remote memungkinkan kolaborasi dan berbagi repositori Git di antara anggota tim.
       Git adalah sistem kontrol versi terdistribusi, yang memungkinkan pengguna untuk bekerja di repositori lokal tanpa koneksi konstan ke server pusat.
       Server Git menyimpan repositori dan mendukung berbagai mekanisme komunikasi, termasuk HTTP/HTTPS dan SSH.
       SSH (Secure Shell) direkomendasikan untuk komunikasi dengan server Git karena manfaat keamanannya.
       Pengguna perlu membuat kunci SSH untuk autentikasi, yang terdiri dari private key (disimpan secara lokal) dan public key (dibagikan dengan server Git).
       Menambahkan kunci publik SSH ke pengaturan server Git memungkinkan autentikasi yang mulus tanpa memasukkan kata sandi.
       Menguji koneksi SSH ke server Git dapat dilakukan dengan menggunakan perintah SSH yang diikuti dengan URL server.
       Autentikasi yang berhasil di Git berarti pengguna telah diautentikasi.

   B. GIT REMOTE

       1. Menambahkan Remote repository di Git melibatkan penentuan URL-nya menggunakan perintah "git remote add", yang biasanya dinamai "Origin."
    
       2. Remote repository dapat dilihat menggunakan "git remote" untuk menampilkan listnya.
    
       3. Git memerlukan push manual untuk perubahan ke remote repository, perintah "git push" mengirimkan perubahan ke remote repository.
    
       4. Untuk mendorong semua branch ke remote repository, gunakan "git push origin --all".
    
       5. Branch dapat dihapus dari remote repository menggunakan "git push --delete".
    
       6. Mengkloning project dari remote repository ke komputer lain dilakukan dengan menggunakan "git clone". Ini secara otomatis membuat salinan repository.
    
       7. Ketika mengkloning repository, nama remotenya adalah "Origin," dan secara otomatis mengambil konten branch utama. branch lain tidak diunduh secara otomatis.
    
       8. Ketika mengkloning repository, branch utama diambil secara default. Untuk melihat semua remote branch, gunakan "git branch -r".
    
       9. Untuk melihat semua branch, termasuk branch utama dan remote, gunakan "git branch -a".
    
       10. Untuk membuat branch dari remote branch, gunakan "git checkout -b [branch_name] [remote_name/remote_branch_name]".

       11. Untuk membandingkan branch antara repository local dan remote, gunakan "git diff [local_branch] [remote_name/remote_branch_name]".
    
       12. "git fetch" mengambil perubahan dari remote repository tanpa menggabungkannya ke local repository.
    
       13. "git pull" mengambil perubahan dari remote repository dan menggabungkannya ke dalam branch saat ini di local repository.
    
       14. Tag yang dibuat secara lokal tidak secara otomatis dipush ke remote repository. Gunakan "git push --tag" untuk mengunduh tag ke remote repository.
    
       15. Git memungkinkan pembuatan tag untuk menandai titik-titik tertentu dalam project history, sehingga membantu dalam kontrol versi dan manajemen rilis. Tag dapat didorong ke remote repository menggunakan perintah "git push <remote_name> <tag_name>".
    
       16. Untuk mengunduh semua tag sekaligus ke remote repository, gunakan "git push <remote_name> --tags".
    
       17. Menghapus tag secara lokal tidak secara otomatis menghapusnya dari remote repository kamu harus secara manual menghapusnya menggunakan "git push --delete <remote_name> <tag_name>".
    
       18. Menarik perubahan dari remote repository termasuk tag dapat dilakukan dengan menggunakan "git fetch <remote_name>".
    
       19. Menarik semua perubahan termasuk tag dari remote repository dapat dilakukan dengan menggunakan "git fetch <remote_name> --tags".

   C. PULL

       1. Pull request (PR) memungkinkan kolaborasi dan peninjauan perubahan kode sebelum menggabungkannya ke dalam branch utama.
          Pull request dapat dibuat dan dikelola menggunakan platform seperti GitHub, yang memfasilitasi peninjauan dan kolaborasi kode.
          Pull request dapat digabungkan setelah ditinjau dan disetujui, mengintegrasikan perubahan ke dalam cabang utama.
    
       2. Conflict dapat muncul dalam pull request ketika perubahan bertentangan dengan kode yang ada di target branch.
          Menyelesaikan konflik membutuhkan intervensi manual untuk merekonsiliasi perbedaan sebelum menggabungkan pull request.
          Conflict dapat muncul ketika membuat pull request, biasanya karena perubahan pada basis kode.

   D. SUBMODULE

       1. Submodule berguna untuk menyertakan repository eksternal di dalam sebuah project, sehingga memungkinkan pengelolaan kode eksternal secara terpisah saat mengaksesnya di dalam project utama.
          Submodule memfasilitasi pembagian kode di antara beberapa project, memastikan konsistensi dan kemudahan pembaruan di seluruh project.
          Menambahkan submodule melibatkan penentuan URL submodule dan folder tempat penyimpanannya di dalam project.
          Submodule secara otomatis dikloning ke dalam folder yang ditentukan dan ditautkan ke repositori masing-masing.

       2. Untuk menambah submodule kita bisa menggunakan perintah "git submodule add urlgitrepo namafolder"
    
       3. Untuk memperbarui submodule, gunakan perintah "git submodule update --remote".
    
       4. Setelah memperbarui, perubahan pada submodule dapat dilihat menggunakan status git.
    
       5. Untuk menginisialisasi submodule setelah mengkloning repository, gunakan "git submodule init".
    
       6. Untuk mengunduh atau memperbarui submodule, gunakan "git submodule update".
    
       7. Menghapus submodule melibatkan penghapusan folder submodule dan memperbarui file .gitmodules.

   E. Forking Workflow

       1. Forking Workflow adalah hal yang umum dalam project open source, di mana kontributor menduplikasi repositori utama, membuat perubahan dalam fork mereka, dan kemudian meminta perubahan tersebut untuk digabungkan ke dalam proyek utama.
    
       2. Forking Workflow memungkinkan kolaborasi sambil mempertahankan kontrol atas repositori utama dan memastikan perubahan ditinjau sebelum integrasi.


2. KESIMPULAN

       Dengan adanya git remote, seseorang dapat membuat dan mengelola git repository baik secara lokal maupun remote.
   
   
