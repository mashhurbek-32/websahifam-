<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Shaxsiy Video Darsliklar Sayti</title>
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
            height: auto;
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
            <li>
                <video controls>
                    <source src=".video/m1.mp4" type="video/mp4" />
                    Sizning brauzeringiz video formatini qo‘llab-quvvatlamaydi.
                </video>
                <h3>Dars 1: HTML asoslari</h3>
                <p>Ushbu dars HTML ning asosiy elementlarini tushuntiradi.</p>
            </li>
            <li>
                <video controls>
                    <source src=".video/m2.mp4" type="video/mp4" />
                    Sizning brauzeringiz video formatini qo‘llab-quvvatlamaydi.
                </video>
                <h3>Dars 2: CSS bilan ishlash</h3>
                <p>Bu dars CSS yordamida sahifani bezashni o‘rgatadi.</p>
            </li>
              <li>
                <video controls>
                    <source src=".video/m3.mp4" type="video/mp4" />
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
