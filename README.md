<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>نت كافيه السرايا - جيمينج | استريم | بلايستيشن</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700;900&display=swap');
        
        :root {
            --primary: #6e00ff;
            --secondary: #ff00a0;
            --dark: #0a0a1a;
            --light: #f0f0ff;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Tajawal', sans-serif;
        }
        
        body {
            background-color: var(--dark);
            color: var(--light);
            background-image: 
                radial-gradient(circle at 20% 30%, rgba(110, 0, 255, 0.15) 0%, transparent 30%),
                radial-gradient(circle at 80% 70%, rgba(255, 0, 160, 0.15) 0%, transparent 30%);
            overflow-x: hidden;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            padding: 1rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .logo {
            font-size: 2.5rem;
            font-weight: 900;
            margin-bottom: 0.5rem;
            text-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
            background: linear-gradient(to right, #fff, #ccc);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .tagline {
            font-size: 1.2rem;
            opacity: 0.9;
        }
        
        nav {
            display: flex;
            justify-content: center;
            background-color: rgba(10, 10, 26, 0.8);
            padding: 1rem;
            gap: 2rem;
            flex-wrap: wrap;
        }
        
        nav a {
            color: var(--light);
            text-decoration: none;
            font-weight: bold;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            transition: all 0.3s;
        }
        
        nav a:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }
        
        .hero {
            height: 60vh;
            background: 
                linear-gradient(rgba(10, 10, 26, 0.7), rgba(10, 10, 26, 0.9)),
                url('https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 2rem;
            position: relative;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin-bottom: 2rem;
        }
        
        .btn {
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            color: white;
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            box-shadow: 0 5px 15px rgba(110, 0, 255, 0.4);
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(110, 0, 255, 0.6);
        }
        
        .services {
            padding: 4rem 2rem;
            text-align: center;
        }
        
        .section-title {
            font-size: 2.5rem;
            margin-bottom: 3rem;
            position: relative;
            display: inline-block;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            border-radius: 2px;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .service-card {
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 2rem;
            transition: all 0.3s;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(110, 0, 255, 0.2);
            border-color: var(--primary);
        }
        
        .service-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        /* أنماط جدول الأسعار */
        .pricing {
            padding: 4rem 2rem;
            text-align: center;
            background-color: rgba(255, 255, 255, 0.03);
        }
        
        .pricing-table {
            max-width: 800px;
            margin: 2rem auto;
            border-collapse: collapse;
            width: 100%;
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .pricing-table th, .pricing-table td {
            padding: 1.2rem;
            text-align: center;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .pricing-table th {
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            color: white;
            font-weight: bold;
            font-size: 1.1rem;
        }
        
        .pricing-table tr:last-child td {
            border-bottom: none;
        }
        
        .pricing-table tr:hover {
            background-color: rgba(110, 0, 255, 0.1);
        }
        
        .price {
            font-weight: bold;
            font-size: 1.2rem;
            color: var(--secondary);
        }
        
        .discount-badge {
            background-color: #00ffaa;
            color: var(--dark);
            padding: 0.3rem 0.8rem;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: bold;
            margin-right: 0.5rem;
        }
        
        .contact {
            padding: 4rem 2rem;
            background-color: rgba(10, 10, 26, 0.8);
            text-align: center;
        }
        
        .contact-info {
            margin-top: 2rem;
            font-size: 1.2rem;
            line-height: 2;
        }
        
        footer {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            padding: 2rem;
            text-align: center;
            font-weight: bold;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 1rem;
        }
        
        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            transform: translateY(-5px);
        }
        
        /* تأثيرات الجيمينج */
        .gaming-effect {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: -1;
        }
        
        .pixel {
            position: absolute;
            width: 2px;
            height: 2px;
            background-color: var(--primary);
            opacity: 0;
            animation: float 5s infinite;
        }
        
        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) rotate(360deg);
                opacity: 0;
            }
        }
        
        /* تصميم متجاوب */
        @media (max-width: 768px) {
            .logo {
                font-size: 2rem;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            nav {
                gap: 1rem;
            }
            
            .pricing-table {
                font-size: 0.9rem;
            }
            
            .pricing-table th, .pricing-table td {
                padding: 0.8rem;
            }
        }
    </style>
</head>
<body>
    <!-- تأثيرات الجيمينج -->
    <div class="gaming-effect" id="gamingEffect"></div>
    
    <header>
        <div class="logo">السرايا للجيمينج</div>
        <div class="tagline">عالم من الألعاب والترفيه</div>
    </header>
    
    <nav>
        <a href="#home">الرئيسية</a>
        <a href="#services">خدماتنا</a>
        <a href="#prices">الأسعار</a>
        <a href="#contact">اتصل بنا</a>
    </nav>
    
    <section class="hero" id="home">
        <h1>نت كافيه السرايا للجيمينج</h1>
        <p>أفضل مكان لمحبي الألعاب والاستريمينج، أحدث أجهزة البلايستيشن، سرعة إنترنت فائقة، جو تنافسي ممتع</p>
        <a href="#contact" class="btn">احجز مكانك الآن</a>
    </section>
    
    <section class="services" id="services">
        <h2 class="section-title">خدماتنا</h2>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">🎮</div>
                <h3>جيمينج</h3>
                <p>أحدث أجهزة الجيمينج بمواصفات عالية لتحقيق أفضل تجربة لعب</p>
            </div>
            <div class="service-card">
                <div class="service-icon">📹</div>
                <h3>استريم</h3>
                <p>غرف مخصصة للاستريمينج مجهزة بأفضل التقنيات</p>
            </div>
            <div class="service-card">
                <div class="service-icon">🎯</div>
                <h3>بلايستيشن 5</h3>
                <p>أحدث إصدارات أجهزة البلايستيشن مع جميع الألعاب</p>
            </div>
        </div>
    </section>
    
    <section class="pricing" id="prices">
        <h2 class="section-title">تعرفة الأسعار</h2>
        
        <table class="pricing-table">
            <thead>
                <tr>
                    <th>الخدمة</th>
                    <th>السعر (ساعة)</th>
                    <th>خصومات المجموعات</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>أجهزة الكمبيوتر (PC)</td>
                    <td class="price">30 جنيه</td>
                    <td>5 ساعات بـ 90 جنيه </td>
                </tr>
                <tr>
                    <td>البلايستيشن (PS5)</td>
                    <td class="price">35 جنيه</td>
                    <td>5 ساعات بـ 150 جنيه</td>
                </tr>
                <tr>
                    <td>غرف الاستريم</td>
                    <td class="price">150 جنيه</td>
                    <td>حزمة 3 ساعات بـ 400 جنيه</td>
                </tr>
            </tbody>
        </table>
        
        <div style="margin-top: 2rem; background: rgba(110, 0, 255, 0.1); padding: 1.5rem; border-radius: 10px; max-width: 800px; margin-left: auto; margin-right: auto;">
            <h3 style="margin-bottom: 1rem; color: var(--secondary);">عروض خاصة!</h3>
           
            </p>
            <p style="margin-top: 0.8rem;">
                <span class="discount-badge">جديد</span>
                اشترِ أي 5 ساعات واحصل على ساعة مجانية!
            </p>
        </div>
    </section>
    
    <section class="contact" id="contact">
        <h2 class="section-title">اتصل بنا</h2>
        <div class="contact-info">
            <p><strong>العنوان:</strong> ٣٩ شارع الشيخ ريحان، وسط البلد</p>
            <p><strong>الهاتف:</strong> 01021977645</p>
            <p><strong>ساعات العمل:</strong> يومياً من 10 صباحاً حتى 2 بعد منتصف الليل</p>
        </div>
        <a href="tel:01021977645" class="btn">اتصل الآن</a>
        
        <div class="social-links">
            <a href="#" title="فيسبوك">📘</a>
            <a href="#" title="إنستجرام">📷</a>
            <a href="#" title="تويتر">🐦</a>
            <a href="#" title="واتساب">📱</a>
        </div>
    </section>
    
    <footer>
        <p>© 2023 نت كافيه السرايا للجيمينج - جميع الحقوق محفوظة</p>
    </footer>
    
    <script>
        // إنشاء تأثيرات الجيمينج (بكسلات عائمة)
        const gamingEffect = document.getElementById('gamingEffect');
        
        function createPixels() {
            for (let i = 0; i < 50; i++) {
                const pixel = document.createElement('div');
                pixel.classList.add('pixel');
                
                // وضع عشوائي
                pixel.style.left = Math.random() * 100 + 'vw';
                pixel.style.top = Math.random() * 100 + 'vh';
                
                // حجم وتأخير عشوائي
                const size = Math.random() * 3 + 1;
                pixel.style.width = size + 'px';
                pixel.style.height = size + 'px';
                pixel.style.animationDelay = Math.random() * 5 + 's';
                pixel.style.animationDuration = (Math.random() * 10 + 5) + 's';
                
                gamingEffect.appendChild(pixel);
            }
        }
        
        createPixels();
        
        // تغيير لون البكسلات بشكل دوري
        setInterval(() => {
            const pixels = document.querySelectorAll('.pixel');
            const colors = ['#6e00ff', '#ff00a0', '#00ffaa', '#ffcc00'];
            
            pixels.forEach(pixel => {
                const randomColor = colors[Math.floor(Math.random() * colors.length)];
                pixel.style.backgroundColor = randomColor;
            });
        }, 3000);
    </script>
</body>
</html>
