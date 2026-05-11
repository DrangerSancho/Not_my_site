[index.html.html](https://github.com/user-attachments/files/27593415/index.html.html)

<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>С Днём Рождения 💖</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: 'Segoe UI', sans-serif;
}

body{
    background: linear-gradient(180deg,#ffd6e7,#fff0f6);
    overflow:hidden;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    position:relative;
}

/* Сердечки */
.heart{
    position:absolute;
    color:#ff5c93;
    animation: float 8s linear infinite;
    opacity:0.7;
    font-size:20px;
}

@keyframes float{
    0%{
        transform:translateY(100vh) scale(1);
        opacity:0;
    }
    20%{
        opacity:0.7;
    }
    100%{
        transform:translateY(-120px) scale(1.5);
        opacity:0;
    }
}

.container{
    width:90%;
    max-width:500px;
    background:white;
    border-radius:30px;
    padding:35px;
    text-align:center;
    box-shadow:0 10px 30px rgba(255,105,180,0.2);
    position:relative;
    z-index:2;
}

.slide{
    display:none;
    animation:fade 0.6s ease;
}

.slide.active{
    display:block;
}

@keyframes fade{
    from{
        opacity:0;
        transform:translateY(20px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

.envelope{
    width:220px;
    height:150px;
    background:#ffb6cc;
    margin:0 auto 25px;
    border-radius:20px;
    position:relative;
    display:flex;
    justify-content:center;
    align-items:center;
    color:white;
    font-size:35px;
    font-weight:bold;
}

.envelope::before{
    content:"💌";
    position:absolute;
    top:15px;
    font-size:25px;
}

h1{
    color:#ff4f8b;
    margin-bottom:15px;
}

p{
    color:#555;
    font-size:18px;
    line-height:1.5;
    margin-bottom:20px;
}

.btn{
    border:none;
    background:linear-gradient(90deg,#ff5c93,#ff2e74);
    color:white;
    padding:14px 30px;
    border-radius:40px;
    cursor:pointer;
    font-size:17px;
    margin:10px;
    transition:0.3s;
    box-shadow:0 5px 15px rgba(255,92,147,0.4);
}

.btn:hover{
    transform:scale(1.07);
}

.gif-placeholder{
    width:100%;
    height:220px;
    border:3px dashed #ff8db5;
    border-radius:20px;
    margin:20px 0;
    display:flex;
    justify-content:center;
    align-items:center;
    color:#ff5c93;
    font-size:18px;
    background:#fff5f9;
}

.big-text{
    max-height:300px;
    overflow:auto;
    text-align:left;
    padding-right:5px;
}

.big-text::-webkit-scrollbar{
    width:6px;
}

.big-text::-webkit-scrollbar-thumb{
    background:#ff8db5;
    border-radius:10px;
}
</style>
</head>

<body>

<!-- Сердечки -->
<script>
for(let i=0;i<25;i++){
    let heart=document.createElement('div');
    heart.className='heart';
    heart.innerHTML='💖';
    heart.style.left=Math.random()*100+'vw';
    heart.style.animationDuration=(5+Math.random()*5)+'s';
    heart.style.fontSize=(15+Math.random()*20)+'px';
    document.body.appendChild(heart);
}
</script>

<div class="container">

    <!-- Слайд 1 -->
    <div class="slide active" id="slide1">
        <div class="envelope">love</div>

        <h1>У меня для тебя письмо... 💕</h1>

        <button class="btn" onclick="nextSlide(2)">Далее →</button>
    </div>

    <!-- Слайд 2 -->
    <div class="slide" id="slide2">

        <h1>Хочешь ли открыть? 🥺</h1>

        <div class="gif-placeholder">
            <img src="https://giffun.ru/wp-content/uploads/2023/02/0a6f0697514f5517e35b2e741eaaabed.gif" style="width:100%; height:100%; object-fit:cover; border-radius:20px;">
        </div>

        <button class="btn" onclick="openLetter()">Открыть 💌</button>
        <button class="btn" onclick="nope()">Не-а</button>

        <p id="pleaseText"></p>
    </div>

    <!-- Слайд 3 -->
    <div class="slide" id="slide3">

        <h1>С Днём Рождения 🎂💖</h1>

        <div class="gif-placeholder">
            <img src="https://cojo.ru/wp-content/uploads/2024/01/milye-stikery-obnimashki-11.gif" style="width:100%; height:100%; object-fit:cover; border-radius:20px;">
        </div>

        <p>
            Поздравляю тебя с Днём Рождения 💕<br><br>

            Желаю тебе огромного счастья, море улыбок,
            исполнения всех мечт и чтобы каждый твой день
            был наполнен теплом, радостью и любовью 💫
        </p>

        <button class="btn" onclick="nextSlide(4)">Далее 💖</button>
    </div>

    <!-- Слайд 4 -->
    <div class="slide" id="slide4">

        <h1>Для тебя 💌</h1>

        <div class="big-text">
            <p>
                Сегодня особенный день, потому что сегодня родился
                самый замечательный человек 💖<br><br>

                Спасибо тебе за твою доброту, заботу, поддержку
                и за все моменты, которые делают жизнь ярче и теплее ✨<br><br>

                Пусть у тебя всегда всё получается, пусть рядом будут
                только хорошие люди, а счастье никогда не заканчивается 🌸<br><br>

                Я очень хочу, чтобы ты чаще улыбался,
                верил в себя и никогда не грустил 🫶<br><br>

                Пусть впереди тебя ждёт только самое прекрасное:
                успех, радость, любовь, вдохновение и исполнение
                каждой мечты 🌷<br><br>

                С Днём Рождения тебя 💕
            </p>
        </div>

    </div>

</div>

<script>
function nextSlide(num){
    document.querySelectorAll('.slide').forEach(slide=>{
        slide.classList.remove('active');
    });

    document.getElementById('slide'+num).classList.add('active');
}

function nope(){
    document.getElementById('pleaseText').innerHTML =
    "Ну пожалуйста давай ещё раз 🥺💖";

    let btns = document.querySelectorAll('#slide2 .btn');

    btns[1].innerText = "Ещё раз ?";
}

function openLetter(){
    nextSlide(3);
}
</script>

</body>
</html>
