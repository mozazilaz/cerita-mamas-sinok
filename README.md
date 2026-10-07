<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cerita Kita dan Cinta yang Terus Bertumbuh</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Poppins:wght@300;400;500;600&display=swap');

:root{
  --navy:#202638;
  --navy2:#151a2b;
  --cream:#f8f3ec;
  --taupe:#a88f86;
  --rose:#b97883;
  --gold:#d6b77c;
  --charcoal:#30323a;
  --white:#fffdf9;
}

*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

html{
  scroll-behavior:smooth;
}

body{
  font-family:'Poppins',sans-serif;
  background:var(--navy);
  color:var(--cream);
  overflow-x:hidden;
}

button{
  font-family:inherit;
}

section{
  position:relative;
}

/* ================= BACKGROUND STARS ================= */

#stars{
  position:fixed;
  inset:0;
  pointer-events:none;
  z-index:0;
}

.star{
  position:absolute;
  width:2px;
  height:2px;
  background:#fff;
  border-radius:50%;
  opacity:.6;
  animation:twinkle 3s infinite ease-in-out;
}

@keyframes twinkle{
  0%,100%{opacity:.15;transform:scale(.8)}
  50%{opacity:1;transform:scale(1.4)}
}

/* ================= MUSIC ================= */

.music-btn{
  position:fixed;
  right:20px;
  top:20px;
  z-index:1000;
  width:48px;
  height:48px;
  border-radius:50%;
  border:1px solid rgba(214,183,124,.5);
  background:rgba(32,38,56,.85);
  color:var(--gold);
  cursor:pointer;
  backdrop-filter:blur(10px);
  box-shadow:0 8px 30px rgba(0,0,0,.25);
  transition:.3s;
}

.music-btn:hover{
  transform:scale(1.08);
}

/* ================= OPENING ================= */

#opening{
  min-height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
  padding:30px;
  background:
    radial-gradient(circle at 50% 40%,rgba(185,120,131,.12),transparent 28%),
    radial-gradient(circle at 20% 20%,rgba(214,183,124,.08),transparent 25%),
    linear-gradient(145deg,var(--navy2),var(--navy));
  z-index:1;
}

.opening-content{
  max-width:700px;
  position:relative;
  z-index:2;
}

.small-title{
  letter-spacing:6px;
  font-size:12px;
  color:var(--gold);
  margin-bottom:25px;
}

.opening-content h1{
  font-family:'Cormorant Garamond',serif;
  font-size:clamp(48px,9vw,92px);
  line-height:.9;
  font-weight:500;
  margin-bottom:25px;
}

.opening-content p{
  color:#d8d5d0;
  font-size:14px;
  line-height:1.8;
}

.date{
  color:var(--rose);
  letter-spacing:4px;
  margin:22px 0 35px;
  font-size:13px;
}

.open-btn{
  border:none;
  padding:15px 30px;
  border-radius:40px;
  background:var(--cream);
  color:var(--navy);
  font-weight:600;
  cursor:pointer;
  transition:.3s;
  box-shadow:0 10px 35px rgba(0,0,0,.25);
}

.open-btn:hover{
  transform:translateY(-3px);
  box-shadow:0 15px 40px rgba(0,0,0,.35);
}

/* ================= MAIN ================= */

#main{
  display:none;
}

.container{
  width:min(1050px,90%);
  margin:auto;
}

.section{
  padding:110px 0;
}

.section.light{
  background:var(--cream);
  color:var(--charcoal);
}

.section.dark{
  background:var(--navy);
}

.eyebrow{
  color:var(--rose);
  letter-spacing:4px;
  font-size:11px;
  text-transform:uppercase;
  margin-bottom:14px;
}

.section-title{
  font-family:'Cormorant Garamond',serif;
  font-size:clamp(42px,7vw,70px);
  font-weight:500;
  line-height:1;
  margin-bottom:25px;
}

.center{
  text-align:center;
}

/* ================= STORY ================= */

.story-card{
  max-width:800px;
  margin:40px auto 0;
  padding:45px;
  border:1px solid rgba(214,183,124,.2);
  border-radius:28px;
  background:rgba(255,255,255,.035);
  box-shadow:0 20px 80px rgba(0,0,0,.18);
}

