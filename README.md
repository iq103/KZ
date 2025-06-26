<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>من قلبي إليه - هدية شعرية رومانسية</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #ffe6f0, #fff0f5);
            color: #5a3d5c;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
            line-height: 1.6;
            overflow-x: hidden;
            position: relative;
        }
        
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://i.ibb.co/mP71DTN/IMG-2936.jpg') no-repeat center center;
            background-size: cover;
            opacity: 0.4;
            z-index: -1;
        }
        
        .container {
            max-width: 800px;
            width: 100%;
            text-align: center;
            padding: 40px 30px;
            position: relative;
            z-index: 2;
        }
        
        .heart-icon {
            font-size: 3rem;
            color: #fca5b0;
            margin-bottom: 20px;
            animation: pulse 2s infinite;
            text-shadow: 0 0 20px rgba(252, 165, 176, 0.5);
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }
        
        h1 {
            font-size: 3.5rem;
            color: #9d3b6e;
            margin-bottom: 30px;
            font-weight: 700;
            text-shadow: 0 2px 8px rgba(157, 59, 110, 0.2);
            letter-spacing: 1px;
        }
        
        .poem-container {
            background: rgba(255, 255, 255, 0.85);
            border-radius: 20px;
            padding: 40px 30px;
            margin: 30px 0;
            position: relative;
            min-height: 220px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            transition: all 0.5s ease;
            box-shadow: 0 10px 30px rgba(252, 165, 176, 0.3);
            border: 2px solid rgba(252, 165, 176, 0.2);
        }
        
        .poem-box {
            font-size: 1.8rem;
            line-height: 2.5;
            color: #7d3c5c;
            font-weight: 500;
        }
        
        .poem-line {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.8s ease, transform 0.8s ease;
            margin: 10px 0;
        }
        
        .poem-line.show {
            opacity: 1;
            transform: translateY(0);
        }
        
        .btn-container {
            margin: 40px 0 20px;
        }
        
        #newPoemBtn {
            background: linear-gradient(145deg, #fca5b0, #e8919d);
            color: white;
            border: none;
            border-radius: 50px;
            padding: 20px 60px;
            font-size: 1.7rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 10px 25px rgba(252, 165, 176, 0.4);
            position: relative;
            overflow: hidden;
            letter-spacing: 1px;
        }
        
        #newPoemBtn:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(252, 165, 176, 0.6);
        }
        
        #newPoemBtn:active {
            transform: translateY(2px);
        }
        
        #newPoemBtn::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.2);
            transform: translateX(-100%);
            transition: transform 0.5s ease;
        }
        
        #newPoemBtn:hover::after {
            transform: translateX(100%);
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .fade-in {
            animation: fadeIn 1.5s ease forwards;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.8rem;
            }
            
            .poem-box {
                font-size: 1.5rem;
                line-height: 2.2;
            }
            
            #newPoemBtn {
                padding: 18px 50px;
                font-size: 1.5rem;
            }
        }
        
        @media (max-width: 480px) {
            h1 {
                font-size: 2.3rem;
            }
            
            .poem-box {
                font-size: 1.3rem;
                line-height: 2.0;
            }
            
            #newPoemBtn {
                padding: 16px 40px;
                font-size: 1.3rem;
            }
            
            .container {
                padding: 20px 15px;
            }
            
            .heart-icon {
                font-size: 2.5rem;
            }
            
            .poem-container {
                padding: 30px 20px;
            }
        }
        
        /* Floating hearts */
        .heart {
            position: absolute;
            width: 24px;
            height: 24px;
            background-color: #fca5b0;
            opacity: 0;
            pointer-events: none;
            z-index: 10;
        }
        
        .heart::before, .heart::after {
            content: '';
            position: absolute;
            width: 24px;
            height: 24px;
            background-color: #fca5b0;
            border-radius: 50%;
        }
        
        .heart::before {
            top: -12px;
            left: 0;
        }
        
        .heart::after {
            top: 0;
            left: -12px;
        }
        
        @keyframes float {
            0% {
                opacity: 1;
                transform: translateY(0) rotate(0deg);
            }
            100% {
                opacity: 0;
                transform: translateY(-120px) rotate(360deg);
            }
        }
        
        /* Decorative elements */
        .floating-text {
            position: absolute;
            color: rgba(252, 165, 176, 0.15);
            font-size: 6rem;
            font-weight: 800;
            z-index: 1;
            pointer-events: none;
            transform: rotate(-25deg);
            top: 20%;
            left: 5%;
            animation: floatText 30s linear infinite;
        }
        
        @keyframes floatText {
            0% { transform: rotate(-25deg) translateX(-100px); }
            100% { transform: rotate(-25deg) translateX(100px); }
        }
    </style>
