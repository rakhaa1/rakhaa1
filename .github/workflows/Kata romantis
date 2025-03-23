<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pesan Spesial Untukmu</title>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@500&display=swap" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>
  <style>
    body {
      margin: 0;
      background: url('https://feeldreams.github.io/pics/awan6.jpg') no-repeat center center fixed;
      background-size: cover;
      font-family: 'Quicksand', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      overflow: hidden;
    }
    .container {
      background: rgba(255, 255, 255, 0.15);
      border-radius: 20px;
      padding: 30px;
      max-width: 90%;
      text-align: center;
      backdrop-filter: blur(6px);
      box-shadow: 0 0 20px rgba(0,0,0,0.3);
    }
    .slide {
      display: none;
      transition: opacity 0.5s ease;
    }
    .slide.active {
      display: block;
    }
    .word-box {
      display: inline-block;
      background-color: rgba(255, 255, 255, 0.85);
      color: #333;
      margin: 5px;
      padding: 12px 16px;
      border-radius: 12px;
      font-size: 18px;
      animation: fadein 0.4s ease-in-out;
    }
    @keyframes fadein {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }
    .btn {
      background-color: #ff6faa;
      color: white;
      padding: 12px 25px;
      border: none;
      border-radius: 20px;
      margin-top: 25px;
      cursor: pointer;
      font-size: 16px;
      transition: 0.3s;
    }
    .btn:hover {
      background-color: #ff4d88;
    }
    .sticker {
      width: 90px;
      margin-bottom: 18px;
    }
  </style>
</head>
<body>

<audio autoplay loop>
  <source src="https://feeldreams.github.io/audio/janjisuci.mp3" type="audio/mpeg">
</audio>

<div class="container">
  <img src="https://feeldreams.github.io/pandapanah.gif" id="stickerImage" class="sticker" alt="sticker">
  
  <div class="slide active" id="slide1">
    <div id="words1"></div>
    <button class="btn" onclick="nextSlide()">Geser ➡️</button>
  </div>

  <div class="slide" id="slide2">
    <div id="words2"></div>
    <button class="btn" onclick="nextSlide()">Geser Lagi ➡️</button>
  </div>

  <div class="slide" id="slide3">
    <div id="words3"></div>
    <button class="btn" onclick="reply()">Balas Pesan</button>
  </div>
</div>

<script>
  const slideTexts = {
    words1: [
      "Sayangku,", "terima", "kasih", "telah", "menjadi", "cahayaku", "di", "hari-hari", "gelap.",
      "Denganmu,", "semua", "terasa", "lebih", "indah", "dan", "bermakna."
    ],
    words2: [
      "Setiap", "tatapanmu,", "setiap", "senyummu,", "selalu", "membuat", "hatiku", "tenang.", 
      "Kamu", "adalah", "rumah", "yang", "selalu", "aku", "rindukan."
    ],
    words3: [
      "Aku", "tak", "butuh", "puisi,", "karena", "hatiku", "sudah", "berisi", "namamu.", 
      "Aku", "sayang", "kamu,", "lebih", "dari", "kata-kata", "bisa", "ungkapkan."
    ]
  };

  const stickers = [
    "https://feeldreams.github.io/pandapanah.gif",
    "https://feeldreams.github.io/weee.gif",
    "https://feeldreams.github.io/pusn.gif"
  ];

  function renderWords(containerId, words) {
    const container = document.getElementById(containerId);
    container.innerHTML = "";
    words.forEach(word => {
      const box = document.createElement('span');
      box.className = 'word-box';
      box.textContent = word;
      container.appendChild(box);
    });
  }

  renderWords('words1', slideTexts.words1);
  renderWords('words2', slideTexts.words2);
  renderWords('words3', slideTexts.words3);

  let currentSlide = 1;
  function nextSlide() {
    document.getElementById('slide' + currentSlide).classList.remove('active');
    currentSlide++;
    if (stickers[currentSlide - 1]) {
      document.getElementById('stickerImage').src = stickers[currentSlide - 1];
    }
    document.getElementById('slide' + currentSlide).classList.add('active');
  }

  function reply() {
    Swal.fire({
      title: 'Balas Pesan Cintamu',
      input: 'textarea',
      inputLabel: 'Tulis balasan untukku di sini ya...',
      inputPlaceholder: 'Isi hatimu...',
      showCancelButton: true,
      confirmButtonText: 'Kirim via Whats