.story-card p{
  line-height:2;
  color:#ddd9d3;
  margin-bottom:20px;
}

.highlight{
  color:var(--gold);
  font-family:'Cormorant Garamond',serif;
  font-size:30px;
}

/* ================= TIMELINE ================= */

.timeline{
  position:relative;
  max-width:850px;
  margin:60px auto 0;
}

.timeline:before{
  content:"";
  position:absolute;
  left:50%;
  top:0;
  bottom:0;
  width:1px;
  background:rgba(214,183,124,.35);
  transform:translateX(-50%);
}

.timeline-item{
  width:50%;
  padding:25px 45px;
  position:relative;
}

.timeline-item:nth-child(odd){
  margin-left:0;
  text-align:right;
}

.timeline-item:nth-child(even){
  margin-left:50%;
}

.timeline-dot{
  position:absolute;
  width:13px;
  height:13px;
  border-radius:50%;
  background:var(--gold);
  top:35px;
  box-shadow:0 0 20px rgba(214,183,124,.7);
}

.timeline-item:nth-child(odd) .timeline-dot{
  right:-6px;
}

.timeline-item:nth-child(even) .timeline-dot{
  left:-6px;
}

.timeline-box{
  background:rgba(255,255,255,.05);
  border:1px solid rgba(214,183,124,.15);
  border-radius:20px;
  padding:25px;
}

.timeline-box h3{
  font-family:'Cormorant Garamond',serif;
  font-size:28px;
  color:var(--gold);
  margin-bottom:10px;
}

.timeline-box p{
  font-size:13px;
  line-height:1.8;
  color:#d7d3ce;
}

/* ================= PHOTO GALLERY ================= */

.gallery{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:25px;
  margin-top:50px;
}

.photo-card{
  background:white;
  padding:12px 12px 30px;
  box-shadow:0 15px 35px rgba(0,0,0,.15);
  transform:rotate(-1deg);
  transition:.35s;
}

.photo-card:nth-child(2){
  transform:rotate(1.5deg);
}

.photo-card:nth-child(3){
  transform:rotate(-2deg);
}

.photo-card:nth-child(4){
  transform:rotate(1deg);
}

.photo-card:nth-child(5){
  transform:rotate(-1.5deg);
}

.photo-card:nth-child(6){
  transform:rotate(2deg);
}

.photo-card:hover{
  transform:rotate(0) translateY(-8px) scale(1.02);
}

.photo-card img{
  width:100%;
  aspect-ratio:1/1;
  object-fit:cover;
  background:#ddd;
  display:block;
}

.photo-caption{
  color:var(--charcoal);
  font-family:'Cormorant Garamond',serif;
  font-size:20px;
  text-align:center;
  margin-top:13px;
}

/* ================= LETTER ================= */

.letter{
  max-width:760px;
  margin:45px auto 0;
  background:#fffdf9;
  color:var(--charcoal);
  padding:55px;
  border-radius:4px;
  box-shadow:0 25px 70px rgba(0,0,0,.25);
  position:relative;
}

.letter:before{
  content:"";
  position:absolute;
  inset:12px;
  border:1px solid rgba(168,143,134,.3);
  pointer-events:none;
}

.letter p{
  position:relative;
  line-height:2;
  margin-bottom:22px;
}

.signature{
  font-family:'Cormorant Garamond',serif;
  font-size:34px;
  color:var(--rose);
  margin-top:35px;
}

/* ================= FUTURE ================= */

.future-grid{
  display:grid;
  grid-template-columns:repeat(5,1fr);
  gap:15px;
  margin-top:50px;
}

.future-card{
  padding:28px 18px;
  border-radius:22px;
  background:rgba(255,255,255,.045);
  border:1px solid rgba(214,183,124,.15);
  text-align:center;
  transition:.3s;
}

.future-card:hover{
  transform:translateY(-6px);
  border-color:rgba(214,183,124,.5);
}

.future-icon{
  font-size:30px;
  margin-bottom:15px;
}

