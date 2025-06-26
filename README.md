<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>من قلبي إلچ - هدية رومانسية</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Tajawal', sans-serif;
            background: linear-gradient(135deg, #ffe6f0, #fff0f5);
            color: #444;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
            line-height: 1.6;
        }
        
        .container {
            max-width: 800px;
            width: 100%;
            text-align: center;
            padding: 30px;
        }
        
        .heart-icon {
            font-size: 1.8rem;
            color: #fca5b0;
            margin-bottom: 10px;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }
        
        h1 {
            font-size: 3.5rem;
            color: #6d2e46;
            margin-bottom: 30px;
            text-shadow: 0 2px 4px rgba(0,0,0,0.1);
            font-weight: 700;
        }
        
        .poem-container {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(252, 165, 176, 0.3);
            padding: 40px;
            margin: 30px 0;
            position: relative;
            min-height: 220px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            transition: all 0.5s ease;
        }
        
        .poem-container::before {
            content: "";
            position: absolute;
            top: -10px;
            left: -10px;
            right: -10px;
            bottom: -10px;
            border-radius: 30px;
            border: 2px dashed #fca5b0;
            z-index: -1;
            opacity: 0.5;
        }
        
        .poem-box {
            font-size: 1.5rem;
            line-height: 2.2;
            color: #5a3d5c;
        }
        
        .poem-line {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.8s ease, transform 0.8s ease;
        }
        
        .poem-line.show {
            opacity: 1;
            transform: translateY(0);
        }
        
        .btn-container {
            margin: 30px 0;
        }
        
        #newPoemBtn {
            background: linear-gradient(145deg, #fca5b0, #d88592);
            color: white;
            border: none;
            border-radius: 50px;
            padding: 16px 45px;
            font-size: 1.4rem;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 6px 15px rgba(252, 165, 176, 0.4);
            position: relative;
            overflow: hidden;
        }
        
        #newPoemBtn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(252, 165, 176, 0.6);
        }
        
        #newPoemBtn:active {
            transform: translateY(1px);
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
            transition: transform 0.4s ease;
        }
        
        #newPoemBtn:hover::after {
            transform: translateX(100%);
        }
        
        footer {
            margin-top: 30px;
            color: #7d5a5a;
            font-size: 1.1rem;
            padding: 15px;
            border-top: 1px solid rgba(252, 165, 176, 0.3);
            width: 100%;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .fade-in {
            animation: fadeIn 1.2s ease forwards;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.8rem;
            }
            
            .poem-container {
                padding: 25px 20px;
            }
            
            .poem-box {
                font-size: 1.3rem;
                line-height: 2.0;
            }
            
            #newPoemBtn {
                padding: 14px 35px;
                font-size: 1.2rem;
            }
        }
        
        @media (max-width: 480px) {
            h1 {
                font-size: 2.2rem;
            }
            
            .poem-box {
                font-size: 1.1rem;
                line-height: 1.8;
            }
            
            #newPoemBtn {
                padding: 12px 30px;
                font-size: 1.1rem;
            }
            
            .container {
                padding: 15px;
            }
        }
        
        /* Floating hearts */
        .heart {
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: #fca5b0;
            opacity: 0;
            pointer-events: none;
        }
        
        .heart::before, .heart::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: #fca5b0;
            border-radius: 50%;
        }
        
        .heart::before {
            top: -10px;
            left: 0;
        }
        
        .heart::after {
            top: 0;
            left: -10px;
        }
        
        @keyframes float {
            0% {
                opacity: 1;
                transform: translateY(0) rotate(0deg);
            }
            100% {
                opacity: 0;
                transform: translateY(-100px) rotate(360deg);
            }
        }
    </style>
