# Registrasi-wa
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registrasi Masuk Grup</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin: 50px; }
        form { max-width: 300px; margin: auto; }
        input, button { width: 100%; padding: 10px; margin: 5px 0; }
    </style>
</head>
<body>

    <h2>Daftar Masuk Grup WhatsApp</h2>
    <form id="registrationForm">
        <input type="text" id="nama" placeholder="Nama" required>
        <input type="number" id="umur" placeholder="Umur" required>
        <input type="text" id="askot" placeholder="Asal Kota" required>
        <button type="button" onclick="kirimWhatsApp()">Daftar & Masuk Grup</button>
    </form>

    <script>
        function kirimWhatsApp() {
            var nama = document.getElementById("nama").value;
            var umur = document.getElementById("umur").value;
            var askot = document.getElementById("askot").value;

            if (nama && umur && askot) {
                var pesan = `Halo, saya ingin masuk grup!\nNama: ${nama}\nUmur: ${umur}\nAsal Kota: ${askot}`;
                var nomorAdmin = "6285824390625"; // Ganti dengan nomor admin

                var url = `https://wa.me/${nomorAdmin}?text=${encodeURIComponent(pesan)}`;
                window.open(url, "_blank");

                // Redirect ke grup WhatsApp setelah pendaftaran
                setTimeout(() => {
                    window.location.href = "https://chat.whatsapp.com/LNmgwawdgukGhZZifI5t7o";
                }, 3000);
            } else {
                alert("Harap isi semua data!");
            }
        }
    </script>

</body>
</html>