.future-card h3{
  font-family:'Cormorant Garamond',serif;
  font-size:22px;
  color:var(--gold);
  margin-bottom:8px;
}

.future-card p{
  font-size:12px;
  color:#d5d1cb;
  line-height:1.7;
}

/* ================= GAME ================= */

.game-box{
  max-width:700px;
  margin:50px auto 0;
  background:var(--white);
  color:var(--charcoal);
  padding:35px;
  border-radius:28px;
  box-shadow:0 25px 70px rgba(0,0,0,.2);
}

.question-number{
  color:var(--rose);
  font-size:12px;
  letter-spacing:3px;
  text-transform:uppercase;
  margin-bottom:15px;
}

.question{
  font-family:'Cormorant Garamond',serif;
  font-size:34px;
  margin-bottom:25px;
}

.options{
  display:grid;
  gap:12px;
}

.option{
  border:1px solid #ddd5cc;
  background:white;
  padding:15px 18px;
  border-radius:14px;
  text-align:left;
  cursor:pointer;
  transition:.25s;
}

.option:hover{
  border-color:var(--rose);
  transform:translateX(4px);
}

.option.correct{
  background:#e8f3e7;
  border-color:#83a980;
}

.option.wrong{
  background:#f8e5e7;
  border-color:#c67e88;
}

.feedback{
  min-height:30px;
  margin-top:20px;
  font-size:14px;
  font-weight:500;
}

.next-btn{
  display:none;
  margin-top:15px;
  border:none;
  background:var(--navy);
  color:white;
  padding:13px 24px;
  border-radius:30px;
  cursor:pointer;
}

.score{
  text-align:center;
  display:none;
}

.score h3{
  font-family:'Cormorant Garamond',serif;
  font-size:42px;
  margin-bottom:15px;
}

.secret{
  display:none;
  margin-top:30px;
  padding:30px;
  background:var(--navy);
  color:var(--cream);
  border-radius:20px;
  text-align:center;
}

.secret h3{
  font-family:'Cormorant Garamond',serif;
  font-size:35px;
  color:var(--gold);
  margin-bottom:12px;
}

/* ================= END ================= */

.final{
  min-height:90vh;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
  background:
    radial-gradient(circle at 50% 45%,rgba(185,120,131,.16),transparent 30%),
    var(--navy2);
}

.final-content{
  max-width:700px;
}

.final h2{
  font-family:'Cormorant Garamond',serif;
  font-size:clamp(50px,9vw,90px);
  font-weight:500;
  line-height:.95;
  margin:20px 0;
}

.final p{
  line-height:2;
  color:#d7d3ce;
}

.heart{
  font-size:45px;
  animation:heartbeat 1.5s infinite;
}

@keyframes heartbeat{
  0%,100%{transform:scale(1)}
  50%{transform:scale(1.15)}
}

.footer{
  padding:30px;
  text-align:center;
  font-size:11px;
  color:#858998;
  background:var(--navy2);
}

/* ================= MOBILE ================= */

@media(max-width:750px){

  .section{
    padding:80px 0;
  }

  .story-card{
    padding:28px 22px;
  }

  .timeline:before{
    left:10px;
  }

  .timeline-item,
  .timeline-item:nth-child(even){
    width:100%;
    margin-left:0;
    padding:25px 0 25px 40px;
    text-align:left;
  }

  .timeline-item:nth-child(odd) .timeline-dot,
  .timeline-item:nth-child(even) .timeline-dot{
    left:4px;
    right:auto;
  }

  .gallery{
    grid-template-columns:repeat(2,1fr);
    gap:15px;
  }

  .photo-card{
    padding:8px 8px 20px;
  }

  .photo-caption{
    font-size:16px;
  }

  .letter{
    padding:35px 25px;
  }

  .future-grid{
    grid-template-columns:1fr 1fr;
  }

  .future-card:last-child{
    grid-column:span 2;
  }

  .game-box{
    padding:25px 18px;
  }

  .question{
    font-size:29px;
  }
}
</style>
</head>

<body>

<div id="stars"></div>

