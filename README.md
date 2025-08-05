# website
web
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>LizalStore - Jual Followers Murah</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    function updateHarga() {
      const layanan = document.getElementById('layanan').value;
      const jumlah = parseInt(document.getElementById('jumlah').value);
      let hargaPerUnit = 0;

      if (layanan === 'Instagram Followers') hargaPerUnit = 25;
      if (layanan === 'TikTok Followers') hargaPerUnit = 30;
      if (layanan === 'YouTube Subscribers') hargaPerUnit = 50;

      const total = jumlah * hargaPerUnit;
      document.getElementById('harga').innerText = isNaN(total) ? 'Rp0' : `Rp${total.toLocaleString('id-ID')}`;
    }
  </script>
</head>
<body class="bg-gray-100 font-sans">

  <!-- Navbar -->
  <header class="bg-white shadow-md">
    <div class="container mx-auto flex justify-between items-center p-4">
      <h1 class="text-xl font-bold text-blue-600">LizalStore</h1>
      <a href="#order" class="bg-blue-600 text-white px-4 py-2 rounded-lg">Pesan Sekarang</a>
    </div>
  </header>

  <!-- Hero -->
  <section class="text-center py-12 bg-blue-100">
    <h2 class="text-3xl font-bold mb-4">Jual Followers Sosial Media Murah</h2>
    <p class="text-gray-700">Instagram, TikTok, YouTube & lainnya</p>
  </section>

  <!-- Layanan -->
  <section class="container mx-auto py-10 px-4">
    <h3 class="text-2xl font-semibold mb-6 text-center">Layanan Kami</h3>
    <div class="grid md:grid-cols-3 gap-6">
      <div class="bg-white p-6 rounded-lg shadow">
        <h4 class="text-lg font-bold mb-2">Instagram Followers</h4>
        <p>1000 followers - Rp25.000</p>
      </div>
      <div class="bg-white p-6 rounded-lg shadow">
        <h4 class="text-lg font-bold mb-2">TikTok Followers</h4>
        <p>1000 followers - Rp30.000</p>
      </div>
      <div class="bg-white p-6 rounded-lg shadow">
        <h4 class="text-lg font-bold mb-2">YouTube Subscribers</h4>
        <p>1000 subs - Rp50.000</p>
      </div>
    </div>
  </section>

  <!-- Formulir Pemesanan -->
  <section id="order" class="bg-white py-10 px-4">
    <div class="container mx-auto max-w-xl">
      <h3 class="text-2xl font-semibold mb-4">Formulir Pemesanan</h3>
      <form class="space-y-4">
        <input type="text" placeholder="Nama Anda" class="w-full border p-2 rounded" required />
        <input type="text" placeholder="Username/Link Akun" class="w-full border p-2 rounded" required />
        <select id="layanan" class="w-full border p-2 rounded" onchange="updateHarga()" required>
          <option value="">Pilih Layanan</option>
          <option value="Instagram Followers">Instagram Followers</option>
          <option value="TikTok Followers">TikTok Followers</option>
          <option value="YouTube Subscribers">YouTube Subscribers</option>
        </select>
        <input type="number" id="jumlah" placeholder="Jumlah" class="w-full border p-2 rounded" oninput="updateHarga()" required />

        <!-- Harga Otomatis -->
        <div class="bg-gray-50 p-3 border rounded text-center">
          <p class="font-semibold">Total Harga:</p>
          <p id="harga" class="text-xl font-bold text-green-600">Rp0</p>
        </div>

        <!-- DANA Payment Section -->
        <div class="text-center mt-4">
          <p class="font-semibold">Pembayaran via DANA</p>
          <div class="bg-blue-50 p-4 rounded border w-full">
            <p class="text-lg font-bold text-blue-700">0821 2911 1408</p>
            <p class="text-gray-600">A/N: RUSLIZAL</p>
          </div>
        </div>

        <!-- ShopeePay Payment Section -->
        <div class="text-center mt-4">
          <p class="font-semibold">Pembayaran via ShopeePay</p>
          <div class="bg-orange-50 p-4 rounded border w-full">
            <p class="text-lg font-bold text-orange-600">0821 2911 1408</p>
            <p class="text-gray-600">A/N: RUSLIZAL</p>
          </div>
        </div>

        <!-- Upload Bukti Pembayaran -->
        <div>
          <label class="block mb-2 font-semibold mt-6">Upload Bukti Pembayaran</label>
          <input type="file" accept="image/*" class="w-full border p-2 rounded bg-white" required />
          <p class="text-sm text-gray-500 mt-1">Format gambar: JPG, PNG</p>
        </div>

        <a href="https://wa.me/6282129111408" class="block bg-green-500 text-white text-center py-2 rounded">Konfirmasi via WhatsApp</a>
      </form>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-gray-800 text-white text-center py-4 mt-10">
    &copy; 2025 LizalStore. All rights reserved.
  </footer>

</body>
</html>