</head>
<body>
    <div class="floating-text">♥ حب ♥</div>
    <div class="floating-text" style="top: 70%; left: 70%; transform: rotate(15deg);">♥ رومانسية ♥</div>
    
    <div class="container fade-in">
        <div class="heart-icon">❤</div>
        <h1>من قلبي إليه</h1>
        
        <div class="poem-container">
            <div class="poem-box" id="poemBox">
                <!-- الشعر سيتم عرضه هنا بالجافاسكريبت -->
            </div>
        </div>
        
        <div class="btn-container">
            <button id="newPoemBtn">همسة جديدة</button>
        </div>
    </div>

    <script>
        // مجموعة الأشعار الرومانسية (3 شعر فقط)
        const poems = [
            [
                "أنتِ النور الذي يضيء دربي",
                "والماء الذي يروي ظمأ روحي",
                "أنتِ الحب الذي يملأ قلبي",
                "وأنتِ الحياة التي أعيشها"
            ],
            [
                "في عينيكِ وجدت وطني وحبي",
                "وفيكِ رأيتُ دربي ومنتهى طريقي",
                "فلا تبتعدي، فبدونكِ يا حبيبتي",
                "أكون كطيرٍ بلا جناحٍ ولا أملٍ في التحليق"
            ],
            [
                "أشتاق إليكِ كما يشتاق الظمأ للماء",
                "وكما يشتاق العصفور للأغصان في الربيع",
                "أشتاق لدفءِ يديكِ وهمسِ كلامكِ",
                "فهل من لقاءٍ قريبٍ يطفئ لهيب الشوق؟"
            ]
        ];

        // عناصر DOM
        const poemBox = document.getElementById('poemBox');
        const newPoemBtn = document.getElementById('newPoemBtn');
        
        // إنشاء عناصر القلوب
        function createHearts() {
            for (let i = 0; i < 20; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.classList.add('heart');
                    heart.style.left = Math.random() * 100 + 'vw';
                    heart.style.animation = `float ${Math.random() * 3 + 2}s linear forwards`;
                    document.body.appendChild(heart);
                    
                    // إزالة القلب بعد انتهاء الرسوم المتحركة
                    setTimeout(() => {
                        heart.remove();
                    }, 5000);
                }, i * 150);
            }
        }
        
        // عرض شعر عشوائي مع حركة ناعمة
        function displayRandomPoem() {
            // إنشاء قلوب متحركة
            createHearts();
            
            // إخفاء الأسطر الحالية
            const lines = poemBox.querySelectorAll('.poem-line');
            lines.forEach(line => {
                line.classList.remove('show');
            });
            
            // اختيار شعر عشوائي
            const randomIndex = Math.floor(Math.random() * poems.length);
            const selectedPoem = poems[randomIndex];
            
            // مسح المحتوى الحالي بعد فترة قصيرة
            setTimeout(() => {
                poemBox.innerHTML = '';
                
                // إضافة الأسطر الجديدة مع حركة ظهور تدريجي
                selectedPoem.forEach((line, index) => {
                    const p = document.createElement('p');
                    p.classList.add('poem-line');
                    p.textContent = line;
                    poemBox.appendChild(p);
                    
                    // تأخير ظهور كل سطر
                    setTimeout(() => {
                        p.classList.add('show');
                    }, 300 * (index + 1));
                });
            }, 500);
        }
        
        // تهيئة الصفحة عند التحميل
        window.addEventListener('DOMContentLoaded', () => {
            // عرض شعر عند التحميل الأولي
            displayRandomPoem();
            
            // إضافة حدث النقر على الزر
            newPoemBtn.addEventListener('click', displayRandomPoem);
        });
    </script>
</body>
</html>