<button class="music-btn" id="musicBtn" title="Putar musik">♫</button>

<audio id="music" loop>
  <!--
  GANTI file di bawah dengan file audio yang kamu punya.
  Simpan file audio di folder yang sama dengan index.html
  dengan nama: photograph.mp3
  -->
  <source src="photograph.mp3" type="audio/mpeg">
</audio>

<!-- ================= OPENING ================= -->

<section id="opening">

  <div class="opening-content">

    <div class="small-title">FOR MAMAS</div>

    <h1>Cerita Kita</h1>

    <p>
      dan cinta yang terus bertumbuh
    </p>

    <div class="date">
      22 • 11 • 2026
    </div>

    <button class="open-btn" onclick="openStory()">
      Buka cerita kita ♡
    </button>

  </div>

</section>


<!-- ================= MAIN ================= -->

<main id="main">

  <!-- STORY -->

  <section class="section dark">

    <div class="container">

      <div class="center">

        <div class="eyebrow">Chapter 01</div>

        <h2 class="section-title">
          Semuanya bermula<br>
          dari sebuah chat.
        </h2>

      </div>

      <div class="story-card">

        <p>
          Kalau dipikir-pikir, lucu juga bagaimana dua orang
          bisa sampai sejauh ini hanya karena awalnya bertemu
          di <span class="highlight">Leo Telegram.</span>
        </p>

        <p>
          Kita mulai dari ngobrol, bercanda, saling cerita,
          sampai akhirnya terasa nyaman. Entah sejak kapan,
          setiap kali ngobrol sama Mamas, Sinok selalu merasa
          senang.
        </p>

        <p>
          Kita bahkan nggak pernah punya momen resmi seperti
          "mau nggak jadi pacarku?".
        </p>

        <p>
          Kita cuma sama-sama tahu...
          <br>
          <span class="highlight">
            ternyata kita sudah menjadi kita.
          </span>
        </p>

        <p>
          Sampai akhirnya, setelah dua bulan hanya mengenal
          lewat chat, kita bertemu untuk pertama kalinya.
          Dan jujur...
          Sinok sempat ragu waktu pertama kali melihat Mamas.
        </p>

        <p>
          Tapi ternyata keraguan kecil di hari itu adalah
          awal dari perjalanan yang jauh lebih panjang.
        </p>

      </div>

    </div>

  </section>


  <!-- TIMELINE -->

  <section class="section dark">

    <div class="container">

      <div class="center">

        <div class="eyebrow">Our Little Timeline</div>

        <h2 class="section-title">
          Beberapa momen<br>yang Sinok simpan.
        </h2>

      </div>

      <div class="timeline">

        <div class="timeline-item">

          <div class="timeline-dot"></div>

          <div class="timeline-box">

            <h3>Pertemuan Pertama</h3>

            <p>
              Setelah dua bulan chatting, akhirnya Mamas
              menjemput Sinok di stasiun.
              Walaupun Mamas telat...
              tetap saja, hari itu menjadi hari ketika
              dua orang yang selama ini hanya saling mengenal
              lewat layar akhirnya bertemu langsung.
            </p>

          </div>

        </div>


        <div class="timeline-item">

          <div class="timeline-dot"></div>

          <div class="timeline-box">

            <h3>Pantai Tirang</h3>

            <p>
              Sunset, ngobrol, lari-larian, menikmati waktu
              sederhana bersama, bahkan Mamas menggendong Sinok.
              Sederhana, tapi justru momen seperti ini yang
              terasa paling hangat untuk diingat.
            </p>

          </div>

        </div>


        <div class="timeline-item">

          <div class="timeline-dot"></div>

          <div class="timeline-box">

            <h3>Pertama Kali Berenang</h3>

            <p>
              Mamas menjemput Sinok dan mengajak bermain
              bersama keluarga Mamas.
              Hari itu terasa spesial karena Sinok mulai
              masuk sedikit demi sedikit ke dunia Mamas.
            </p>

          </div>

        </div>


        <div class="timeline-item">

          <div class="timeline-dot"></div>

          <div class="timeline-box">

            <h3>Ketika Mamas Menjadi Imam</h3>

            <p>
              Di mushola alun-alun, Mamas memimpin Sinok dalam
              salat. Ada perasaan yang sulit dijelaskan.
              Melihat seseorang yang Sinok sayangi menjadi imam,
              membuat Sinok membayangkan bahwa mungkin...
              suatu hari nanti, ini bukan lagi sekadar sebuah
              momen.
            </p>

          </div>

        </div>


        <div class="timeline-item">

          <div class="timeline-dot"></div>

          <div class="timeline-box">

            <h3>Di Saat Sinok Tidak Baik-Baik Saja</h3>

            <p>
              Setelah menghadiri sebuah acara, Sinok tidak
              dalam kondisi yang baik. Dan di saat seperti itu,
              Mamas tetap ada. Membelikan minuman, membantu,
              merawat, dan memastikan Sinok baik-baik saja.
            </p>

            <p>
              Karena ternyata cinta bukan cuma tentang
              tertawa bersama.
              Kadang cinta terlihat paling jelas ketika
              salah satu dari kita sedang tidak baik-baik saja.
            </p>

          </div>

        </div>

      </div>

    </div>

  </section>


  <!-- PHOTOS -->

  <section class="section light">

    <div class="container">

      <div class="center">

        <div class="eyebrow">Our Memories</div>

        <h2 class="section-title">
          Foto-foto yang<br>nanti Sinok isi sendiri.
        </h2>

        <p>
          Tinggal ganti file foto sesuai petunjuk di kode.
        </p>

      </div>

      <div class="gallery">

        <div class="photo-card">
          <img src="foto-1.jpg" alt="Foto pertama">
          <div class="photo-caption">First Meeting</div>
        </div>

        <div class="photo-card">
          <img src="foto-2.jpg" alt="Foto Pantai Tirang">
          <div class="photo-caption">Pantai Tirang</div>
        </div>

        <div class="photo-card">
          <img src="foto-3.jpg" alt="Foto bersama">
          <div class="photo-caption">Our Little Day</div>
        </div>

        <div class="photo-card">
          <img src="foto-4.jpg" alt="Foto bersama keluarga">
          <div class="photo-caption">Mamas' World</div>
        </div>

        <div class="photo-card">
          <img src="foto-5.jpg" alt="Foto kenangan">
          <div class="photo-caption">A Little Memory</div>
        </div>

        <div class="photo-card">
          <img src="foto-6.jpg" alt="Foto favorit">
          <div class="photo-caption">My Favorite</div>
        </div>

      </div>

    </div>

  </section>


  <!-- LETTER -->

  <section class="section dark">

    <div class="container">

      <div class="center">

        <div class="eyebrow">A Letter From Sinok</div>

        <h2 class="section-title">
          Untuk Mamas.
        </h2>

      </div>

      <div class="letter">

        <p>
          Mamas,
        </p>

        <p>
          Kadang Sinok masih heran bagaimana seseorang yang
          awalnya cuma dikenal dari sebuah chat bisa menjadi
          seseorang yang begitu penting dalam hidup Sinok.
        </p>

        <p>
          Kita tidak punya awal cerita yang sempurna.
          Tidak ada pernyataan cinta yang dramatis.
          Tidak ada momen yang benar-benar seperti di film.
        </p>

        <p>
          Tapi mungkin justru itu yang membuat cerita kita
          terasa nyata.
        </p>

        <p>
          Kita tumbuh dari obrolan kecil, candaan, pertemuan,
          perjalanan, keluarga, doa, dan hari-hari sederhana
          yang akhirnya menjadi kenangan.
        </p>

        <p>
          Terima kasih sudah menjadi seseorang yang tetap ada.
          Terima kasih untuk perhatian kecil yang mungkin
          terlihat sederhana, tapi selalu Sinok ingat.
        </p>

        <p>
          Semoga perjalanan kita tidak berhenti sampai di sini.
          Semoga kita terus belajar menjadi dua orang yang
          saling menjaga, saling menguatkan, dan saling memilih.
        </p>

        <p>
          Dan kalau suatu hari nanti kita melihat kembali
          website kecil ini, Sinok ingin kita bisa tersenyum
          dan berkata:
        </p>

        <p>
          <strong>
            "Ternyata kita benar-benar berhasil sampai sejauh ini."
          </strong>
        </p>

        <div class="signature">
          Love,<br>
          Sinok ♡
        </div>

      </div>

    </div>

  </section>


  <!-- FUTURE -->

  <section class="section dark">

    <div class="container">

      <div class="center">

        <div class="eyebrow">Our Future</div>

        <h2 class="section-title">
          Masa depan yang<br>Sinok bayangkan.
        </h2>

      </div>

      <div class="future-grid">

        <div class="future-card">

          <div class="future-icon">♡</div>

          <h3>Bahagia</h3>

          <p>
            Harapan Sinok sederhana:
            semoga kita bahagia selamanya.
          </p>

        </div>


        <div class="future-card">

          <div class="future-icon">✦</div>

          <h3>Rezeki</h3>

          <p>
            Semoga kita bisa menjadi kaya,
            bukan hanya harta tapi juga
            kaya akan kebahagiaan.
          </p>

        </div>


        <div class="future-card">

          <div class="future-icon">☾</div>

          <h3>Makkah</h3>

          <p>
            Suatu hari nanti,
            Sinok ingin pergi bersama Mamas
            ke Makkah.
          </p>

        </div>


        <div class="future-card">

          <div class="future-icon">☽</div>

          <h3>Madinah</h3>

          <p>
            Berjalan bersama,
            berdoa bersama,
            dan menikmati perjalanan yang
            selama ini kita impikan.
          </p>

        </div>


        <div class="future-card">

          <div class="future-icon">💍</div>

          <h3>5 Tahun Lagi</h3>

          <p>
            Dalam bayangan Sinok,
            kita sudah menikah dan sedang
            menjalani hidup bahagia bersama.
          </p>

        </div>

      </div>

    </div>

  </section>


  <!-- GAME -->

  <section class="section light">

    <div class="container">

      <div class="center">

        <div class="eyebrow">Mini Game</div>

        <h2 class="section-title">
          Seberapa ingat<br>Mamas sama Sinok?
        </h2>

        <p>
          Jangan sampai salah ya...
        </p>

      </div>

      <div class="game-box">

        <div id="gameArea">

          <div class="question-number" id="questionNumber"></div>

          <div class="question" id="questionText"></div>

          <div class="options" id="options"></div>

          <div class="feedback" id="feedback"></div>

          <button class="next-btn" id="nextBtn" onclick="nextQuestion()">
            Lanjut →
          </button>

        </div>


        <div class="score" id="scoreArea">

          <div class="heart">♡</div>

          <h3>
            Game selesai!
          </h3>

          <p id="scoreText"></p>

          <div class="secret" id="secret">

            <h3>Secret Message</h3>

            <p>
              Kalau Mamas berhasil sampai sini...
            </p>

            <br>

            <p>
              berarti Mamas sudah melewati
              sedikit perjalanan kecil tentang kita.
            </p>

            <br>

            <p>
              Tapi ada satu hal yang nggak perlu
              ditebak dari game apa pun:
            </p>

            <br>

            <strong>
              Sinok sayang Mamas.
              Dan Sinok masih ingin melanjutkan
              cerita ini bersama Mamas. ♡
            </strong>

          </div>

        </div>

      </div>

    </div>

  </section>


  <!-- FINAL -->

  <section class="final">

    <div class="final-content">

      <div class="eyebrow">
        22 • 11 • 2026
      </div>

      <div class="heart">♥</div>

      <h2>
        Kalau boleh<br>
        memilih lagi...
      </h2>

      <p>
        Sinok tetap akan memilih Mamas.
      </p>

      <br>

      <p>
        Dari semua kemungkinan yang ada di dunia,
        Sinok bersyukur cerita kita dipertemukan.
      </p>

      <br>

      <p>
        Semoga ini bukan hanya anniversary pertama kita,
        tapi salah satu dari banyak anniversary
        yang akan kita rayakan bersama.
      </p>

      <br>

      <p>
        <strong>
          Sampai nanti kita tua bersama.
        </strong>
      </p>

    </div>

  </section>


  <div class="footer">
    Made with love by Sinok ♡ for Mamas
  </div>