</head>
<body>
    <div class="container fade-in">
        <div class="heart-icon">❤</div>
        <h1>من قلبي إلچ</h1>
        
        <div class="poem-container">
            <div class="poem-box" id="poemBox">
                <!-- الشعر سيتم عرضه هنا بالجافاسكريبت -->
            </div>
        </div>
        
        <div class="btn-container">
            <button id="newPoemBtn">بعد، گلبي بعد...</button>
        </div>
        
        <footer>كرار حيدر – 2025 ©</footer>
    </div>

    <script>
        // مجموعة الأشعار الرومانسية (20 شعر)
        const poems = [
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
                "فهل من لقاءٍ قريبٍ يطفئ لهيب الشوق في داخلي؟"
            ],
            [
                "حبكِ في قلبي كالورد في البستان",
                "ينمو ويزدهر مع كل نفسٍ أتنفسه",
                "فكوني لي كما الندى للورد",
                "أكون لكِ كالبستان الذي يحمي الورد من حر الصيف"
            ],
            [
                "أحبكِ.. كلمتان خفيفتان على اللسان",
                "ولكنهما تزنان في قلبي الجبال",
                "أحبكِ.. هي نغمةٌ أعزفها كل صباح",
                "لأبدأ يومي بابتسامةٍ وفرحٍ وأملٍ لا يضاهى"
            ],
            [
                "لو أن البحرَ مدادٌ والقلمُ من الريحان",
                "والنجومُ كلماتٌ والكونُ صفحاتٌ",
                "ما كتبتْ كفايةً عن حبكِ يا سيدتي",
                "فحبكِ أكبر من أن يحويه كتابٌ أو يصفه بيان"
            ],
            [
                "يا حبيبتي، أنتِ النور في ظلماتي",
                "والسكن في وحشتي، والأمل في همومي",
                "لكِ في قلبي مكانٌ لا يُقاس",
                "ولكِ في روحي حضورٌ لا يزول"
            ],
            [
                "كلما ابتعدتِ زاد اشتياقي",
                "وكلما اقتربتِ ازداد هيامي",
                "فأنتِ يا حياتي كل شيءٍ",
                "ولولاكِ ما عرفت معنى الحياة"
            ],
            [
                "أرسمُ اسمكِ على جنبات قلبي",
                "وأكتبُ حبكِ في كل نبضةٍ من نبضاتي",
                "فأنتِ الحلم الذي طالما انتظرته",
                "وأنتِ الحب الذي طالما حلمت به"
            ],
            [
                "في ليل البعدِ، يا قمرَ حياتي",
                "أبحثُ عنكِ بين النجومِ الساطعة",
                "فأراكِ في كل نجمةٍ تتلألأ",
                "وأسمعُ همسكِ في كل نسيمٍ هفهاف"
            ],
            [
                "يا حبيبتي، كم أشتاق لرؤياكِ",
                "ولسماعِ صوتكِ كالموسيقى في أذني",
                "أشتاق لضحكتكِ كالربيعِ الزاهر",
                "أشتاق لكل شيءٍ فيكِ، فهل من لقاء؟"
            ],
            [
                "حبي لكِ يا حياتي بحرٌ لا ساحل له",
                "وسحابٌ لا ينضبُ ماؤه أبداً",
                "فهل تقبلين هذا الحبَّ العظيم؟",
                "وهل تسمحين له أن يكون مأواكِ للأبد؟"
            ],
            [
                "في قلبي سراديبُ من الأشواق",
                "تتحدث عنكِ في صمت الليالي",
                "وتهمسُ باسمكِ في كل حين",
                "فهل تسمعين همس قلبي إليكِ؟"
            ],
            [
                "أحبكِ أكثر من كل الكلمات",
                "وأكثر من كل النجوم في السما",
                "وأكثر من كل الأيام التي مضت",
                "وأكثر من كل الأيام التي ستأتي"
            ],
            [
                "أنتِ النور الذي يضيء دربي",
                "والماء الذي يروي ظمأ روحي",
                "أنتِ الحب الذي يملأ قلبي",
                "وأنتِ الحياة التي أعيشها"
            ],
            [
                "يا حبيبتي، أنتِ أغلى من الدرر",
                "وأثمن من كل الكنوز في الوجود",
                "فأنتِ نعمةٌ من الله لا تُقدر بثمن",
                "وحبكِ هديةٌ لا تعوض"
            ],
            [
                "أراكِ في كل زهرةٍ تتفتح",
                "وفي كل نجمةٍ تتلألأ في السماء",
                "أراكِ في ضياء القمر",
                "وفي دفء الشمس في الصباح"
            ],
            [
                "حبي لكِ يا حياتي بحرٌ عميق",
                "لا يعرف حدوداً ولا شواطئ",
                "فهل تقبلين أن تكوني سفينتي؟",
                "وأكون بحاركِ في هذا البحر الواسع"
            ],
            [
                "أشتاق إليكِ كما يشتاق الطفل لأمه",
                "وكما يشتاق المسافر لموطنه",
                "أشتاق إلى دفءِ حضوركِ",
                "وإلى رائحتكِ التي تملأ كل مكان"
            ],
            [
                "يا حبيبتي، أنتِ القصيدة التي لا تنتهي",
                "واللوحة التي لا تكتمل",
                "أنتِ الحلم الذي لا يزول",
                "وأنتِ الحب الذي لا ينتهي"
            ],
            [
                "في عينيكِ رأيتُ الكونَ كله",
                "ورأيتُ مستقبلي وحاضري وماضيي",
                "فلا تبتعدي عني أبداً",
                "فأنتِ كل شيءٍ في حياتي"
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
                }, i * 200);
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
