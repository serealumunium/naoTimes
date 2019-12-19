# Showtimes

Ini merupakan module utama yang membantu tracking garapan Fansub.<br>
Untuk menyiapkannya, tolong liat bagian [Invite Bot](README#invite-bot)<br>
Jika sudah, mari kita mulai melihat list perintahnya

## Perintah Utama

Perintah utama dibagi menjadi 3 tier, yaitu pengujung/user, staff, dan admin.
* [Perintah User](#perintah-utama-user)
* [Perintah Staff](#perintah-utama-staff)
* [Perintah Admin](#perintah-utama-admin)
* [Dalam .gif](showtimes_cmd#dalam-gif)

#### Perintah Utama: User

| Nama Command | Penjelasan |  Contoh  | Alias |
|:------------:|:----------:|:--------:|:-----:|
| !tagih **[judul]** | Menagih garapan suatu fansub yang terdaftar di database.<br><br>**[judul]**: Judul garapan yang terdaftar, bisa disingkat sesingkat mungkin | !tagih kyuuketsuki | !blame<br>!mana |
| !jadwal | Melihat jadwal tayang anime musiman yang di ambil. | !jadwal | !airing |
| !staff **[judul]** | Melihat ~~tukang delay~~ staff yang mengerjakan suatu garapan.<br><br>**[judul]**: Judul garapan yang terdaftar, bisa disingkat sesingkat mungkin | !staff kyuuketsuki |! tukangdelay<br>!pendelay |

#### Perintah Utama: Staff

| Nama Command | Penjelasan |  Contoh  | Alias |
|:------------:|:----------:|:--------:|:-----:|
| !beres **[posisi]** **[judul]** | Menandakan posisi garapan episode yang telah dikerjakan.<br><br>**[posisi]**: tl, tlc, enc, ed, tm, ts, atau qc <br>(Translator, Translation Checker, Encoder, Editor, Timer, Typesetter, Quality Checker)<br><br>**[judul]**: Judul garapan yang terdaftar, bisa disingkat sesingkat mungkin | !beres enc hitoribocchi | !done |
| !gakjadi **[posisi]** **[judul]** | Menandakan posisi garapan episode yang telah dikerjakan tetapi ada kesalahan dan ingin diulang.<br><br>**[posisi]**: tl, tlc, enc, ed, tm, ts, atau qc <br>(Translator, Translation Checker, Encoder, Editor, Timer, Typesetter, Quality Checker)<br><br>**[judul]**: Judul garapan yang terdaftar, bisa disingkat sesingkat mungkin | !gakjadi enc hitoribocchi | !undone<br>!cancel |
| !tandakan **[posisi]** **[episode]** **[judul]** | Mengubah status posisi untuk episode tertentu dari belum ke sudah atau sebaliknya.<br><br>**[posisi]**: tl, tlc, enc, ed, tm, ts, atau qc <br>(Translator, Translation Checker, Encoder, Editor, Timer, Typesetter, Quality Checker)<br><br>**[episode]**: Episode yang ingin diubah tandanya<br><br>**[judul]**: Judul garapan yang terdaftar, bisa disingkat sesingkat mungkin<br><br>Note: Akan otomatis terubah dari ``beres`` ke ``belum beres`` atau sebaliknya jika perintah ini dipakai<br>perintah ini tidak akan mengannounce perubahan ke channel publik | !tandakan enc 3 hitoribocchi | !mark |
| !rilis <...> | Merilis garapan!<br>***Hanya bisa dipakai oleh Admin atau tukang QC***<br>Penjelasan ada di bawah ini. | !rilis kyuuketsuki<br><br>!rilis batch 3 kyuuketsuki<br><br>!rilis semua kyuuketsuki | !release |

**!rilis \<judul>**<br>
Merilis episode dari judul yang dikerjakan<br>
<br>
**!rilis batch \<jumlah> \<judul>**<br>
Merilis jumlah episode tertentu dari judul yang dikerjakan<br>
<br>
**!rilis semua \<judul>**<br>
Merilis semua episode dari judul yang dikerjakan

<p class="notice">
<strong>Note:</strong> Untuk perintah !rilis batch, terdapat <strong>[jumlah]</strong> episode yang mau dirilis.
Penghitungannya adalah <strong>Episode terakhir yang sedang dikerjakan ditambah jumlah</strong>.<br>
Misalkan lagi <strong>ngerjain Episode 4</strong>, terus mau <strong>rilis sampai episode 7</strong><br>
Total dari <strong>Episode 4 sampai 7 ada 4</strong> (4, 5, 6, dan 7)<br>
Maka tulis <strong>jumlahnya 4</strong>
</p>

#### Perintah Utama: Admin

| Nama Command | Penjelasan |  Contoh  | Alias |
|:------------:|:----------:|:--------:|:-----:|
| !tambahutang | Menambah garapan baru ke database.<br>Anda akan dibantu melewati proses penambahan utang<br>silakan melihat [.gif ini](https://p.ihateani.me/ifQMCsOt.gif) jika kurang mengerti | !tambahutang | !add<br>!tambah |
| !ubahdata **[judul]** | Mengubah informasi data suatu garapan.<br>Penjelasan lebih lengkap ada di bawah ini.<br><br>**[judul]**: Judul garapan yang terdaftar, bisa disingkat sesingkat mungkin | !ubahdata kyuuketsuki | - |

**!ubahdata** memiliki 5 mode interaktif, yaitu:
- Ubah Staff
- Ubah Role
- Tambah Episode
- Hapus Episode
- (!) Drop

**Ubah Staff** akan membawa anda dalam proses mengubah posisi tertentu dengan staff lain (jikalau ada kesalahan, atau memang ada perubahan.)<br>
**Ubah Role** akan mengubah role yang dipakai untuk garapan tersebut, role dipakai untuk pengecekan agar garapan tersebut hanya dapat diubah statusnya oleh role tersebut.<br>
**Tambah Episode** akan menambah episode dengan jumlah tertentu, instruksi lengkap ada di mode tersebut.<br>
**Hapus Episode** akan menghapus episode dengan range tertentu, instruksi lengkap ada di mode tersebut.<br>
**Drop (!!!)** akan menghapus garapan dari database untuk selamanya.

#### Dalam .gif

##### !tagih<br>
![tagih](https://p.ihateani.me/NLu8jpFr.gif)

##### !staff<br>
![staff](https://p.ihateani.me/X9TppU1y.gif)

##### !staff<br>
![staff](http://p.ihateani.me/z7O78goi.gif)

<br><br>

##### !beres<br>
![beres](https://p.ihateani.me/ZcAtLsiO.gif)

##### !gakjadi<br>
![gakjadi](https://p.ihateani.me/gjCfsFpA.gif)

##### !tandakan
![tandakan](https://p.ihateani.me/eOVoUfoD.gif)

##### !rilis | !rilis batch | !rilis semua<br>
![rilis](http://p.ihateani.me/OyNzFpoL.gif)

<br><br>

##### !tambahutang<br>
![tambahutang](https://p.ihateani.me/ifQMCsOt.gif)

##### !ubahdata<br>
![ubahdata](http://p.ihateani.me/0V0wbuFu.gif)
