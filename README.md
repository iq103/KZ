<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>أنسيت روحي - هدية شعرية</title>
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
            filter: blur(2px);
        }
        
        .container {
            max-width: 800px;
            width: 100%;
            text-align: center;
            padding: 30px;
            position: relative;
            z-index: 2;
        }
        
        .title-container {
            margin-bottom: 30px;
            perspective: 800px;
        }
        
        h1 {
            font-size: 3.5rem;
            color: #d32f2f;
            font-weight: 700;
            text-shadow: 0 2px 8px rgba(211, 47, 47, 0.3);
            letter-spacing: 1px;
            display: inline-block;
            transition: all 0.5s ease;
            transform-style: preserve-3d;
            animation: floatTitle 6s ease-in-out infinite;
        }
        
        @keyframes floatTitle {
            0%, 100% { 
                transform: translateY(0) rotateX(5deg);
                text-shadow: 0 5px 15px rgba(211, 47, 47, 0.3);
            }
            50% { 
                transform: translateY(-15px) rotateX(-5deg);
                text-shadow: 0 15px 25px rgba(211, 47, 47, 0.5);
            }
        }
        
        .poem-container {
            background: rgba(255, 255, 255, 0.92);
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
            border: 1px solid rgba(252, 165, 176, 0.2);
            overflow: hidden;
        }
        
        .poem-box {
            font-size: 1.8rem;
            line-height: 2.5;
            color: #7d3c5c;
            font-weight: 500;
            position: relative;
            z-index: 2;
        }
        
        .poem-line {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 1s ease, transform 1s ease;
            margin: 12px 0;
            transition-delay: calc(0.2s * var(--line-index));
        }
        
        .poem-line.show {
            opacity: 1;
            transform: translateY(0);
        }
        
        .btn-container {
            margin: 35px 0 15px;
        }
        
        #newPoemBtn {
            background: linear-gradient(145deg, #d32f2f, #b71c1c);
            color: white;
            border: none;
            border-radius: 50px;
            padding: 20px 60px;
            font-size: 1.7rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 10px 25px rgba(211, 47, 47, 0.4);
            position: relative;
            overflow: hidden;
            letter-spacing: 1px;
        }
        
        #newPoemBtn:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(211, 47, 47, 0.6);
            background: linear-gradient(145deg, #b71c1c, #d32f2f);
        }
        
        #newPoemBtn:active {
            transform: translateY(2px) scale(0.98);
            box-shadow: 0 5px 15px rgba(211, 47, 47, 0.5);
        }
        
        #newPoemBtn::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.3);
            transform: translateX(-100%);
            transition: transform 0.5s ease;
        }
        
        #newPoemBtn:hover::after {
            transform: translateX(100%);
        }
        
        /* حركات ظهور الشعر */
        @keyframes fadeSlideIn {
            from { 
                opacity: 0; 
                transform: translateY(30px); 
            }
            to { 
                opacity: 1; 
                transform: translateY(0); 
            }
        }
        
        .fade-slide-in {
            animation: fadeSlideIn 1.2s ease-out forwards;
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
                font-size: 3rem;
            }
            
            .poem-box {
                font-size: 1.6rem;
                line-height: 2.3;
            }
            
            #newPoemBtn {
                padding: 18px 50px;
                font-size: 1.5rem;
            }
            
            .container {
                padding: 25px;
            }
            
            .poem-container {
                padding: 35px 25px;
            }
        }
        
        @media (max-width: 480px) {
            h1 {
                font-size: 2.4rem;
            }
            
            .poem-box {
                font-size: 1.4rem;
                line-height: 2.0;
            }
            
            #newPoemBtn {
                padding: 16px 40px;
                font-size: 1.3rem;
            }
            
            .container {
                padding: 20px 15px;
            }
            
            .poem-container {
                padding: 25px 15px;
            }
        }
        
        @media (max-width: 360px) {
            h1 {
                font-size: 2.1rem;
            }
            
            .poem-box {
                font-size: 1.2rem;
            }
            
            #newPoemBtn {
                padding: 14px 35px;
                font-size: 1.2rem;
            }
        }
        
        /* خلفية شعرية متحركة */
        .poem-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.03;
            z-index: 1;
            background-image: 
                repeating-linear-gradient(
                    0deg,
                    transparent,
                    transparent 50px,
                    rgba(211, 47, 47, 0.1) 50px,
                    rgba(211, 47, 47, 0.1) 52px
                );
            animation: moveLines 60s linear infinite;
        }
        
        @keyframes moveLines {
            from { background-position: 0 0; }
            to { background-position: 0 1000px; }
        }
    </style>
</head>
<body>
    <div class="container fade-in">
        <div class="title-container">
            <h1>أنسيت روحي</h1>
        </div>
        
        <div class="poem-container">
            <div class="poem-bg"></div>
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
                "أنسيت روحي بين يديكِ حبيبتي",
                "وأضاعني الشوق في عينيكِ",
                "فهل من رحمةٍ تعيد الروح لصاحبها",
                "أم ستبقينَ حبيبتي تسرقين الروح مني؟"
            ],
            [
                "لو تدري كم أشتاق لرؤياكِ",
                "لكُنتِ ترحمين قلبي من لوعته",
                "فيا حبيبتي، يا من أخذتِ الروح والقلب",
                "هل من لقاءٍ يطفئ نار اشتياقي؟"
            ],
            [
                "أنا ذلك المسافر في دروب العشق",
                "والسائر في رحاب حبكِ",
                "فإن نسيت روحي، فلا تنسي",
                "أنكِ أنتِ الروح التي تبحث عنها"
            ]
        ];

        // عناصر DOM
        const poemBox = document.getElementById('poemBox');
        const newPoemBtn = document.getElementById('newPoemBtn');
        const title = document.querySelector('h1');
        
        // إضافة تفاعلية للعنوان
        title.addEventListener('mouseenter', () => {
            title.style.animation = 'none';
            setTimeout(() => {
                title.style.animation = 'floatTitle 6s ease-in-out infinite';
            }, 10);
        });
        
        // إضافة تأثير النقر للزر
        newPoemBtn.addEventListener('mousedown', () => {
            newPoemBtn.style.transform = 'translateY(2px) scale(0.98)';
        });
        
        newPoemBtn.addEventListener('mouseup', () => {
            newPoemBtn.style.transform = 'translateY(-5px)';
        });
        
        newPoemBtn.addEventListener('mouseleave', () => {
            newPoemBtn.style.transform = 'translateY(0)';
        });
        
        // عرض شعر عشوائي مع حركة ناعمة
        function displayRandomPoem() {
            // إخفاء الأسطر الحالية بسلاسة
            const lines = poemBox.querySelectorAll('.poem-line');
            lines.forEach((line, index) => {
                line.style.opacity = '0';
                line.style.transform = 'translateY(30px)';
                setTimeout(() => {
                    line.remove();
                }, 500);
            });
            
            // اختيار شعر عشوائي
            const randomIndex = Math.floor(Math.random() * poems.length);
            const selectedPoem = poems[randomIndex];
            
            // إضافة الأسطر الجديدة مع حركة ظهور تدريجي
            setTimeout(() => {
                poemBox.innerHTML = '';
                
                selectedPoem.forEach((line, index) => {
                    const p = document.createElement('p');
                    p.classList.add('poem-line');
                    p.textContent = line;
                    p.style.setProperty('--line-index', index);
                    poemBox.appendChild(p);
                    
                    // تأخير ظهور كل سطر
                    setTimeout(() => {
                        p.classList.add('show');
                    }, 200 * (index + 1));
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
