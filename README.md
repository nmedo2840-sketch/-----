<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<meta name="theme-color" content="#030303">

<title>Gharably Integrated Engineering Co. S.A.E</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:'Inter',sans-serif;
    background:#030303;
    color:#fff;
    overflow-x:hidden;
}

/* ================= BACKGROUND ================= */

body::before{
    content:"";
    position:fixed;
    inset:0;
    background:
    radial-gradient(circle at top right, rgba(0,153,255,0.18), transparent 30%),
    radial-gradient(circle at bottom left, rgba(255,183,0,0.15), transparent 35%),
    #030303;
    z-index:-3;
}

body::after{
    content:"";
    position:fixed;
    inset:0;
    background:url('https://res.cloudinary.com/dq9azsujw/image/upload/q_auto/f_auto/v1778232585/c439c687-293b-42e4-a8c3-f2530deddbd6.png') center/cover no-repeat;
    opacity:0.12;
    z-index:-2;
}

/* ================= HEADER ================= */

header{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    padding:18px 5%;
    display:flex;
    justify-content:space-between;
    align-items:center;
    z-index:999;
    backdrop-filter:blur(14px);
    background:rgba(0,0,0,0.45);
    border-bottom:1px solid rgba(255,255,255,0.08);
    flex-wrap:wrap;
    gap:15px;
}

.logo{
    display:flex;
    align-items:center;
    gap:15px;
}

.logo img{
    height:65px;
}

.logo-text{
    font-family:'Cinzel',serif;
    letter-spacing:2px;
    font-size:20px;
}

nav{
    display:flex;
    gap:35px;
}

nav a{
    color:#fff;
    text-decoration:none;
    font-size:14px;
    letter-spacing:2px;
    transition:0.4s;
    position:relative;
}

nav a::after{
    content:"";
    position:absolute;
    left:0;
    bottom:-8px;
    width:0;
    height:1px;
    background:#d4af37;
    transition:0.4s;
}

nav a:hover{
    color:#d4af37;
}

nav a:hover::after{
    width:100%;
}

/* ================= HERO ================= */

.hero{
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:120px 30px;
    position:relative;
}

.hero-content{
    max-width:1100px;
}

.hero h1{
    font-family:'Cinzel',serif;
    font-size:clamp(38px,8vw,90px);
    letter-spacing:clamp(2px,1vw,10px);
    line-height:1.15;
    margin-bottom:25px;
    text-shadow:0 0 30px rgba(255,255,255,0.12);
}

.hero p{
    font-size:clamp(15px,2vw,20px);
    line-height:1.9;
    color:#d9d9d9;
    max-width:900px;
    margin:auto;
}

.hero-buttons{
    margin-top:50px;
    display:flex;
    justify-content:center;
    gap:25px;
    flex-wrap:wrap;
}

.hero-buttons a{
    padding:18px 40px;
    border-radius:50px;
    text-decoration:none;
    font-size:14px;
    letter-spacing:2px;
    transition:0.4s;
}

