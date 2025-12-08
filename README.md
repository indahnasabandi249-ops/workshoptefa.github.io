<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Teknik Komputer & Jaringan — SMK Negeri 8 Batam</title>
  <meta name="description" content="Jurusan Teknik Komputer dan Jaringan (TKJ) — SMK Negeri 8 Batam. Tunjukkan Kualitas Jawaramu.">

  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root{
      --tkj-blue:#0b63c8;
      --tkj-red:#e0302a;
      --bg:#f6f8fb;
      --card:#ffffff;
      --muted:#6b7280;
      --glass: rgba(255,255,255,0.65);
      --radius:14px;
      --shadow: 0 10px 30px rgba(11,20,40,0.08);
      font-family: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      background:linear-gradient(180deg,var(--bg),#ffffff);
      color:#0f1724;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.5;
      scroll-behavior:smooth;
    }

    .wrap{max-width:1200px;margin:0 auto;padding:0 20px}

    /* NAVBAR */
    header.site-header{
      position:sticky;top:0;z-index:90;
      backdrop-filter: blur(8px);
      background:linear-gradient(180deg, rgba(255,255,255,0.88), rgba(255,255,255,0.78));
      border-bottom:1px solid rgba(11,20,40,0.04);
    }
    .nav{display:flex;align-items:center;justify-content:space-between;padding:12px 0}
    .brand{display:flex;align-items:center;gap:12px}
    .brand img{width:64px;height:64px;object-fit:contain;border-radius:10px;box-shadow:0 6px 18px rgba(11,20,40,0.06)}
    .brand h1{font-size:16px;margin:0}
    .brand p{margin:0;font-size:12px;color:var(--muted)}

    nav.links{display:flex;gap:10px;align-items:center}
    nav.links a{padding:8px 12px;border-radius:10px;text-decoration:none;color:inherit;font-weight:600}
    nav.links a.cta{background:linear-gradient(90deg,var(--tkj-blue),var(--tkj-red));color:#fff;box-shadow:0 8px 24px rgba(11,20,40,0.08)}
    .hamburger{display:none;padding:6px;border-radius:8px;background:transparent;border:1px solid rgba(11,20,40,0.03);font-size:18px}

    /* HERO / SLIDER */
    .hero{position:relative;overflow:hidden;border-bottom-left-radius:22px;border-bottom-right-radius:22px;margin-bottom:28px}
    .hero-wrap{position:relative;overflow:hidden}
    .slider{display:flex;width:300%;transition:transform 0.8s cubic-bezier(.2,.9,.2,1)}
    .slide{min-width:100%;display:flex;gap:28px;align-items:center;padding:44px 20px}
    .hero-left{flex:1;min-width:280px}
    .hero-right{flex:1;display:flex;justify-content:center}
    .brand-hero{display:flex;gap:14px;align-items:center;background:var(--glass);padding:8px;border-radius:12px;backdrop-filter: blur(6px)}
    .brand-hero img{width:84px;height:84px;border-radius:10px;object-fit:contain}
    .hero h2{font-size:36px;margin:12px 0 8px}
    .hero p.lead{color:var(--muted);max-width:560px}
    .cta-row{display:flex;gap:12px;margin-top:18px}
    .btn{display:inline-block;padding:12px 18px;border-radius:12px;text-decoration:none;font-weight:700}
    .btn-primary{background:linear-gradient(90deg,var(--tkj-blue),var(--tkj-red));color:#fff}
    .btn-outline{border:2px solid var(--tkj-blue);color:var(--tkj-blue);background:transparent}
    .hero-image{width:100%;max-width:560px;border-radius:12px;overflow:hidden;box-shadow:var(--shadow)}
    .hero-image img{width:100%;height:420px;object-fit:cover;display:block;transition:transform .6s ease}

    .dots{display:flex;gap:8px;position:absolute;right:24px;bottom:18px}
    .dot{width:12px;height:12px;border-radius:50%;background:rgba(11,20,40,0.12);cursor:pointer}
    .dot.active{background:linear-gradient(90deg,var(--tkj-blue),var(--tkj-red));box-shadow:0 6px 18px rgba(11,20,40,0.08)}

    /* Sections */
    section{padding:64px 0}
    h2.section-title{font-size:26px;margin:0 0 18px 0;text-align:center;color:var(--tkj-blue)}
    p.lead-muted{color:var(--muted);text-align:center;max-width:900px;margin:10px auto 34px}

    .card{background:var(--card);padding:18px;border-radius:12px;box-shadow:var(--shadow)}
    .muted{color:var(--muted)}

    /* ABOUT */
    .about-grid{display:grid;grid-template-columns:1fr 420px;gap:24px;align-items:start}
    .about-grid img{width:100%;height:260px;object-fit:cover;border-radius:12px}

    .about-cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:18px}

    /* NEWS */
    .news-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:22px}
    .news-card{background:#fff;border-radius:12px;overflow:hidden;box-shadow:0 10px 30px rgba(11,20,40,0.06);transition:transform .3s}
    .news-card:hover{transform:translateY(-8px)}
    .news-thumb{width:100%;height:180px;object-fit:cover;display:block}
    .news-body{padding:16px}

    /* SAMBUTAN */
    .sambutan-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(320px,1fr));gap:26px}
    .sambutan-card{background:#fff;border-radius:12px;overflow:hidden;box-shadow:0 10px 30px rgba(11,20,40,0.06)}
    .sambutan-img{width:100%;height:260px;object-fit:cover}
    .sambutan-content{padding:18px}

    /* FASILITAS */
    .fasilitas-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:20px}
    .fasilitas-card{background:#fff;border-radius:12px;overflow:hidden;box-shadow:0 10px 30px rgba(11,20,40,0.06)}
    .fasilitas-card img{width:100%;height:200px;object-fit:cover}
    .fasilitas-cap{padding:12px;color:var(--muted)}

    /* PRESTASI */
    .prestasi-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:20px}
    .prestasi-card{position:relative;background:#fff;border-radius:12px;overflow:hidden;box-shadow:0 10px 30px rgba(11,20,40,0.06)}
    .prestasi-card img{width:100%;height:220px;object-fit:cover}
    .prestasi-badge{position:absolute;left:14px;top:14px;background:var(--tkj-red);color:#fff;padding:8px 12px;border-radius:10px;font-weight:700}

    /* WORKSHOP / PRICING */
    .price-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(210px,1fr));gap:12px}
    .price-item{display:flex;justify-content:space-between;align-items:center;padding:12px;border-radius:10px;border:1px solid rgba(11,20,40,0.04);background:#fff}
    .price-item strong{color:var(--tkj-blue)}

    /* GALLERY */
    .gallery-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:18px}
    .gallery-card{position:relative;border-radius:12px;overflow:hidden}
    .gallery-card img{width:100%;height:200px;object-fit:cover;transition:transform .5s,filter .5s}
    .gallery-card .caption{position:absolute;left:12px;bottom:12px;background:rgba(0,0,0,0.5);color:#fff;padding:8px 12px;border-radius:8px;font-weight:700}

    .gallery-card:hover img{transform:scale(1.08);filter:brightness(.7) blur(.8px)}

    /* CONTACT */
    .contact-grid{display:grid;grid-template-columns:1fr 420px;gap:18px}
    .map-embed{width:100%;height:320px;border-radius:12px;border:0;box-shadow:0 10px 30px rgba(11,20,40,0.06)}
    form.contact-form{background:#fff;padding:18px;border-radius:12px;box-shadow:0 10px 30px rgba(11,20,40,0.06)}
    form.contact-form input, form.contact-form textarea{width:100%;padding:12px;border-radius:8px;border:1px solid #e6e9ef;margin-bottom:10px}

    /* TESTIMONI */
    .testi-wrap{display:flex;gap:12px;overflow:auto;padding-bottom:6px}
    .testi{min-width:260px;background:linear-gradient(180deg,#fff,#fbfbff);padding:14px;border-radius:12px;box-shadow:0 6px 18px rgba(11,20,40,0.04)}

    /* CTA BOTTOM */
    .cta-bottom{display:flex;justify-content:space-between;align-items:center;padding:22px;border-radius:12px;background:linear-gradient(90deg,var(--tkj-blue),var(--tkj-red));color:#fff;box-shadow:0 10px 30px rgba(11,20,40,0.12);margin:36px 0}
    .cta-bottom a{background:rgba(255,255,255,0.15);padding:10px 16px;border-radius:10px;color:#fff;text-decoration:none;font-weight:700}

    /* FOOTER */
    footer{padding:28px 0;background:#fff;border-top:1px solid rgba(11,20,40,0.04)}
    .foot-inner{display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap}
    .socials a{margin-left:8px;text-decoration:none;color:var(--muted)}

    /* small helpers & responsive */
    .center{text-align:center}
    @media (max-width:980px){
      .about-grid{grid-template-columns:1fr}
      .contact-grid{grid-template-columns:1fr}
      nav.links{display:none}
      .hamburger{display:block}
    }
    @media (max-width:640px){
      .brand img{width:52px;height:52px}
      .hero h2{font-size:28px}
      .hero-image img{height:260px}
    }
  </style>
</head>
<body>

  <header class="site-header">
    <div class="wrap nav">
      <div class="brand">
        <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgsULl5hSUAWDElBJ6xqAj3SMOgIm_9IE-55cQhMhpbtzTjm7hfBP4GS_QddflBx0hVMlZNYBeoOCm2tviQbyGsh5ruX_etcBe0nECKoTrcIKpdotvZykUWFkM6wDVXTXh9yh-NovmHFjlae-srQyL6axU8YbFspatgQxPvLLdN0c5yogEyH6xu6I3xmw/s500/1000251870-fotor-bg-remover-2025102171820.png" alt="Logo TKJ SMKN 8 Batam">
        <div>
          <h1 style="margin:0">Teknik Komputer & Jaringan</h1>
          <p class="muted" style="margin:0;font-size:12px">SMK Negeri 8 Batam</p>
        </div>
      </div>

      <nav class="links" aria-label="Main navigation">
        <a href="#tentang">Tentang</a>
        <a href="#berita">Berita</a>
        <a href="#sambutan">Sambutan</a>
        <a href="#prestasi">Prestasi</a>
        <a href="#kontak" class="cta btn-primary">Hubungi Kami</a>
      </nav>

      <button class="hamburger" aria-label="menu">☰</button>
    </div>
  </header>

  <section class="hero" aria-label="Hero TKJ">
    <div class="hero-wrap wrap">
      <div class="slider" id="heroSlider" role="region" aria-roledescription="carousel">
        <article class="slide">
          <div class="hero-left">
            <div class="brand-hero">
              <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgsULl5hSUAWDElBJ6xqAj3SMOgIm_9IE-55cQhMhpbtzTjm7hfBP4GS_QddflBx0hVMlZNYBeoOCm2tviQbyGsh5ruX_etcBe0nECKoTrcIKpdotvZykUWFkM6wDVXTXh9yh-NovmHFjlae-srQyL6axU8YbFspatgQxPvLLdN0c5yogEyH6xu6I3xmw/s500/1000251870-fotor-bg-remover-2025102171820.png" alt="Logo TKJ">
              <div>
                <div style="font-weight:800">Jurusan TKJ</div>
                <div class="muted" style="font-size:13px">Teknik Komputer & Jaringan — SMKN 8 Batam</div>
              </div>
            </div>

            <h2>Tunjukkan Kualitas Jawaramu.</h2>
            <p class="lead-muted">Program vokasi yang menyiapkan siswa menguasai jaringan, sistem komputer, dan keterampilan IT siap kerja melalui praktik industri, TEFA, dan sertifikasi.</p>

            <div class="cta-row">
              <a class="btn btn-primary" href="#daftar">Daftar Sekarang</a>
              <a class="btn btn-outline" href="#prestasi">Lihat Prestasi</a>
            </div>

            <div style="margin-top:12px;color:var(--muted);font-size:13px">
              <strong>Alamat:</strong> Kav. Bukit Melati - Sei Pelunggut, Kec. Sagulung, Batam — <strong style="color:var(--tkj-blue)">+62 819-4372-5324</strong>
            </div>
          </div>

          <div class="hero-right">
            <div class="hero-image">
              <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhr1eaIntEU_OnEa50arxuLt_rdIz69NUJL_lfv0tmULz77o1pogd5Ip-3ijROpMdWRUjkraCUwNZXVc2cKDyr_eCyEpc70q10QZ6F2cq4PA6iUW7Y2itb5HqOSEFoNswbjngzgIvdNP2o-5A-j55mq4D0XO-wRH6ePuW6WZ3eHcifnCLdua-JpLSZ8KQ/s800/WhatsApp%20Image%202025-11-26%20at%2012.20.45%20PM.jpeg" alt="Ruangan TKJ">
            </div>
          </div>
        </article>

        <article class="slide">
          <div class="hero-left">
            <div class="brand-hero">
              <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgsULl5hSUAWDElBJ6xqAj3SMOgIm_9IE-55cQhMhpbtzTjm7hfBP4GS_QddflBx0hVMlZNYBeoOCm2tviQbyGsh5ruX_etcBe0nECKoTrcIKpdotvZykUWFkM6wDVXTXh9yh-NovmHFjlae-srQyL6axU8YbFspatgQxPvLLdN0c5yogEyH6xu6I3xmw/s500/1000251870-fotor-bg-remover-2025102171820.png" alt="Logo TKJ">
              <div>
                <div style="font-weight:800">Laboratorium & TEFA</div>
                <div class="muted" style="font-size:13px">Praktik intensif & sertifikasi</div>
              </div>
            </div>

            <h2>Praktik Nyata, Siap Kerja.</h2>
            <p class="lead-muted">TEFA dan modul industri membentuk keterampilan teknis siswa — siap bekerja dan berwirausaha.</p>

            <div class="cta-row">
              <a class="btn btn-primary" href="#fasilitas">Lihat Fasilitas</a>
              <a class="btn btn-outline" href="#workshop">Workshop & Jasa</a>
            </div>
          </div>

          <div class="hero-right">
            <div class="hero-image">
              <img src="https://lh6.googleusercontent.com/yMJ3zOxhoaZP6FBmQA7jqXZERbBAKPZvhyupPUA2KFubeDOvEVzXF44YczHXHjQWQFP5tOoV8uIbxhHVnflnZOwkWrSJ2O_VCgtVzWQmIYydkA74YNWkWzshgBnsyHv5IeHvneY" alt="Laboratorium TKJ">
            </div>
          </div>
        </article>

        <article class="slide">
          <div class="hero-left">
            <div class="brand-hero">
              <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgsULl5hSUAWDElBJ6xqAj3SMOgIm_9IE-55cQhMhpbtzTjm7hfBP4GS_QddflBx0hVMlZNYBeoOCm2tviQbyGsh5ruX_etcBe0nECKoTrcIKpdotvZykUWFkM6wDVXTXh9yh-NovmHFjlae-srQyL6axU8YbFspatgQxPvLLdN0c5yogEyH6xu6I3xmw/s500/1000251870-fotor-bg-remover-2025102171820.png" alt="Logo TKJ">
              <div>
                <div style="font-weight:800">Prestasi Kreatif</div>
                <div class="muted" style="font-size:13px">Film, poster, lomba</div>
              </div>
            </div>

            <h2>Berkarya & Menang.</h2>
            <p class="lead-muted">Juara 1 Lomba Film & Poster (Sumpah Pemuda) — bukti kompetensi kreatif siswa TKJ.</p>

            <div class="cta-row">
              <a class="btn btn-primary" href="#prestasi">Lihat Prestasi</a>
              <a class="btn btn-outline" href="#kontak">Hubungi Kami</a>
            </div>
          </div>

          <div class="hero-right">
            <div class="hero-image">
              <img src="https://lh3.googleusercontent.com/h3tdm2Gsm2Wg2UC_yHcxm7ZTFjWCeBF5_HFCi6SaFaSBYIUzvAlE7tWTvTZtU6xzHVz8ZA2wVu3v3bAo1z-RLbS1CybZWXL92JSPjmqR5QpbIy_6VI1Fw7R8B5927e1Bc5Bc1crf" alt="Multimedia TKJ">
            </div>
          </div>
        </article>
      </div>

      <div class="dots" id="heroDots" aria-hidden="false">
        <div class="dot active" data-index="0" aria-label="Slide 1"></div>
        <div class="dot" data-index="1" aria-label="Slide 2"></div>
        <div class="dot" data-index="2" aria-label="Slide 3"></div>
      </div>
    </div>
  </section>

  <main>
    <section id="tentang">
      <div class="wrap">
        <h2 class="section-title">Tentang Jurusan — Teknik Komputer & Jaringan</h2>
        <p class="lead-muted">Teknik Komputer dan Jaringan (TKJ) di SMK Negeri 8 Batam berfokus pada penguasaan jaringan komputer, administrasi server, keamanan sistem, dan teknologi informasi modern. Pembelajaran menggabungkan teori & praktik intensif untuk menyiapkan lulusan yang kompeten dan siap kerja.</p>

        <div class="about-grid">
          <div>
            <div class="card about-cards">
              <div>
                <h3 style="margin-top:0">Profil Kompetensi</h3>
                <p class="muted">Siswa dibekali kemampuan instalasi, konfigurasi, pemeliharaan jaringan, administrasi server, serta troubleshooting perangkat keras & perangkat lunak.</p>
              </div>

              <div>
                <h3>Visi</h3>
                <p style="font-weight:700">Terwujudnya peserta didik Jurusan Teknik Komputer dan Jaringan yang beriman, bertakwa, sehat, tangguh, menguasai teknologi jaringan dan sistem komputer, serta memiliki jiwa profesional dan entrepreneur di bidang teknologi informasi.</p>
              </div>

              <div>
                <h3>Misi</h3>
                <ol class="muted">
                  <li>Menumbuhkan peserta didik yang beriman, bertakwa, berkarakter, dan beretika profesional dalam bidang teknologi informasi.</li>
                  <li>Melaksanakan pembelajaran berbasis kompetensi dan teknologi terkini di bidang komputer dan jaringan, sesuai kebutuhan industri.</li>
                  <li>Meningkatkan keterampilan siswa melalui kegiatan praktik, TEFA (Teaching Factory), dan sertifikasi keahlian.</li>
                  <li>Mengembangkan jiwa wirausaha dan inovasi di bidang teknologi informasi serta mendorong siswa menjadi teknisi yang kreatif dan mandiri.</li>
                  <li>Membangun kerja sama dengan dunia industri, instansi, dan lembaga sertifikasi untuk mendukung pembelajaran berbasis dunia kerja.</li>
                </ol>
              </div>

              <div>
                <h3>Tujuan</h3>
                <ol class="muted">
                  <li>Menghasilkan lulusan yang beriman, berakhlak mulia, dan memiliki kompetensi tinggi di bidang komputer dan jaringan.</li>
                  <li>Membekali peserta didik dengan kemampuan instalasi, konfigurasi, pemeliharaan, dan pengelolaan jaringan komputer sesuai standar industri.</li>
                  <li>Menyiapkan lulusan yang mampu beradaptasi dengan perkembangan teknologi dan memiliki daya saing di dunia kerja maupun dunia usaha.</li>
                  <li>Mendorong siswa memiliki jiwa wirausaha dan mampu menciptakan peluang kerja di bidang teknologi informasi.</li>
                  <li>Menjalin kemitraan berkelanjutan dengan dunia industri untuk meningkatkan kualitas pembelajaran dan penyerapan lulusan.</li>
                </ol>
              </div>
            </div>
          </div>

          <aside>
            <div class="card">
              <h3 style="margin-top:0">Sekilas TKJ</h3>
              <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhr1eaIntEU_OnEa50arxuLt_rdIz69NUJL_lfv0tmULz77o1pogd5Ip-3ijROpMdWRUjkraCUwNZXVc2cKDyr_eCyEpc70q10QZ6F2cq4PA6iUW7Y2itb5HqOSEFoNswbjngzgIvdNP2o-5A-j55mq4D0XO-wRH6ePuW6WZ3eHcifnCLdua-JpLSZ8KQ/s800/WhatsApp%20Image%202025-11-26%20at%2012.20.45%20PM.jpeg" alt="Ruangan TKJ" style="width:100%;border-radius:10px;margin-top:12px">
              <p class="muted" style="margin-top:12px">Program praktik intensif, TEFA, magang industri, dan sertifikasi menjadi fokus utama pengembangan kompetensi siswa.</p>
            </div>
          </aside>
        </div>
      </div>
    </section>

    <section id="berita">
  <div class="wrap">
    <h2 class="section-title">Berita & Kegiatan Terbaru</h2>
    <p class="lead-muted">Berita kegiatan jurusan TKJ dan prestasi siswa.</p>

    <div class="news-grid">

      <!-- Berita 1 -->
      <article class="news-card">
        <img class="news-thumb" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjg6ry3Hqly8CxV3WYt9r-YaPlQZSVFpAW34INoAdaDo0vZTiLKoVvQsgi-jbZL-dUFepKzmuVMHA3mLM693R8sGaytUAiu8JBiFxqx8GfY9xyF6EfKUCUdMNf5ypphUQ_YSWQrFrJqKtYqoqs7ANV_xoPhZDnBltsZk0nh3oJo7aV5u28JdL5jZZKpAQ/s320/WhatsApp%20Image%202025-12-07%20at%208.37.14%20PM%20(1).jpeg" alt="MPLS 2024">
        <div class="news-body">
          <span class="muted">MPLS — 2024</span>
          <h3 style="margin:8px 0">MPLS 2024 — Angkatan ke 2</h3>
          <p class="muted">
            MPLS Angkatan ke-2 TKJ menjadi langkah pertama bagi para siswa baru untuk mengenal dunia jaringan komputer lebih dekat...
          </p>
        </div>
      </article>

      <!-- Berita 2 -->
      <article class="news-card">
        <img class="news-thumb" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiz_t7237N28Z1ONNOn2f54WlmYLQ1TXdPB-HCD27NzJlqLQD0HAXlhMxD1siD1tDXNJBX64QT4m3RY7PTWWJSA0Ly6k6avo6DRzlxvwmSBDB2jYeXQQKfXVZysSUVbM35cKH8jrM2QS6XVDBtsg0MSSMhllM95k558T83jn7n89_FqzJ4n_QP7wFlsUg/s320/WhatsApp%20Image%202025-12-07%20at%208.09.51%20PM.jpeg" alt="Juara Poster">

        <div class="news-body">
          <span class="muted">Sumpah Pemuda</span>
          <h3 style="margin:8px 0">Juara 1 Lomba Poster & Film</h3>
          <p class="muted">
            Tim XI TKJ A & XI TKJ B meraih Juara 1 pada lomba poster & film saat peringatan Sumpah Pemuda — apresiasi atas kreativitas dan kerja tim siswa.
          </p>
        </div>
      </article>

    </div>
  </div>
</section>

    <section id="sambutan">
      <div class="wrap">
        <h2 class="section-title">Sambutan</h2>
        <p class="lead-muted">Ucapan selamat datang dari pimpinan sekolah dan kepala program studi TKJ.</p>

        <div class="sambutan-grid">
          <div class="sambutan-card">
            <img class="sambutan-img" src="https://smknegeri8batam.sch.id/media_library/images/c1bdd661fd08dbf875d8773254d97979.jpg" alt="Kepala Sekolah">
            <div class="sambutan-content">
              <h3 style="margin:6px 0;color:var(--tkj-blue)">Kepala Sekolah</h3>
              <h4 style="margin:6px 0">Sholekhah Nurul Bariyah, S.Pd, M.Ak</h4>
              <p class="muted">Assalamu’alaikum. Selamat datang di Jurusan Teknik Komputer & Jaringan SMK Negeri 8 Batam. Kami berkomitmen memberikan pendidikan berkualitas, berkarakter, dan relevan dengan kebutuhan industri. Semoga website ini membantu Anda mengenal lebih jauh potensi dan keunggulan jurusan kami.</p>
            </div>
          </div>

          <div class="sambutan-card">
            <img class="sambutan-img" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjzi37GCi9qUq0TTMd40hM6u3U2zfJQtEz3mY5LAIUE_NKrT8QPK2kRTFMX78H_E07YzAi249-U2O7w260kU0ZAjPRsLaZ47qtZWt5-7b0lvK7JFsg3DbeAAde5wHJwQVOC6AlG42hy1gn6AZjH9a5b2dd93BURjPbE70ixkzelXQuG8IVMflBrit68cQ/s320/WhatsApp%20Image%202025-12-07%20at%208.37.14%20PM.jpeg" alt="Kaprodi TKJ">
            <div class="sambutan-content">
              <h3 style="margin:6px 0;color:var(--tkj-blue)">Kepala Program Studi</h3>
              <h4 style="margin:6px 0">Yohanna Br Tarigan, S.Kom</h4>
              <p class="muted">Selamat datang. Jurusan TKJ fokus membentuk lulusan yang kompeten dan kreatif. Melalui pembelajaran praktik, TEFA, dan program sertifikasi, kami mendukung siswa menjadi teknisi profesional dan wirausaha muda di bidang teknologi informasi.</p>
            </div>
          </div>
        </div>
      </div>
    </section>


    <section id="prestasi">
      <div class="wrap">
        <h2 class="section-title">Prestasi Jurusan</h2>
        <p class="lead-muted">Beberapa capaian dan penghargaan siswa TKJ.</p>

        <div class="prestasi-grid">
          <div class="prestasi-card">
            <div class="prestasi-badge">Juara 1</div>
            <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiz_t7237N28Z1ONNOn2f54WlmYLQ1TXdPB-HCD27NzJlqLQD0HAXlhMxD1siD1tDXNJBX64QT4m3RY7PTWWJSA0Ly6k6avo6DRzlxvwmSBDB2jYeXQQKfXVZysSUVbM35cKH8jrM2QS6XVDBtsg0MSSMhllM95k558T83jn7n89_FqzJ4n_QP7wFlsUg/s320/WhatsApp%20Image%202025-12-07%20at%208.09.51%20PM.jpeg" alt="Juara">
            <div style="padding:16px">
            <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiXJQGOdOXBaGgK2T1VEG2O6Vl6GVzBSoHlrAfgh6gh0YRmfvt7a70zFpy3sMCxBBukNso51BwZg1zsnmAMpaJZX1z56S8bYYHeifsBRi65PQd-FB23IolOKQ1dlJsQ_mt1Tyqn29WHlr3rGMtWqmqDrUUp80X9IN9RW0v4dwLTdgiviYtoS7n_r8V9Ig/s320/WhatsApp%20Image%202025-12-07%20at%208.09.51%20PM%20(1).jpeg" alt="Juara">
            <div style="padding:16px">
              <h3 style="margin:6px 0;color:var(--tkj-blue)">Juara 1 — Lomba Film & Poster</h3>
              <p class="muted">Pada peringatan Sumpah Pemuda, tim XI TKJ A & XI TKJ B meraih juara 1 pada lomba poster & film tingkat sekolah.</p>
            </div>
          </div>
        </div>
      </div>
    </section>  
    
<html lang="id">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>Workshop TKJ — SMK Negeri 8 Batam | Percetakan & Alat Tulis</title>
    <meta
      name="description"
      content="Workshop TKJ SMK Negeri 8 Batam: layanan percetakan, scan, jilid, laminating, ganci custom, fotocopy & penjualan alat tulis. Harga terjangkau, pengerjaan cepat."
    />
    <meta
      name="keywords"
      content="Workshop TKJ, SMK Negeri 8 Batam, percetakan, print warna, print hitam putih, laminating, jilid, scan, ganci custom, alat tulis"
    />
    <meta name="author" content="Workshop TKJ - SMK Negeri 8 Batam" />
    <style>
      :root {
        --accent: #0b6cf0;
        --muted: #6b7280;
        --bg: #f7f8fb;
        --card: #ffffff;
      }
      * {
        box-sizing: border-box;
      }
      body {
        font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto,
          "Helvetica Neue", Arial, sans-serif;
        margin: 0;
        background: var(--bg);
        color: #0f172a;
      }
      a {
        color: inherit;
      }
      header {
        background: linear-gradient(
          90deg,
          rgba(11, 108, 240, 0.06),
          rgba(11, 108, 240, 0.02)
        );
        border-bottom: 1px solid rgba(15, 23, 42, 0.04);
      }
      .container {
        max-width: 1100px;
        margin: 0 auto;
        padding: 24px;
      }
      .topbar {
        display: flex;
        align-items: center;
        justify-content: space-between;
      }
      .brand {
        display: flex;
        gap: 12px;
        align-items: center;
      }
      .brand img {
        width: 56px;
        height: 56px;
        object-fit: cover;
        border-radius: 8px;
      }
      .brand h1 {
        font-size: 18px;
        margin: 0;
      }
      nav a {
        margin-left: 18px;
        text-decoration: none;
        color: var(--muted);
        font-weight: 700;
      }

      /* Hero */
      .hero {
        display: grid;
        grid-template-columns: 1fr 420px;
        gap: 28px;
        align-items: center;
        padding: 36px 0;
      }
      .hero h2 {
        font-size: 34px;
        margin: 0 0 12px;
      }
      .hero p {
        color: var(--muted);
        margin: 0 0 18px;
        line-height: 1.6;
      }
      .cta {
        display: flex;
        gap: 12px;
      }
      .btn {
        padding: 12px 18px;
        border-radius: 10px;
        text-decoration: none;
        font-weight: 700;
        display: inline-block;
      }
      .btn-primary {
        background: var(--accent);
        color: white;
      }
      .btn-ghost {
        background: transparent;
        border: 2px solid rgba(11, 108, 240, 0.12);
        color: var(--accent);
      }
      .card {
        background: var(--card);
        padding: 18px;
        border-radius: 12px;
        box-shadow: 0 6px 18px rgba(15, 23, 42, 0.04);
      }

      /* Services grid */
      .grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
        gap: 16px;
        margin-top: 18px;
      }
      .service {
        padding: 18px;
        border-radius: 10px;
        text-align: left;
        border: 1px solid rgba(15, 23, 42, 0.03);
        background: linear-gradient(
          180deg,
          rgba(255, 255, 255, 1),
          rgba(247, 248, 251, 1)
        );
      }
      .service h4 {
        margin: 0 0 8px;
      }
      .price {
        font-weight: 800;
        font-size: 18px;
        color: var(--accent);
      }
      .muted {
        color: var(--muted);
      }

      /* Pricing table */
      table {
        width: 100%;
        border-collapse: collapse;
        margin-top: 12px;
      }
      th,
      td {
        padding: 12px;
        border-bottom: 1px solid #eef2ff;
        text-align: left;
      }
      th {
        background: #fbfdff;
      }

      /* Sections */
      section {
        padding: 36px 0;
      }
      h3 {
        margin: 0 0 12px;
      }
      .lead {
        color: var(--muted);
      }

      /* Contact */
      .contact-grid {
        display: grid;
        grid-template-columns: 1fr 320px;
        gap: 18px;
      }
      .contact-card p {
        margin: 6px 0;
      }

      footer {
        padding: 28px 0;
        border-top: 1px solid rgba(15, 23, 42, 0.04);
        margin-top: 36px;
        text-align: center;
        color: var(--muted);
      }

      /* Small */
      @media (max-width: 900px) {
        .hero {
          grid-template-columns: 1fr;
          padding: 18px 0;
        }
        .contact-grid {
          grid-template-columns: 1fr;
        }
        .brand h1 {
          font-size: 16px;
        }
      }
    </style>
  </head>
  <body>
    <header>
      <div class="container topbar">
        <div class="brand">
          <img
            src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgfK4NiGt3G7z9NqRgFkg6qiZfuiySFZsT0WTj41daMYOP4n8xoDY11HAYZferNyisIcwyh0Jvdv8HOMtOhNZdTo54CAx5rzzlvZt-ApbpRg4bzlwe2OBgzWPZxUyK8PEm4AkCBBd7ywTbT2sabD_NQ4yxhyphenhyphenE9tGa7XTEpoedlJgcu40Jp0dCpPFEPuTA/s300/OIP%20(1).jpg"
            alt="Logo Workshop TKJ"
            style="
              width: 56px;
              height: 56px;
              object-fit: cover;
              border-radius: 8px;
            "
          />
          <div>
            <h1>Workshop TKJ — SMK Negeri 8 Batam</h1>
            <div class="muted" style="font-size: 13px">
              Percetakan • Scan • Jilid • Laminating • Alat Tulis
            </div>
          </div>
        </div>
        <nav>
          <a href="#layanan">Layanan</a>
          <a href="#harga">Harga</a>
          <a href="#lokasi">Lokasi</a>
          <a href="#kontak">Kontak</a>
        </nav>
      </div>
    </header>

    <main class="container">
      <!-- Hero -->
      <section class="hero">
        <div>
          <h2>Workshop Teknik Komputer & Jaringan — SMK Negeri 8 Batam</h2>
          <p class="lead">
            Kami menyediakan layanan percetakan, scan, fotocopy, finishing
            dokumen, produk kreatif (ganci custom), dan penjualan alat tulis
            dengan harga terjangkau. Dikelola oleh siswa TKJ yang kompeten dan
            diawasi guru profesional.
          </p>
          <div class="cta">
            <a class="btn btn-primary" href="#kontak">Hubungi via WhatsApp</a>
            <a class="btn btn-ghost" href="#layanan">Lihat Layanan</a>
          </div>

          <div style="margin-top: 22px" class="card">
            <strong>Jam Operasional</strong>
            <p class="muted" style="margin: 6px 0">
              Senin - Jumat: 07.00 - 15.00 WIB<br />Sabtu: Close
            </p>
            <strong>Alamat</strong>
            <p class="muted">
              SMK Negeri 8 Batam, Kav. Bukit Melati - Sei Pelunggut, Kecamatan
              Sagulung, Batam
            </p>
          </div>
        </div>

        <aside>
          <div class="card">
            <h3>Pesan Sekarang</h3>
            <p class="muted">
              Kirimkan file cetak atau pesan produk lewat WhatsApp. Cantumkan
              jenis layanan, jumlah, dan waktu pengambilan.
            </p>
            <p style="margin-top: 12px">
              <strong>WhatsApp:</strong>
              <a href="https://wa.me/6281943725324" target="_blank"
                >+62 819-4372-5324</a
              >
            </p>
            <p style="margin: 6px 0">
              <strong>Estimasi Selesai:</strong> 30 menit - 1 hari tergantung
              antrian dan jenis layanan.
            </p>
            <a
              class="btn btn-primary"
              href="https://wa.me/6281943725324"
              target="_blank"
              >Chat WhatsApp</a
            >
          </div>
        </aside>
      </section>

      <!-- Services -->
      <section id="layanan">
        <h3>Layanan Kami</h3>
        <p class="muted">
          Layanan lengkap untuk kebutuhan akademik dan administrasi, dikerjakan
          rapi oleh tim Workshop TKJ.
        </p>

        <div class="grid" style="margin-top: 18px">
          <div class="service">
            <img
              src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi5i-J2FbiTgM1OUvRhTV6pZvOl_9Fbmk5mo2rOJg1t0H8O8D2KVdlzHWUJWtS04y3I1Dj1T49i_lvhA7X4QzHvL17IogPWVJ8VwtgdrVvnE5zYK4CxoXEGN2bWuzBhyts7QcGqleiq__l1nFPzSgNgRzZ7QJhKfcy7IxWxcpCbKrbRqRvFgG2FZoRndw/s1200/WhatsApp%20Image%202025-12-01%20at%209.23.19%20PM.jpeg"
              style="width: 100%; border-radius: 10px; margin-bottom: 10px"
            />
            <h4>Print & Fotocopy</h4>
            <p class="muted">
              Print dokumen hitam putih maupun berwarna dengan hasil tajam.
            </p>
            <div class="price">Print Warna: Rp 1.000 / lembar</div>
            <div style="margin-top: 6px" class="muted">
              Print Hitam Putih / Fotocopy: Rp 500 / lembar
            </div>
          </div>

          <div class="service">
            <img
              src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjwr-Iki2r_f4zYwScN1r64Y1SXfCE0mebpeJM6HCpld-ExJEqmSz9nT3LKNC3bwap5y3BOmHTvmJTwHh5bzTcuzgjdi459QQonravitp_BdHzHC89u7Egf7Cw9e1eQY3WFF-VRdkJurusJrtvLQsIeBeZ_gy_v6RS78Ookr4iyIvn1_iwP3LyZFf6wNA/s900/WhatsApp%20Image%202025-12-01%20at%209.21.36%20PM.jpeg"
              style="width: 100%; border-radius: 10px; margin-bottom: 10px"
            />
            <h4>Scan Dokumen</h4>
            <p class="muted">
              Hasil scan PDF/JPG siap kirim lewat WhatsApp atau email.
            </p>
            <div class="price">Rp 1.000 / lembar</div>
          </div>

          <div class="service">
            <div style="display: flex; gap: 10px; margin-bottom: 10px">
              <img
                src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiLT_GA4C7ALZYVSaE7mdMsHrQNywtkle2Nuez4DtisNZwwdCfAtUSzrFe0gAUqKwI9b7oLskD-aAbauisq-r5TuTNAJIW9H20ezMprFvGUtrqMKsJzA-Byx2n3gDpr1wrMimMGwqDXx7qaC8TFoEeqCXSZsKhy3XHSiYyNFiUsrwa-K6GwFq0wIX9cFw/s900/WhatsApp%20Image%202025-12-01%20at%209.21.36%20PM%20(1).jpeg"
                style="width: 50%; border-radius: 10px; object-fit: cover"
              />
              <img
                src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgYzNn21dywtRWDq-Slzd_LMCOKNW2lwBoT4Z62SIhGnZW2O7mZUUCgfREjOdPaOaXBABN4rWRhVpVyq3WymRigDElN4nng6HBgEwTHJneXegMYaahGRrCVNE-RzeILmA3EevkVzYySsdaEkBjcf6J9EjjxEQ5Payq9xXN7wPZoIEDRmPFa1x0fVVzDxQ/s700/WhatsApp%20Image%202025-12-01%20at%209.21.46%20PM.jpeg"
                style="width: 50%; border-radius: 10px; object-fit: cover"
              />
            </div>
            <h4>Finishing (Jilid & Laminating)</h4>
            <p class="muted">
              Jilid rapi untuk tugas, skripsi, dan laporan. Laminating
              melindungi dokumen penting.
            </p>
            <div class="price">Jilid: Rp 3.000 • Laminating A4: Rp 5.000</div>
          </div>

          <div class="service">
            <img
              src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhvrHBhLcNmW1z8D4oQfjtIVtHpwjfmMelNILLgQE69e_CSINDX-ndnKcySPbzm54j0bQL_AkY1vI9tua0d7odJGDjDmUXQ9YpMRU2hENhma7wNSoXqPZa0s2jxfvhfI1v8JIW1Z2Cz1vYEienyc5yNca5gTUm6DX1zoFfTI0tO9h1m7lRKRkBAO_1FNw/s800/WhatsApp%20Image%202025-12-01%20at%209.23.18%20PM.jpeg"
              style="width: 100%; border-radius: 10px; margin-bottom: 10px"
            />
            <h4>Produk Custom</h4>
            <p class="muted">
              Ganci custom, cocok untuk hadiah atau souvenir acara sekolah.
            </p>
            <div class="price">Ganci Custom: Rp 5.000 / pcs</div>
          </div>

          <div class="service">
            <h4>Alat Tulis</h4>
            <p class="muted">
              Menjual berbagai alat tulis: pulpen, pensil, stabilo, buku tulis,
              map, kertas HVS, dan lainnya.
            </p>
            <div class="muted">Stok lengkap & harga pelajar.</div>
          </div>
        </div>
      </section>

      <!-- Pricing Table -->
      <section id="harga">
        <h3>Daftar Harga (Ringkas)</h3>
        <div class="card">
          <table>
            <thead>
              <tr>
                <th>Layanan</th>
                <th>Harga</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Print Berwarna</td>
                <td>Rp 1.000 / lembar</td>
              </tr>
              <tr>
                <td>Print Hitam Putih</td>
                <td>Rp 500 / lembar</td>
              </tr>
              <tr>
                <td>Scan Dokumen</td>
                <td>Rp 1.000 / lembar</td>
              </tr>
              <tr>
                <td>Fotocopy</td>
                <td>Rp 500 / lembar</td>
              </tr>
              <tr>
                <td>Jilid</td>
                <td>Rp 3.000 / dokumen</td>
              </tr>
              <tr>
                <td>Laminating A4</td>
                <td>Rp 5.000 / lembar</td>
              </tr>
              <tr>
                <td>Ganci Custom</td>
                <td>Rp 5.000 / pcs</td>
              </tr>
            </tbody>
          </table>
        </div>
      </section>

      <!-- Keunggulan -->
      <section>
        <h3>Mengapa Memilih Kami?</h3>
        <ul>
          <li>Harga terjangkau dan transparan — cocok untuk pelajar.</li>
          <li>
            Dikerjakan langsung oleh siswa TKJ berkompeten dengan pengawasan
            guru.
          </li>
          <li>Peralatan modern untuk kualitas cetak & finishing yang rapi.</li>
          <li>Pelayanan ramah, cepat, dan mudah dihubungi via WhatsApp.</li>
        </ul>
      </section>

      <!-- Testimoni -->
      <section>
        <h3>Testimoni</h3>
        <div class="grid">
          <div class="card">
            <strong>Rizki, Siswa XI</strong>
            <p class="muted">
              "Print tugas cepet dan hasilnya oke. Harga juga terjangkau buat
              kami pelajar."
            </p>
          </div>
          <div class="card">
            <strong>Bu Maya, Guru</strong>
            <p class="muted">
              "Jilid laporan rapi, servis ramah — sangat membantu untuk
              administrasi sekolah."
            </p>
          </div>
        </div>
      </section>

      <!-- Lokasi & Kontak -->
      <section id="lokasi">
        <h3>Lokasi & Kontak</h3>
        <div class="contact-grid">
          <div>
            <div class="card contact-card">
              <h4>Alamat</h4>
              <p>
                SMK Negeri 8 Batam<br />Kav. Bukit Melati - Sei Pelunggut<br />Kecamatan
                Sagulung, Batam
              </p>

              <h4 style="margin-top: 12px">Jam Operasional</h4>
              <p class="muted">
                Senin - Jumat: 08.00 - 15.00 WIB<br />Sabtu - Minggu : Close
              </p>

              <h4 style="margin-top: 12px">Informasi & Pemesanan</h4>
              <p>
                <strong>WhatsApp:</strong>
                <a href="https://wa.me/6281943725324" target="_blank"
                  >+62 819-4372-5324</a
                >
              </p>
              <p class="muted">
                Sertakan jenis layanan, jumlah, dan waktu pengambilan saat
                memesan.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>


      <!-- FAQ -->
      <section>
        <h3>Pertanyaan Umum (FAQ)</h3>
        <div class="card">
          <h4>Apa saja metode pembayaran yang diterima?</h4>
          <p class="muted">
            Pembayaran tunai di tempat, dan dapat menerima transfer bank /
            e-wallet jika diperlukan. Konfirmasi melalui WhatsApp.
          </p>

          <h4>Berapa lama proses cetak biasa?</h4>
          <p class="muted">
            Untuk print standar, biasanya 30 menit sampai 1 jam tergantung
            antrian. Untuk jumlah besar, waktu disesuaikan.
          </p>

          <h4>Apakah menerima file cetak via email atau WhatsApp?</h4>
          <p class="muted">
            Ya. Kirim file PDF atau gambar ke WhatsApp kami dan sertakan
            instruksi (warna/hitam-putih, jumlah, finishing).
          </p>
        </div>
      </section>

      <!-- CTA akhir -->
      <section id="kontak">
        <div
          class="card"
          style="
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 16px;
            flex-wrap: wrap;
          "
        >
          <div>
            <h3>Siap Cetak atau Butuh Alat Tulis?</h3>
            <p class="muted">
              Kirim file atau pertanyaan lewat WhatsApp. Kami siap bantu dengan
              cepat dan ramah.
            </p>
          </div>
          <div>
            <a
              class="btn btn-primary"
              href="https://wa.me/6281943725324"
              target="_blank"
              >Chat WhatsApp: +62 819-4372-5324</a
            >
          </div>
        </div>
      </section>
    </main>

    <footer>
      <div class="container">
        <div
          style="
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 12px;
            flex-wrap: wrap;
          "
        >
          <div>
            <strong>Workshop TKJ — SMK Negeri 8 Batam</strong>
            <div class="muted">
              Kav. Bukit Melati - Sei Pelunggut, Kecamatan Sagulung, Batam
            </div>
          </div>
          <div class="muted">© 2025 — Semua hak dilindungi</div>
        </div>
      </div>
    </footer>
  </body>
</html>


        <div class="gallery-grid" style="margin-top:18px">
          <div class="gallery-card"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhGoCBq4FWlprBCCLKc6LmGv9VCRNzpcZubPU2Pg5ne30JfFMRUPxEh1oDrH3qlCuwf-6kXsEL07jhoR5Dt3vo7rvKw9UyvZb1W-MgMhP8Qorou_emb7ghqfaRdNVjbhEUkXMkvBwETNRlvyG5zcEZ_sHgUgD3uKdN8SC_tzpZlLCzjYKJ7wLHzSjX6Cg/s1280/WhatsApp%20Image%202025-12-07%20at%208.12.35%20PM.jpeg" alt="Kegiatan Siswi TKJ"></div>
          <div class="gallery-card"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjEwLFrohX9bpMfm55C6GOX0o7kEeGBVXHkmtzZ-_i51HVzjFwJwkWHwC95wmHtGmFCy3q6kZyaMhEzfDlKCc7UNb8Edi8JOXMbX-nC01ap5tETMWDgFCneE9k9PGhwSISGS_fqaBSaLXCXOUncI-aA62zNDfvpZpOqEzMkIJf2L3HKqeHUMwVYY0rlgw/s1280/WhatsApp%20Image%202025-12-07%20at%208.12.34%20PM.jpeg" alt="Sablon Gelas"></div>
          <div class="gallery-card"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjqjVZMrX2yMWjmI5KQHHfdb2SlA5SZvoQuXHUcObJfCyGMp4WydXz5IKMluKKeqHIQ6pjFtn7BAp2zS8wfDIcfe5sqcSy9ksyxMglRMwrDYhJcbxb7jH9H182E4pD-HaFHv9fjLPO9iFuHLazg_RnhwyeXGiIsZTXqer3aUhy3kyoafflHJ6Bj_SoTlA/s1280/WhatsApp%20Image%202025-12-07%20at%208.12.32%20PM.jpeg" alt="Proses Ganci"></div>
          <div class="gallery-card"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgDWNht5QCNJdj04M62KBDJmLLWz8rYNd-FXKiaB-BVRi5fEZq9t1x7VCqnylInEKb-C9bbLo8T166MDHMgL1zH0gUleCFQE31YrEfCsPCE9xUzl8i8hmfzhDEdAkinO030EOmgTEd9uMNN30obJkhKpS8xn-2foj5ZnnA4CzjDaE2Qh0x86l2zcM-PYg/s1280/WhatsApp%20Image%202025-12-07%20at%208.12.33%20PM.jpeg" alt="Proses Ganci"></div>
        </div>
      </div>
    </section>

    <section id="testimoni">
      <div class="wrap">
        <h2 class="section-title">Testimoni</h2>
        <p class="lead-muted">Suara siswa & alumni tentang pengalaman di Jurusan TKJ.</p>

        <div class="testi-wrap">
          <div class="testi card"><strong>Rizky (Alumni)</strong><p class="muted">"Praktik & magang yang intens membuat saya siap kerja dalam waktu singkat."</p></div>
          <div class="testi card"><strong>Siti (Siswa)</strong><p class="muted">"Guru suportif, lab lengkap, TEFA sangat membantu meningkatkan skill."</p></div>
          <div class="testi card"><strong>Farhan (Alumni)</strong><p class="muted">"Berkat TKJ saya mendapat pekerjaan di perusahaan jaringan lokal."</p></div>
        </div>
      </div>
    </section>


    <section id="kontak">
      <div class="wrap">
        <h2 class="section-title">Hubungi Kami</h2>
        <p class="lead-muted">Kontak & lokasi Jurusan TKJ — SMK Negeri 8 Batam.</p>

        <div class="contact-grid">
          <div>
            <div class="card">
              <h3 style="margin-top:0">Informasi Kontak</h3>
              <p class="muted"><strong>Alamat:</strong> SMK Negeri 8 Batam — Kav. Bukit Melati - Sei Pelunggut, Kecamatan Sagulung, Batam</p>
              <p class="muted"><strong>Telepon / WA:</strong> <a href="https://wa.me/6281943725324" style="color:var(--tkj-blue);text-decoration:none">+62 819-4372-5324</a></p>
              <p class="muted"><strong>Email:</strong> officialhumas20@gmail.com</p>

              <h4 style="margin-top:12px">Form Kontak</h4>
              <form class="contact-form" id="contactForm">
                <input type="text" name="nama" placeholder="Nama lengkap" required>
                <input type="text" name="telp" placeholder="No. Telepon" required>
                <input type="email" name="email" placeholder="Email">
                <textarea name="pesan" placeholder="Pesan Anda..." required></textarea>
                <div style="display:flex;gap:8px">
                  <button type="submit" class="btn btn-primary" style="flex:1">Kirim Pesan</button>
                  <button type="reset" class="btn" style="flex:1;border:1px solid rgba(11,20,40,0.06)">Reset</button>
                </div>
                <p class="muted" style="margin-top:8px"></p>
              </form>
            </div>
          </div>

          <aside>
            <div class="card">
              <h3 style="margin-top:0">Lokasi</h3>
              <p class="muted">Klik peta untuk membuka di Google Maps</p>
              <iframe class="map-embed" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3987.005164721909!2d103.95619707496451!3d1.0504494991921376!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x31d989972d74c5cf%3A0x6e1b652deefd7fc5!2sSMK%20Negeri%208%20Batam!5e0!3m2!1sid!2sid!4v1700000000000" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
          </aside>
        </div>
      </div>
    </section>

    <section id="daftar">
      <div class="wrap">
        <div class="cta-bottom">
          <div>
            <h3 style="margin:0">Tertarik Bergabung di TKJ?</h3>
            <p style="margin:6px 0 0">Daftarkan dirimu sekarang untuk mengikuti program praktis & sertifikasi.</p>
          </div>
          <div style="display:flex;gap:10px">
            <a class="btn" href="#kontak" style="background:#fff;color:var(--tkj-blue;font-weight:700);padding:12px 18px;border-radius:10px;text-decoration:none">Daftar Sekarang</a>
            <a class="btn" href="#prestasi" style="background:rgba(255,255,255,0.12);color:#fff">Lihat Prestasi</a>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="wrap foot-inner">
      <div>
        <strong>Teknik Komputer & Jaringan — SMKN 8 Batam</strong>
        <div class="muted">Kav. Bukit Melati - Sei Pelunggut, Kec. Sagulung, Batam</div>
      </div>
      <div class="muted">© <span id="year"></span> SMK Negeri 8 Batam</div>
    </div>
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();

    (function(){
      const slider = document.getElementById('heroSlider');
      const dots = Array.from(document.querySelectorAll('#heroDots .dot'));
      let index = 0;
      function go(i){
        index = (i + 3) % 3;
        slider.style.transform = 'translateX(' + (-index*100) + '%)';
        dots.forEach(d=>d.classList.remove('active'));
        dots[index].classList.add('active');
      }
      dots.forEach(d => d.addEventListener('click', ()=> go(+d.dataset.index)));
      let interval = setInterval(()=> go(index+1), 6000);
      slider.parentElement.addEventListener('mouseenter', ()=> clearInterval(interval));
      slider.parentElement.addEventListener('mouseleave', ()=> interval = setInterval(()=> go(index+1), 6000));
    })();

    (function(){
      const hb = document.querySelector('.hamburger');
      const nav = document.querySelector('nav.links');
      hb?.addEventListener('click', ()=>{
        if(nav.style.display === 'flex') nav.style.display = '';
        else nav.style.display = 'flex';
      });
    })();

    document.getElementById('contactForm')?.addEventListener('submit', function(e){
      e.preventDefault();
      alert('Terima kasih! Pesan Anda telah tercatat (form demo). Kontak: +62 819-4372-5324');
      this.reset();
    });
  </script>
</body>
</html>
