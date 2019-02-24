# Daftar Perintah Git #

1. Membuat repository baru

    git init nama-folder

2. Melihat status working folder

    git status

3. Menambahkan perubahan ke staging area


4. Menyimpan perubahan ke repository

    git add.
    git commit -m "pesan/ keterangan commit"

5. Melihat history perubahan

    git log
    git log --oneline

6. Melihat perbedaan (difference) antar versi

    git diff commitId1 commitId2

7. Membatakan perubahan staging dan working

    git reset

8. Membatalkan perubahan di staging dan working (!!Bahaya!!)

    git reset --hard

9. Mendaftarkan remote repository

    git remote add origin git@github.com:ustadho/belajar-git.git

10. Mengambil repo dari remote

    git clone git@github.com:ustadho/belajar-git.git

11. Mengupload repo lokal ke remote

    git push -u namaremte namabranch
    git push -u origin master

