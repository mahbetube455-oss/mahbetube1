<!DOCTYPE html>
<html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ማሕቤ ቢዝነስ ማዕከል | Mahbe Business Center</title>
    
    <meta name="google-site-verification" content="FOyAAyP1C_fV915SCmpDu0ktm9u8eZsIQUMRgB07Sb0" />

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --blue: #004e92;
            --yellow: #f7e017;
            --dark-card: #1e272e;
            --white: #ffffff;
        }

        body { font-family: 'Segoe UI', sans-serif; margin: 0; background-color: #f4f7f6; color: #333; }

        header {
            background: var(--white); padding: 10px 5%; display: flex; 
            justify-content: space-between; align-items: center;
            position: fixed; width: 90%; top: 0; z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1); border-bottom: 3px solid var(--blue);
        }
        .logo-area { display: flex; align-items: center; gap: 8px; }
        .logo-img { height: 40px; width: 40px; border-radius: 50%; border: 2px solid var(--blue); object-fit: cover; }
        .logo-text { font-weight: bold; color: var(--blue); font-size: 1rem; }

        nav { display: flex; gap: 10px; }
        nav a { color: #333; text-decoration: none; font-weight: bold; font-size: 0.8rem; cursor: pointer; padding: 5px; }
        nav a:hover, nav a.active { color: var(--blue); border-bottom: 2px solid var(--yellow); }

        .content-section { display: none; padding: 100px 5% 40px; animation: fadeIn 0.5s ease; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

        .hero { background: var(--blue); color: white; padding: 50px 20px; text-align: center; border-radius: 20px; }
        .social-links { display: flex; justify-content: center; gap: 15px; margin-top: 20px; }
        .social-links a { 
            color: white; font-size: 1.5rem; transition: 0.3s; 
            background: rgba(255,255,255,0.1); width: 45px; height: 45px; 
            display: flex; align-items: center; justify-content: center; border-radius: 50%;
            text-decoration: none;
        }
        .social-links a:hover { transform: scale(1.2); background: var(--yellow); color: var(--blue); }

        .testimonial { background: white; color: #333; padding: 25px; border-radius: 15px; border-left: 8px solid var(--yellow); margin-top: 30px; box-shadow: 0 4px 15px rgba(0,0,0,0.05); }

        .service-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; margin-top: 30px; }
        .service-card {
            background: var(--dark-card); color: white; padding: 30px 20px; border-radius: 25px;
            text-align: center; transition: 0.6s; border-bottom: 5px solid var(--yellow);
            opacity: 0; transform: translateY(30px);
        }
        .service-card.show { opacity: 1; transform: translateY(0); }
        .order-btn {
            display: inline-block; background: var(--yellow); color: var(--blue);
            padding: 10px 25px; border-radius: 50px; text-decoration: none;
            font-weight: bold; margin-top: 20px; transition: 0.3s;
        }

        .gallery-grid { 
            display: grid; 
            grid-template-columns: repeat(auto-fill, minmax(140px, 1fr)); 
            gap: 10px; 
        }
        .gallery-item img { 
            width: 100%; height: 140px; border-radius: 8px; 
            object-fit: contain; background: #eee; cursor: zoom-in; transition: 0.3s; 
        }
        .gallery-item img:hover { transform: scale(1.05); }

        #lightbox {
            position: fixed; z-index: 2000; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.9); display: none; justify-content: center; align-items: center;
        }
        #lightbox img { max-width: 95%; max-height: 90%; object-fit: contain; }
        #lightbox.active { display: flex; }

