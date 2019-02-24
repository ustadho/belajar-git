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

