# Web Script
Kumpulan script website sebagai penghubung antara database dengan website

* [Website Progress](#naotimes-website-progress)

## naoTimes Website Progress

Menghubungkan progress garapan dari database bot ke website.

### Instalasi {docsify-ignore}

1. Download file `naoTimes.js` atau `naoTimes.min.js`
2. Ubah line berikut di `naoTimes.js` atau `naoTimes.min.js`
    ```js
    var gist_raw_url = 'MASUKAN URL RAW GIST TANPA REVISI COMMIT';
    ```
    - Format link raw gist: `https://gist.githubusercontent.com/GITHUB_USERNAME/GIST_ID/raw/GIST_FILENAME.EXT`
    - Merupakan link ke database naoTimes di gist
3. Tambahkan script javascript ke website
4. Selipkan snippet html berikut:
    ```html
    <div id='naotimes' class="progress-wrapper">
        <script type="text/javascript" src="/link/menuju/naoTimes.js"></script> <!-- Ubah line ini -->
        <script type="text/javascript">
            naoTimesProcess("MASUKAN ID SERVER DISCORD DI SINI"); // Ubah line ini
        </script>
        <h1 class="naotimes-header">Status Garapan</h1>
        <img id='naotimes-loading' width="40" height="40" src='https://puu.sh/DiJzU/6af20efe7e.gif'>
    </div>
    ```
5. Kustomisasi dengan css, listnya ada:
    - **naotimes-header**: teks header dengan tulisan `Status Garapan`
    - **naotimes-animetitle**: bagian judul anime
    - **naotimes-animeprogress**: bagian anime untuk progressnya

**Bisa diganti dengan versi minimal dengan mengganti `.js` ke `.min.js`**
