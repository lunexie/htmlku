<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<title>Raja Ampat</title>
<style>
    body {
        margin: 0;
        font-family: Arial, sans-serif;
        background-color: #5fbcf5;
    }

    /* ===== HEADER 500px ===== */
    .header {
        width: 100%;
        height: 500px; 
        background-image: url('bg.jpg');
        background-size: cover;
        background-position: center;
        border-bottom: 2px solid black;
        padding: 10px;
        box-sizing: border-box;
    }

    .logo {
        width: 200px;
        height: 75px;
        border: 1px solid rgb(53, 152, 194);
        border-radius: 8px;
        background-color: white;
        background-image: url('logo.jpg'); 
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
        float: left; 
    }

    .menu {
        float: right; 
        margin-top: 25px;
    }

    .menu a {
        text-decoration: none;
        color: white;
        font-weight: bold;
        padding: 0 10px;
        text-shadow: 1px 1px 3px black;
        font-size: 18px;
    }

    .banner-text {
        clear: both; 
        text-align: center;
        margin-top: 180px;
        font-size: 32px;
        color: white;
        font-weight: bold;
        text-shadow: 2px 2px 4px rgb(51, 123, 168);
    }

    /* ===== BODYSECTION ===== */
    .wadah {
        width: 1000px;
        margin: 20px auto;
        background-color: #acf3f4;
        border: 2px solid black;
        border-radius: 10px;
        padding: 20px;
        box-sizing: border-box;
        overflow: hidden;
    }

    .kiri {
        width: 35%;
        float: left; 
        padding: 10px;
        box-sizing: border-box;
    }

    .kanan {
        width: 60%;
        float: right;
        padding: 10px;
        box-sizing: border-box;
        min-height: 320px;
    }

    .tombol {
        width: 100%;
        padding: 15px;
        margin-bottom: 10px;
        background-color: #46b2d6; 
        color: white;
        border: none;
        border-radius: 8px;
        font-size: 16px;
        font-weight: bold;
        cursor: pointer;
    }

    .tombol:hover {
        background-color: #66f792;
        color: #333;
    }

    h2 { 
        color: #4a3b2a; 
        font-style: italic; 
        margin-top: 0;
    }

    p { 
        color: #5a4a3a; 
        line-height: 1.8; 
    }

    /* Gambar Konten 300px x 300px Sesuai Wireframe Layout */
    .img-konten {
        width: 300px;
        height: 300px;
        object-fit: cover;
        float: right;
        margin-left: 15px;
        margin-bottom: 15px;
        border: 2px solid #333;
        border-radius: 8px;
    }

    /* ===== FOOTER 200px ===== */
    .footer {
        width: 100%;
        height: 200px; 
        background-color: #333;
        color: white;
        border-top: 2px solid black;
        padding: 20px 40px;
        box-sizing: border-box;
        clear: both; 
    }

    .footer-logo {
        width: 200px;
        height: 75px;
        border: 1px solid rgb(179, 201, 34);
        background-color: white;
        background-image: url('logo.jpg'); 
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
        float: left;
    }

    .footer-kolom {
        width: 20%;
        float: left;
        margin-left: 40px;
    }

    .footer-kolom ul { list-style: none; padding: 0; margin: 0; }
    .footer-kolom h4 { margin-bottom: 10px; margin-top: 0; }
    .footer-kolom li { margin-bottom: 5px; }
</style>
</head>
<body>

<!-- HEADER -->
<div class="header">
    <div class="logo"></div>
    <div class="menu">
        <a href="#">Home</a> | 
        <a href="#">Service</a> | 
        <a href="#">Contact</a> | 
        <a href="#">About</a>
    </div>
    <div class="banner-text">RAJA AMPAT INDONESIA</div>
</div>

<!-- BODYSECTION -->
<div class="wadah">
    <div class="kiri">
        <button class="tombol" onclick="ganti('Lokasi dan Geografi Letak')">Lokasi dan Geografi Letak</button>
        <button class="tombol" onclick="ganti('Pulau Utama')">Pulau Utama</button>
        <button class="tombol" onclick="ganti('Jumlah Pulau')">Jumlah Pulau</button>
        <button class="tombol" onclick="ganti('Ibu Kota')">Ibu Kota</button>
    </div>

    <div class="kanan" id="isi">
        <h2>Raja Ampat</h2>
        <p>Raja Ampat adalah gugusan kepulauan indah di Provinsi Papua Barat Daya yang terkenal dengan keanekaragaman hayati bawah laut tertinggi di dunia.</p>
    </div>
</div>

<!-- FOOTER -->
<div class="footer">
    <div class="footer-logo"></div>

    <div class="footer-kolom">
        <h4>Quick Link</h4>
        <ul>
          <li>Home</li>
          <li>Service</li>
          <li>Contact</li>
        </ul>
    </div>
    <div class="footer-kolom">
        <h4>Lainnya</h4>
        <ul>
          <li>Policy</li>
          <li>Site map</li>
        </ul>
    </div>
    <div class="footer-kolom">
        <h4>Medsos</h4>
        <ul>
          <li>FB</li>
          <li>IG</li>
          <li>Tiktok</li>
        </ul>
    </div>
</div>

<script>
    function ganti(pilih) {
        var wadahKonten = document.getElementById("isi");

        if(pilih == "Lokasi dan Geografi Letak") {
            wadahKonten.innerHTML = 
            '<img src="lokasi.jpg" alt="Lokasi dan Geografi Letak" class="img-konten">' +
            '<h2>Lokasi dan Geografi Letak</h2>' +
            '<p>Berada di bagian paling barat Pulau Papua, kepulauan ini masuk dalam wilayah administratif Provinsi Papua Barat Daya. Letaknya yang strategis di jantung segitiga terumbu karang dunia menjadikannya surga bagi keanekaragaman hayati laut.</p>';
        }
        else if(pilih == "Pulau Utama") {
            wadahKonten.innerHTML = 
            '<img src="jumlah.jpg" alt="Pulau Utama" class="img-konten">' +
            '<h2>Pulau Utama</h2>' +
            '<p>Raja Ampat terdiri dari empat pulau besar utama, yaitu Pulau Waigeo, Pulau Misool, Pulau Salawati, dan Pulau Batanta. Nama "Raja Ampat" sendiri dipercaya berasal dari mitologi setempat yang merujuk pada empat raja yang menguasai empat pulau besar tersebut.</p>';
        }
        else if(pilih == "Jumlah Pulau") {
            wadahKonten.innerHTML = 
            '<img src="jumlah.jpg" alt="Jumlah Pulau" class="img-konten">' +
            '<h2>Jumlah Pulau</h2>' +
            '<p>Wilayah kepulauan ini mencakup area yang sangat luas dengan gugusan pulau karang (karst) yang membentang. Terdiri dari ribuan pulau kecil dan pulau karang dengan total keseluruhan diperkirakan mencapai lebih dari 1.500 hingga 2.900 pulau.</p>';
        }
        else if(pilih == "Ibu Kota") {
            wadahKonten.innerHTML = 
            '<img src="ibu.jpg" alt="Ibu Kota" class="img-konten">' +
            '<h2>Ibu Kota</h2>' +
            '<p>Pusat pemerintahan dan administrasi Kabupaten Raja Ampat berpusat di Kota Waisai, yang terletak di bagian selatan Pulau Waigeo. Waisai juga menjadi gerbang utama bagi para wisatawan yang datang berkunjung.</p>';
        }
    }
</script>

</body>
</html># htmlku
html baru