</main>


<script>

/* ================= STARS ================= */

const stars = document.getElementById("stars");

for(let i=0;i<100;i++){

  const star=document.createElement("div");

  star.className="star";

  star.style.left=Math.random()*100+"%";
  star.style.top=Math.random()*100+"%";
  star.style.animationDelay=Math.random()*3+"s";

  stars.appendChild(star);
}


/* ================= OPEN WEBSITE ================= */

function openStory(){

  document.getElementById("opening").style.display="none";

  document.getElementById("main").style.display="block";

  window.scrollTo({
    top:0,
    behavior:"smooth"
  });

  playMusic();
}


/* ================= MUSIC ================= */

const music=document.getElementById("music");
const musicBtn=document.getElementById("musicBtn");

let playing=false;

function playMusic(){

  music.play()
  .then(()=>{
    playing=true;
    musicBtn.textContent="❚❚";
  })
  .catch(()=>{
    playing=false;
  });

}

musicBtn.addEventListener("click",()=>{

  if(playing){

    music.pause();
    playing=false;
    musicBtn.textContent="♫";

  }else{

    music.play();
    playing=true;
    musicBtn.textContent="❚❚";

  }

});


/* ================= GAME ================= */

const questions=[

  {
    q:"Apa warna baju Sinok saat pertama kali kita bertemu?",
    options:[
      "A. Pink",
      "B. Cream",
      "C. Putih",
      "D. Coklat"
    ],
    answer:0
  },

  {
    q:"Apa masakan pertama yang Sinok masakkan buat Mamas?",
    options:[
      "A. Nasi daun jeruk",
      "B. Sushi",
      "C. Rawon",
      "D. Soto"
    ],
    answer:2
  },

  {
    q:"Siapa yang paling sayang?",
    options:[
      "A. Sinok",
      "B. Dila",
      "C. Cantik",
      "D. Pretty"
    ],
    answer:0
  }

];

