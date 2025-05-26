<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Shaxsiy Video Darsliklar Sayti</title>
<link rel="stylesheet" href="style.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f4f8;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #3f51b5;
            color: white;
            padding: 20px;
            text-align: center;
        }
        main {
            padding: 30px;
            max-width: 800px;
            margin: 0 auto;
        }
        .video-list {
            list-style-type: none;
            padding: 0;
        }
        .video-list li {
            background-color: white;
            margin-bottom: 15px;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 2px 6px rgba(0,0,0,0.1);
        }
        .video-list li video {
            max-width: 100%;
            height: 150px;
            border-radius: 4px;
            display: block;
            margin-bottom: 10px;
        }
        footer {
            text-align: center;
            padding: 15px;
            background-color: #3f51b5;
            color: white;
            margin-top: 40px;
        }
        .video-title {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .m1 {
            background-color: #e8f0fe;
            border: 1px solid #c5cae9;
        }
        .m2 {
            background-color: #fce4ec;
            border: 1px solid #f8bbd0;
        }
        .m3 {
            background-color: #e3f2fd;
            border: 1px solid #bbdefb;
        }
        </style>
</head>
<body>
    <header>
        <h1>Shaxsiy Video Darsliklar</h1>
        <p>Faqat login egalariga mo‘ljallangan sayt</p>
    </header>
    <main>
        <h2>Darsliklar ro‘yxati</h2>
        <ul class="video-list">
            <li class="m1">
                <video controls>
                    <source src="./video.mp4/m1.mp4" type="video/mp4" />
                    Sizning brauzeringiz video formatini qo‘llab-quvvatlamaydi.
                </video>
                <h3>Dars 1: HTML asoslari</h3>
                <p>Ushbu dars HTML ning asosiy elementlarini tushuntiradi.</p>
            </li>
            <li class="m2">
                <video controls>
                    <source src="./video.mp4/m2.mp4" type="video/mp4" />
                    Sizning brauzeringiz video formatini qo‘llab-quvvatlamaydi.
                </video>
                <h3>Dars 2: CSS bilan ishlash</h3>
                <p>Bu dars CSS yordamida sahifani bezashni o‘rgatadi.</p>
            </li>
              <li class="m3">
                <video controls>
                    <source src="./video.mp4/m3.mp4" type="video/mp4" />
                    Sizning brauzeringiz video formatini qo‘llab-quvvatlamaydi.
                </video>
                <h3>Dars 3: CSS bilan ishlash</h3>
                <p>Bu dars CSS yordamida sahifani bezashni o‘rgatadi.</p>
            </li>
        </ul>
    </main>
    <footer>
        &copy; 2025 Shaxsiy Video Darsliklar Sayti
    </footer>
</body>
</html>
