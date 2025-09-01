
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Special Card</title>
  <style>
    body, html {
      margin: 0;
      padding: 0;
      width: 100%;
      height: 100%;
      overflow: hidden;
      font-family: 'Bonest', cursive;
    }
    .page {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: opacity 1s ease;
    }
    .page1 { background: #ffd6e8; }
    .page2 { background: #fce4ec; opacity: 0; z-index: -1; flex-direction: column; }/* Envelope */
.envelope {
  position: relative;
  width: 220px;
  height: 140px;
  background: #fff;
  border: 2px solid #e91e63;
  overflow: hidden;
}
.flap {
  position: absolute;
  top: 0;
  left: 0;
  width: 0;
  height: 0;
  border-left: 110px solid transparent;
  border-right: 110px solid transparent;
  border-bottom: 70px solid #e91e63;
  transform-origin: top;
  transition: transform 1s ease;
  z-index: 2;
}
.envelope.open .flap {
  transform: rotateX(180deg);
}

.letter {
  position: absolute;
  top: 20px;
  left: 10px;
  width: 200px;
  height: 355px;
  aspect-ratio: 9/16;
  background: #fff;
  border: 2px solid #e91e63;
  transform: translateY(100%);
  transition: transform 2s ease, scale 1s ease;
  font-weight: bold;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  text-align: center;
}
.envelope.open .letter {
  transform: translateY(-50%) scale(1.3);
  z-index: 3;
}

.tap-text {
  position: absolute;
  top: -40px;
  width: 100%;
  text-align: center;
  font-size: 18px;
  font-weight: bold;
  font-style: italic;
  color: #e91e63;
}

/* Page 2 hearts */
.heart {
  position: absolute;
  bottom: -50px;
  font-size: 30px;
  color: pink;
  opacity: 0;
  animation: floatUp 5s linear forwards;
}
@keyframes floatUp {
  0% { transform: translateY(0); opacity: 0; }
  20% { opacity: 1; }
  100% { transform: translateY(-600px); opacity: 0; }
}
.page2-text {
  font-size: 24px;
  font-weight: bold;
  margin-top: 20px;
  color: #d81b60;
  text-align: center;
}

  </style>
</head>
<body>
  <!-- Page 1 -->
  <div class="page page1" id="page1">
    <div class="envelope" id="envelope">
      <div class="tap-text">Tap me</div>
      <div class="flap"></div>
      <div class="letter">You are so special ❤️</div>
    </div>
  </div>  <!-- Page 2 -->  <div class="page page2" id="page2">
    <div class="page2-text">With all my love 💕</div>
  </div>  <script>
    const envelope = document.getElementById('envelope');
    const page1 = document.getElementById('page1');
    const page2 = document.getElement