let currentQuestion=0;
let score=0;
let answered=false;

const questionNumber=document.getElementById("questionNumber");
const questionText=document.getElementById("questionText");
const options=document.getElementById("options");
const feedback=document.getElementById("feedback");
const nextBtn=document.getElementById("nextBtn");

function showQuestion(){

  answered=false;

  const q=questions[currentQuestion];

  questionNumber.textContent=
    "Pertanyaan "+(currentQuestion+1)+" dari "+questions.length;

  questionText.textContent=q.q;

  options.innerHTML="";

  feedback.textContent="";

  nextBtn.style.display="none";

  q.options.forEach((option,index)=>{

    const btn=document.createElement("button");

    btn.className="option";

    btn.textContent=option;

    btn.onclick=()=>chooseAnswer(index,btn);

    options.appendChild(btn);

  });

}


function chooseAnswer(index,button){

  if(answered) return;

  answered=true;

  const q=questions[currentQuestion];

  const all=document.querySelectorAll(".option");

  all.forEach(x=>x.disabled=true);

  if(index===q.answer){

    button.classList.add("correct");

    score++;

    feedback.textContent=
      "Benar! Mamas masih ingat detail kecil tentang Sinok 🥹♡";

  }else{

    button.classList.add("wrong");

    all[q.answer].classList.add("correct");

    feedback.textContent=
      "Yahhh... masa Mamas lupa? 😭♡";

  }

  if(currentQuestion < questions.length-1){

    nextBtn.style.display="inline-block";

  }else{

    setTimeout(showScore,900);

  }

}


function nextQuestion(){

  currentQuestion++;

  showQuestion();

}


function showScore(){

  document.getElementById("gameArea").style.display="none";

  document.getElementById("scoreArea").style.display="block";

  document.getElementById("scoreText").textContent=
    "Mamas benar "+score+" dari "+questions.length+" pertanyaan.";

  document.getElementById("secret").style.display="block";

}


showQuestion();

</script>

</body>
</html>
