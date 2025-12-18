# konsultasiJadwalolahraga

<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Estha AI - Konsultasi Jadwal</title>
    <style>
        /* Menghilangkan semua default margin & padding */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Memastikan body memenuhi layar penuh dan tidak bisa di-scroll keluar */
        html, body {
            width: 100%;
            height: 100%;
            overflow: hidden;
            background-color: #000; /* Warna hitam agar seamless dengan notch HP */
        }

        /* Container utama yang mengikuti ukuran layar perangkat apapun */
        .main-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Styling Iframe agar fleksibel di Tab, HP, dan PC */
        iframe {
            width: 100%;
            height: 100%;
            border: none;
            display: block;
        }
    </style>
</head>
<body>

    <div class="main-container">
        <iframe 
            src="https://studio.estha.ai/app/6943a56a9d9a8a600ad7375f" 
            allow="camera; microphone; clipboard-read; clipboard-write; geolocation; autoplay"
            allowfullscreen
            title="Estha AI Application">
        </iframe>
    </div>

</body>
</html>