ዘ-ዓምደ ሥላሴ, [1/3/2026 2:15 AM]
footer { text-align: center; padding: 30px; font-size: 0.85rem; border-top: 1px solid #ddd; background: white; margin-top: 50px; }
    </style>
</head>
<body>

    <div id="lightbox" onclick="this.classList.remove('active')"><img src=""></div>

    <header>
        <div class="logo-area">
            <img src="https://i.ibb.co/Mk7dRNR1/IMG-20260102-205355-990.png" class="logo-img">
            <span class="logo-text">ማሕቤ</span>
        </div>
        <nav>
            <a onclick="showSection('home', this)" class="active">Home</a>
            <a onclick="showSection('services', this)">Service</a>
            <a onclick="showSection('gallery', this)">Gallery</a>
            <a onclick="showSection('about', this)">About</a>
            <a onclick="showSection('comment', this)">Comment</a>
        </nav>
    </header>

    <div id="home" class="content-section" style="display: block;">
        <div class="hero">
            <img src="https://i.ibb.co/Mk7dRNR1/IMG-20260102-205355-990.png" style="width:100px; border-radius:50%; border:3px solid var(--yellow);">
            <h1>ማሕቤ ቢዝነስ ሴንተር</h1>
            <p>ጥራት ያለው አገልግሎት የእኛ መለያ ነው!</p>
            <div class="social-links">
                <a href="https://t.me/Mahbe_4"><i class="fab fa-telegram-plane"></i></a>
                <a href="https://www.tiktok.com/@mahbe_media"><i class="fab fa-tiktok"></i></a>
                <a href="#"><i class="fab fa-youtube"></i></a>
                <a href="https://instagram.com/mahbe_media"><i class="fab fa-instagram"></i></a>
            </div>
        </div>
        <div class="testimonial">
            <p>"በጣም የሚገርም እና ደስ የሚል ስራ ነው ከፍጥነታችሁ ጥራታችሁ እኔ ሲፈጥን እንደዚህ ጥራት ይኖረዋል ብየ አልጠበኩም"</p>
            <p style="text-align: right; font-weight: bold; color: var(--blue);">— ከአንዲት ደንበኛ ⭐⭐⭐⭐⭐</p>
        </div>
    </div>

    <div id="services" class="content-section">
        <h2 style="text-align: center; color: var(--blue);">የምንሰጣቸው አገልግሎቶች</h2>
        <div class="service-grid">
            <div class="service-card">
                <i class="fas fa-palette" style="font-size: 2.5rem; color: var(--yellow); margin-bottom: 15px;"></i>
                <h3>ግራፊክስ ዲዛይን</h3>
                <p>ሎጎ፣ ባነር፣ መጽሐፍ ዲዛይን እና ለማህበራዊ ሚዲያ ማስታወቂያዎች በጥራት እናቀርባለን።</p>
                <a href="https://t.me/temu_amen" class="order-btn">አሁኑኑ ይዘዙ</a>
            </div>
            <div class="service-card">
                <i class="fas fa-video" style="font-size: 2.5rem; color: var(--yellow); margin-bottom: 15px;"></i>
                <h3>ቪዲዮ ኤዲቲንግ</h3>
                <p>ለYouTube፣ TikTok እና ለተለያዩ ፕሮግራሞች የሚሆኑ ቪዲዮዎችን በዘመናዊ ጥበብ ኤዲት እናደርጋለን።</p>
                <a href="https://t.me/temu_amen" class="order-btn">አሁኑኑ ይዘዙ</a>
            </div>
            <div class="service-card">
                <i class="fas fa-print" style="font-size: 2.5rem; color: var(--yellow); margin-bottom: 15px;"></i>
                <h3>የሕትመት ስራዎች</h3>
                <p>ማንኛውንም የሕትመት ውጤቶች በጥራት እና በታማኝነት ለደንበኞቻችን እናቀርባለን።</p>
                <a href="https://t.me/temu_amen" class="order-btn">አሁኑኑ ይዘዙ</a>
            </div>
        </div>
    </div>

    <div id="gallery" class="content-section">
        <h2 style="text-align: center; color: var(--blue);">የስራዎቻችን ማሳያ</h2>
        <div class="gallery-grid">
            <div class="gallery-item"><img src="https://i.ibb.co/zhjkJXpm/20251219-224720.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/1fwpFk6H/20251216-002122.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/QF7PbLyj/20251215-155642.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/XN9qjfN/20251210-224030.jpg" onclick="zoomImg(this)"></div>
<div class="gallery-item"><img src="https://i.ibb.co/pj0G79js/20251210-225324.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/PZBYcCN3/20251209-234129.jpg" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/PsqD4xFT/20251202-120100.jpg" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/LLrvHzJ/20251205-104728.jpg" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/fYH5CVpV/20251128-093307.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/fzPz8G2s/20251127-100038.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/zTn3fYKp/20260102-164217.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/qMk0cqCf/20251230-112306.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/qLhqKJWR/20251230-073553.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/8nwp8rkQ/20251219-132621.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/LzZCXn0y/20251205-122512.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/5XVVtK0q/20251122-144552.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/LhnMBPNF/20251120-202649.jpg" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/YB2q959t/20251120-200348.jpg" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/HTs32qzY/20251119-140559.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/v7RQtHD/20251118-215305.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/WNFRQj2H/20251118-200618.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/d0KmLtSN/20251114-122726.jpg" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/FLLpDNv5/20251108-122343.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/d46N12Ms/20251109-184251.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/3yv4bm2Z/20251023-182429.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/vgz9sgX/20251005-123849.png" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/r2JxTnM2/20251003-164027.jpg" onclick="zoomImg(this)"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/21dLh2P5/20251106-082659.jpg" onclick="zoomImg(this)"></div>
        </div>
    </div>

    <div id="about" class="content-section">
        <h2 style="color: var(--blue);">ስለ ማሕቤ (About)</h2>
        <div style="background:white; padding:25px; border-radius:15px; line-height:1.8; box-shadow: 0 4px 10px rgba(0,0,0,0.05);">
            <p><strong>ማሕቤ</strong> ማለት ሁለት ታላላቅ ትርጉሞች ያሉት ጥልቅ ስም ነው፦</p>
            <ul>
                <li><strong>ማሕፀነ ቤተክርስቲያን ሚዲያ፦</strong> መንፈሳዊ አገልግሎቶችን በዘመናዊ መንገድ የምናቀርብበት ክፍል ነው።</li>
                <li><strong>ማሕቤ ሕትመት ቤት፦</strong> የግራፊክስ ዲዛይን እና የሕትመት ስራዎች በጥራት የምንሰራበት ዘርፍ ነው።</li>
            </ul>
        </div>
    </div>

    <div id="comment" class="content-section">
        <h2 style="text-align: center; color: var(--blue);">አስተያየትዎን ያጋሩን</h2>
        <div style="max-width:500px; margin:0 auto; background:white; padding:30px; border-radius:20px;">
]
<input type="text" id="userName" placeholder="ሙሉ ስምዎ" style="width:100%; padding:12px; margin:10px 0; border:1px solid #ddd; border-radius:10px;">
            <textarea id="userComment" rows="5" placeholder="አስተያየትዎን እዚህ ይጻፉ..." style="width:100%; padding:12px; margin:10px 0; border:1px solid #ddd; border-radius:10px;"></textarea>
            <button onclick="sendToTelegram()" style="background:var(--blue); color:white; border:none; padding:15px; width:100%; border-radius:50px; cursor:pointer;">አስተያየቴን ላክ</button>
        </div>
    </div>

    <footer>
        <p>© 2026 ማሕቤ ቢዝነስ ማዕከል | 📞 0928525029 / 0971825151</p>
    </footer>

    <script>
        function showSection(id, element) {
            const sections = document.querySelectorAll('.content-section');
            sections.forEach(s => s.style.display = 'none');
            document.getElementById(id).style.display = 'block';
            const navLinks = document.querySelectorAll('nav a');
            navLinks.forEach(link => link.classList.remove('active'));
            element.classList.add('active');
            if(id === 'services') {
                document.querySelectorAll('.service-card').forEach(card => card.classList.add('show'));
            }
        }
        function zoomImg(img) {
            const lb = document.getElementById('lightbox');
            lb.querySelector('img').src = img.src;
            lb.classList.add('active');
        }
        function sendToTelegram() {
            const name = document.getElementById('userName').value;
            const comment = document.getElementById('userComment').value;
            if (name === "" || comment === "") { alert("እባክዎ ስም እና አስተያየት ያስገቡ!"); return; }
            window.open(https://t.me/temu_amen?text=ስም፦ ${name}%0Aአስተያየት፦ ${comment}, '_blank');
        }
    </script>
</body>
</html>