.primary-btn{
    background:linear-gradient(135deg,#d4af37,#f5d76e);
    color:#000;
    font-weight:700;
}

.primary-btn:hover{
    transform:translateY(-6px);
    box-shadow:0 20px 40px rgba(212,175,55,0.3);
}

.secondary-btn{
    border:1px solid rgba(255,255,255,0.2);
    color:#fff;
    backdrop-filter:blur(10px);
    background:rgba(255,255,255,0.04);
}

.secondary-btn:hover{
    background:rgba(255,255,255,0.08);
    transform:translateY(-6px);
}

/* ================= SECTION ================= */

.section{
    padding:120px 5%;
}

.section-title{
    text-align:center;
    margin-bottom:80px;
}

.section-title h2{
    font-family:'Cinzel',serif;
    font-size:60px;
    letter-spacing:5px;
    margin-bottom:20px;
}

.section-title p{
    color:#bbb;
    font-size:18px;
}

/* ================= CARDS ================= */

.cards{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
    gap:35px;
}

.card{
    position:relative;
    overflow:hidden;
    border-radius:28px;
    min-height:550px;
    background:rgba(255,255,255,0.04);
    border:1px solid rgba(255,255,255,0.08);
    backdrop-filter:blur(18px);
    transition:0.5s;
}

.card:hover{
    transform:translateY(-15px) scale(1.02);
    box-shadow:0 40px 60px rgba(0,0,0,0.45);
}

.card-image{
    position:absolute;
    inset:0;
    width:100%;
    height:100%;
    object-fit:cover;
    opacity:0.35;
    transition:0.5s;
}

.card:hover .card-image{
    transform:scale(1.1);
    opacity:0.5;
}

.card-overlay{
    position:absolute;
    inset:0;
    background:linear-gradient(to top, rgba(0,0,0,0.92), rgba(0,0,0,0.2));
}

.card-content{
    position:relative;
    z-index:2;
    height:100%;
    display:flex;
    flex-direction:column;
    justify-content:flex-end;
    padding:40px;
}

.card-tag{
    display:inline-block;
    padding:10px 18px;
    border-radius:50px;
    background:rgba(212,175,55,0.15);
    border:1px solid rgba(212,175,55,0.4);
    color:#f5d76e;
    font-size:12px;
    letter-spacing:2px;
    margin-bottom:20px;
    width:max-content;
}

.card h3{
    font-family:'Cinzel',serif;
    font-size:45px;
    line-height:1.2;
    margin-bottom:20px;
}

.card p{
    color:#d5d5d5;
    line-height:1.9;
    margin-bottom:35px;
}

.card-buttons{
    display:flex;
    gap:18px;
    flex-wrap:wrap;
}

.card-buttons a{
    padding:15px 25px;
    border-radius:50px;
    text-decoration:none;
    font-size:13px;
    letter-spacing:2px;
    transition:0.4s;
}

.enter-btn{
    background:#d4af37;
    color:#000;
    font-weight:700;
}

.enter-btn:hover{
    background:#fff;
}

.details-btn{
    border:1px solid rgba(255,255,255,0.2);
    color:#fff;
    background:rgba(255,255,255,0.05);
}

.details-btn:hover{
    background:rgba(255,255,255,0.12);
}

/* ================= STATS ================= */

.stats{
    margin-top:100px;
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:25px;
}

.stat-box{
    padding:40px 30px;
    border-radius:25px;
    background:rgba(255,255,255,0.04);
    border:1px solid rgba(255,255,255,0.08);
    text-align:center;
    backdrop-filter:blur(12px);
}

.stat-box h3{
    font-size:55px;
    color:#d4af37;
    margin-bottom:10px;
}

.stat-box p{
    letter-spacing:2px;
    color:#ccc;
}

/* ================= FOOTER ================= */

footer{
    padding:60px 30px;
    text-align:center;
    border-top:1px solid rgba(255,255,255,0.08);
    background:rgba(0,0,0,0.4);
    margin-top:100px;
}

footer h2{
    font-family:'Cinzel',serif;
    font-size:35px;
    margin-bottom:15px;
}

footer p{
    color:#aaa;
}

/* ================= RESPONSIVE ================= */

@media(max-width:992px){

.hero{
    padding-top:180px;
}

.hero-buttons{
    gap:15px;
}

.card h3{
    font-size:34px;
}

.section-title h2{
    font-size:42px;
}

}

@media(max-width:768px){

header{
    justify-content:center;
    text-align:center;
}

.logo{
    justify-content:center;
    width:100%;
}

nav{
    width:100%;
    justify-content:center;
    flex-wrap:wrap;
    gap:18px;
}

.hero{
    padding:170px 20px 100px;
}

.hero-buttons{
    flex-direction:column;
    align-items:center;
}

.hero-buttons a{
    width:100%;
    max-width:320px;
    text-align:center;
}

.card{
    min-height:500px;
}

.card-content{
    padding:30px;
}

.section-title h2{
    font-size:34px;
}

.stat-box h3{
    font-size:42px;
}

}

@media(max-width:480px){

.logo img{
    height:52px;
}

.logo-text{
    display:none;
}

nav a{
    font-size:11px;
    letter-spacing:1px;
}

.card h3{
    font-size:28px;
}

.card p{
    font-size:14px;
}

.card-buttons{
    flex-direction:column;
}

.card-buttons a{
    text-align:center;
}

.stat-box{
    padding:30px 20px;
}

}

</style>

</head>

<body>

<header>

    <div class="logo">

        <img src="https://res.cloudinary.com/dq9azsujw/image/upload/q_auto/f_auto/v1778313725/0a6ab990-c1a3-4d6f-819b-13921d6d914f.png">

        <div class="logo-text">
            Gharably Integrated Engineering Co. S.A.E
        </div>

    </div>

    <nav>
        <a href="#home">HOME</a>
        <a href="#warehouses">WAREHOUSES</a>
        <a href="#contact">CONTACT</a>
    </nav>

</header>

<section class="hero" id="home">

    <div class="hero-content">

        <h1>
            Strong inventory management means fewer problems and faster work
            <br>
            Efficiency starts from the warehouse
        </h1>

        <p>
            Premium warehouse management experience combining smart inventory control,
            industrial supply operations, and advanced storage systems through
            Gharably Integrated Engineering Co. S.A.E digital platform
        </p>

        <div class="hero-buttons">

            <a href="#warehouses" class="primary-btn">
                ENTER NETWORK
            </a>

            <a href="#contact" class="secondary-btn">
                CONTACT DIVISION
            </a>

        </div>

    </div>

</section>

<section class="section" id="warehouses">

    <div class="section-title">

        <h2>WAREHOUSE DIVISIONS</h2>

        <p>
            Professional Supply Access Portals
        </p>

    </div>

    <div class="cards">

        <!-- Plumbing -->

        <div class="card">

            <img class="card-image"
            src="https://images.unsplash.com/photo-1585704032915-c3400ca199e7?q=80&w=1932&auto=format&fit=crop">

            <div class="card-overlay"></div>

            <div class="card-content">

                <div class="card-tag">
                    INDUSTRIAL SYSTEMS
                </div>

                <h3>
                    PLUMBING
                    <br>
                    WAREHOUSE
                </h3>

                <p>
                    Advanced plumbing inventory platform featuring fittings,
                    valves, PPR systems, industrial components,
                    and structured warehouse supply management.
                </p>

                <div class="card-buttons">

                    <a class="enter-btn"
                    href="https://nmedo2840-sketch.github.io/Plumbing-warehouse/"
                    target="_blank">

                        ENTER WAREHOUSE

                    </a>

                    <a class="details-btn" href="#">
                        VIEW SYSTEM
                    </a>

                </div>

            </div>

        </div>

        <!-- Marine -->

        <div class="card">

            <img class="card-image"
            src="https://images.unsplash.com/photo-1500375592092-40eb2168fd21?q=80&w=1974&auto=format&fit=crop">

            <div class="card-overlay"></div>

            <div class="card-content">

                <div class="card-tag">
                    MARINE PRODUCTION
                </div>

                <h3>
                    MARINE
                    <br>
                    DIVISION
                </h3>

                <p>
                    Integrated marine production and offshore logistics division designed
                    for operational tracking, supply coordination,
                    and heavy-duty industrial workflows.
                </p>

                <div class="card-buttons">

                    <a class="enter-btn"
                    href="https://nmedo2840-sketch.github.io/Marine--production../"
                    target="_blank">

                        ENTER DIVISION

                    </a>

                    <a class="details-btn" href="#">
                        VIEW SYSTEM
                    </a>

                </div>

            </div>

        </div>

    </div>

    <!-- STATS -->

    <div class="stats">

        <div class="stat-box">
            <h3>02</h3>
            <p>ACTIVE DIVISIONS</p>
        </div>

        <div class="stat-box">
            <h3>24/7</h3>
            <p>SUPPLY ACCESS</p>
        </div>

        <div class="stat-box">
            <h3>GLOBAL</h3>
            <p>INDUSTRIAL REACH</p>
        </div>

        <div class="stat-box">
            <h3>PREMIUM</h3>
            <p>ENTERPRISE EXPERIENCE</p>
        </div>

    </div>

</section>

<footer id="contact">

    <h2>
        Gharably Integrated Engineering Co. S.A.E
    </h2>

    <p>
        Enterprise Industrial Marketplace Experience
    </p>

</footer>

</body>
</html>
