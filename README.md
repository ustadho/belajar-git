# Belajar Git

Jika sebelumnya belum disetting username dan user, 
maka kita diminta untuk setting username dan email terlebih dulu. 
Sedangkan jika sebelumnya sudah disetting, maka informasi username dan email disimpan di home folder dengan nama ~/.gitconfig
```
[user]
	email = cak.ust@gmail.com
	name = ustadho
```

git init
git add .
git commit -m "message ...."

Sebelum kita simpan kita review dulu perubahannya dengan perintah 
```
git diff
```

untuk melihat perubahan yang sudah pernah dibuat dengan satu baris
```
git log --oneline
```

melihat perbedaan antar versi

```
git diff 9c2e9d7570fa22c75cbc81cab3630a1c95829a60 f36d65cf43a9640e0b5c447bce1be79e0b8ee9c9
```

Belum tentu semua akan dicommit,
misalkan kita lagi ngerjakan satu file, kita tambahkan fungsi/method, ternyata ada info kalau di production ada bug berarti ada 2 perubahan, 
1. tambahan fungsi baru
2. bug fix
maka kita menggunakan staging, yang 1 masuk staging yang 2 kita commit

Untuk membatalkan staging supaya sama dengan yang ada di working folder, maka kita harus **reset**

git reset

maka sekarang posisinya semua perubahan belum staging

Pilih baris per baris yang akan ditambahkan

```
git add -p
```

Stage this hunk [y,n,q,a,d,e,?]? 
tekan Enter untuk menampilkan keterangan

Apakah potingan ini mau dimasukkan ke staging?

y - stage this hunk (semua yang tampil disini akan masuk)
n - do not stage this hunk (enggak usah)
q - quit; do not stage this hunk or any of the remaining ones
a - stage this hunk and all later hunks in the file
d - do not stage this hunk or any of the later hunks in the file
e - manually edit the current hunk
? - print help

biasanya yang digunakan 's' (split), potongannya baris per baris

untuk melihat apa saja yang di staging
```
git diff --staged
```

apa saya yang tidak masuk staging
```
git diff
```

Hati hati menggunakan git reset --hard karena bisa berpotensi menghilangkan semua perubahan terakhir

add <> reset

## GitIgnore

## Remote Repository

tambahkan ssh key dari folder ~/ssh
buka id_rsa.pub

## Branch 

Istilah: 
HEAD: ujung dari branch commit terakhir

head dengan huruf besar artinya aktif, yang kita sedang ada didalamnya
Branch: HEAD yang dikasih nama misal (1.x)

$ git status

akan menampilkan sedang di branch mana kita saat ini
untuk melihat ada branch apa saja di repository ini

$ git branch

saat ini hanya ada satu branch, sebetulnya ada satu branch lagi yaitu remote branch (untuk mapping dengan kondisi di remote)

untuk menampilkan semua branch (termasuk yang di remote)

$ git branch -a

Kenapa ada 2? karena kalau kita kerja sedangkan ada orang lain yang sudah push. Kita mau mendownload yang diremote, 
tapi kita belum tentu mau pasang (merge) di lokal kita.

solusinya kita pakai command fetch

Teknisnya:

$ git branch perbaikan-format-angka
$ git branch


git log --oneline --all --decorate --graph
