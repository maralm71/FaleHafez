# FaleHafez
<!DOCTYPE html><html lang="fa">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>فال حافظ</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
            direction: rtl;
            background-color: #ffebcd;
            background-image: url('https://example.com/hafez-nowruz.jpg'); /* لینک تصویر حافظ و عید نوروز */
            background-size: cover;
            background-position: center;
        }
        #poem-container {
            background: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            display: inline-block;
        }
        button {
            margin-top: 20px;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border: none;
            background-color: #ff4081;
            color: white;
            border-radius: 5px;
        }
        #new-year-message {
            margin-top: 30px;
            font-size: 20px;
            font-weight: bold;
            color: #d32f2f;
        }
    </style>
    <script>
        function getRandomPoem() {
            let poems = [
                {verse: "بر لب دریای خرابات منم / در دل این بحر حقایق کفنم", meaning: "من در دریای عرفان و حقیقت غرقم و در آن فنا شده‌ام."},
                {verse: "سینه از آتش دل در غم جانانه بسوخت / آتشی بود در این خانه که کاشانه بسوخت", meaning: "عشق و غم یار، دل مرا چنان سوزاند که همه وجودم را خاکستر کرد."},
                {verse: "اگر آن ترک شیرازی بدست آرد دل ما را / به خال هندویش بخشم سمرقند و بخارا را", meaning: "اگر محبوب زیبایم دل مرا بپذیرد، در برابرش همه دارایی‌هایم را فدا می‌کنم."},
                {verse: "ای که در کوی خرابات مقامی داری / جمِّ جم را چه خبر از تو که جامی داری", meaning: "ای کسی که در مسیر عشق جایگاهی داری، کسی مانند پادشاهان از این سیر و سلوک آگاه نیست."},
                {verse: "حافظا چون غم و شادی جهان در گذر است / بهتر آن است که من خاطر خود خوش دارم", meaning: "حافظ! از آنجا که دنیا ناپایدار است، بهتر است که خود را شاد و آسوده نگه داریم."}
            ];
            let randomIndex = Math.floor(Math.random() * poems.length);
            document.getElementById("poem").innerText = poems[randomIndex].verse;
            document.getElementById("meaning").innerText = poems[randomIndex].meaning;
        }
    </script>
</head>
<body onload="getRandomPoem()">
    <h1>فال حافظ</h1>
    <div id="poem-container">
        <p id="poem">...</p>
        <p id="meaning" style="font-style: italic; color: gray;">...</p>
    </div>
    <button onclick="getRandomPoem()">فال جدید</button>
    <div id="new-year-message">سال نو ۱۴۰۴ مبارک!</div>
</body>
</html>
