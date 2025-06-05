<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Daftar Pasien Hewan</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f7f5;
      padding: 20px;
    }
    .form-box {
      max-width: 500px;
      margin: auto;
      background: white;
      padding: 25px;
      border-radius: 12px;
      box-shadow: 0 3px 15px rgba(0,0,0,0.1);
    }
    h2 {
      text-align: center;
      color: #28a745;
    }
    label {
      margin-top: 10px;
      display: block;
      font-weight: bold;
    }
    input, select, textarea, button {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      border-radius: 8px;
      border: 1px solid #ccc;
      margin-bottom: 15px;
    }
    button {
      background-color: #28a745;
      color: white;
      font-size: 16px;
      border: none;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <div class="form-box">
    <body>

      <div class="form-box">
    
        <div style="text-align:center; margin-bottom:20px;">
          <img src="c:\Users\Admin\Downloads\198894855_325139759319332_5871666010250345741_n.jpg" alt="Logo Klinik" style="width:120px; height:auto;"/>
          <h1 style="color:#000000; margin-top:10px;">Klinik Hewan Anugerah Satwa</h1>
        </div>
    
    <h2>Formulir Pasien Hewan 🐶🐱</h2>
    <form id="whatsappForm">
      <label>Nama Pemilik:</label>
      <input type="text" id="namaPemilik" required>

      <label>Nama Hewan:</label>
      <input type="text" id="namaHewan" required>
      
    <label>Jenis Hewan:</label>
      <select id="jenisHewan" required>
        <option value="">Pilih jenis</option>
        <option value="Kucing">Kucing</option>
        <option value="Anjing">Anjing</option>
        <option value="Kelinci">Kelinci</option>
        <option value="Burung">Burung</option>
        <option value="Lainnya">Lainnya</option>
      </select>
      
      <label>alamat:</label>
      <input type="text" id="alamat" required>

      <label>Keluhan:</label>
      <textarea id="keluhan" rows="3" required></textarea>

      <button type="submit">Kirim ke WhatsApp Admin</button>
    </form>
  </div>

  <script>
    document.getElementById("whatsappForm").addEventListener("submit", function(e) {
      e.preventDefault();

      const namaPemilik = document.getElementById("namaPemilik").value;
      const namaHewan = document.getElementById("namaHewan").value;
      const jenisHewan = document.getElementById("jenisHewan").value;
      const keluhan = document.getElementById("keluhan").value;

      const phoneNumber = "6281234567890"; // GANTI dengan nomor WA admin kamu (pakai 62, bukan 0)

      const message = `Halo Admin Klinik Hewan! 🐾%0ASaya ingin mendaftarkan hewan peliharaan saya:%0A%0A` +
        `👤 Nama Pemilik: ${namaPemilik}%0A` +
        `🐶 Nama Hewan: ${namaHewan}%0A` +
        `📋 Jenis Hewan: ${jenisHewan}%0A` +
        `💬 Keluhan: ${keluhan}`;

      window.open(`https://wa.me/${}?text=${message}`, '_blank');
    });
  </script>

</body>
</html>
