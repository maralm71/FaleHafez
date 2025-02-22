# FaleHafez
<!DOCTYPE html><html lang="fa">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>فال حافظ تصادفی</title>
    <style>
        body {
            font-family: 'Tahoma', sans-serif;
            text-align: center;
            margin: 50px;
            direction: rtl;
            background-color: #f9f3e4;
        }
        .fal-box {
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            display: inline-block;
        }
        button {
            margin-top: 20px;
            padding: 10px 20px;
            background: #8d6e63;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        button:hover {
            background: #6d4c41;
        }
    </style>
</head>
<body>
    <h1>فال حافظ تصادفی</h1>
    <div class="fal-box">
        <p id="fal"></p>
        <audio id="falAudio" controls hidden></audio>
        <button onclick="generateFal()">فال جدید</button>
    </div><script>
    const falList = [
        {text: "سال‌ها دل طلب جام جم از ما می‌کرد / وان چه خود داشت ز بیگانه تمنا می‌کرد", audio: "audio1.mp3"},
        {text: "ما ز یاران چشم یاری داشتیم / خود غلط بود آنچه می‌پنداشتیم", audio: "audio2.mp3"},
        {text: "ای دل گر از آن چاه زنخدان به درآیی / هر جا که روی زود پشیمان شده باشی", audio: "audio3.mp3"},
        {text: "صوفی ار باده به اندازه خورد نوشش باد / ور نه اندیشه این کار فراموشش باد", audio: "audio4.mp3"},
        {text: "در کوی نیک نامی ما را گذر ندادند / گر تو نمی‌پسندی تغییر کن قضا را", audio: "audio5.mp3"}
    ];

    function generateFal() {
        const randomIndex = Math.floor(Math.random() * falList.length);
        const selectedFal = falList[randomIndex];
        document.getElementById("fal").innerText = selectedFal.text;
        const audioElement = document.getElementById("falAudio");
        audioElement.src = selectedFal.audio;
        audioElement.hidden = false;
        audioElement.play();
    }

    window.onload = generateFal;
</script>

</body>
</html>
