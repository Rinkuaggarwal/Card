<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Happy Anniversary</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', sans-serif;
            background: linear-gradient(135deg, #fdf0f3, #fde2e4);
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .card {
            background: #ffffff;
            width: 380px;
            padding: 25px;
            border-radius: 18px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
            text-align: center;
        }

        .card h1 {
            color: #b11226;
            margin-bottom: 10px;
        }

        .card h2 {
            font-size: 20px;
            color: #333;
            margin-bottom: 15px;
        }

        .photo-box {
            width: 100%;
            height: 200px;
            border: 2px dashed #d1d1d1;
            border-radius: 12px;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            margin-bottom: 15px;
            background: #fafafa;
        }

        .photo-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        input[type="file"] {
            margin-bottom: 15px;
        }

        .message {
            font-size: 15px;
            color: #555;
            line-height: 1.6;
        }

        .footer {
            margin-top: 15px;
            font-weight: bold;
            color: #b11226;
        }

        .heart {
            color: red;
        }
    </style>
</head>
<body>

<div class="card">
    <h1>Happy Anniversary</h1>
    <h2>Dear Chacha & Chachi <span class="heart">❤️</span></h2>

    <div class="photo-box">
        <img id="preview" src="/storage/emulated/0/Clone Phone/DCIM/Jaan/IMG_20260203_151501.jpg" alt="Upload Photo">
    </div>

    <input type="file" accept="image/*" onchange="loadPhoto(event)">

    <p class="message">
        Wishing you both a lifetime filled with love, laughter, and togetherness.
        Your bond is truly inspiring and your love grows stronger with every passing year.
    </p>

    <div class="footer">
        With Love & Best Wishes 💐
    </div>
</div>

<script>
    function loadPhoto(event) {
        const image = document.getElementById('preview');
        image.src = URL.createObjectURL(event.target.files[0]);
    }
</script>

</body>
</html>
