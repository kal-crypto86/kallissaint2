<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <title>Interaktif by chikal</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(120deg,blue,white);
      font-family: 'Courier New', monospace;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }

    #container {
      background-color: rgba(255, 255, 255, 0.9);
      padding: 30px 40px;
      border-radius: 15px;
      max-width: 700px;
      box-shadow: 0 0 20px rgba(0,0,0,0.3);
    }

    #output {
      font-size: 1.2em;
      white-space: pre-wrap;
      line-height: 1.6;
      margin-bottom: 20px;
      color: black;
      min-height: 150px;
      border-left: 3px solid #000;
      padding-left: 10px;
      position: relative;
    }

    #output::after {
      content: '|';
      position: absolute;
      right: 10px;
      animation: blink 1s steps(2, start) infinite;
      opacity: 0.7;
    }

    @keyframes blink {
      50% {
        opacity: 0;
      }
    }

    button {
      padding: 10px 20px;
      font-size: 1em;
      border: none;
      border-radius: 5px;
      background-color: black;
      color: white;
      cursor: pointer;
    }

    button:hover {
      background-color: #333;
    }

    #footer {
      font-size: 12px;
      color: gray;
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <div id="container">
    <div id="output"></div>
    <button onclick="startTyping()">🔁 Ulangi</button>
    <a href="file:///C:/Users/Administrator/OneDrive/Dokumen/punya%20chikal/learn4.html">She's Thunderstorm</a>
    <a href="file:///C:/Users/Administrator/OneDrive/Dokumen/punya%20chikal/learn3.html">Pemuja Rahasia</a>
    <a href="file:///C:/Users/Administrator/OneDrive/Dokumen/punya%20chikal/learn.html">Sweet</a>
    <div id="footer">Website interaktif by chikal✨</div>
  </div>

  <script>
    const lines = [
      "Your beauty glows like moonlight on a quiet sea,",
      "A silent charm that sets restless hearts free.",
      "Eyes like stars, too deep to ever flee,",
      "Grace in each breath pure poetry to me.",
      "",
      "These songs for u"
    ];

    const output = document.getElementById("output");
    let lineIndex = 0;
    let charIndex = 0;
    const delay = 40;
    const pause = 1200;

    function typeLine() {
      if (lineIndex >= lines.length) return;

      const currentLine = lines[lineIndex];
      if (charIndex < currentLine.length) {
        output.innerHTML += currentLine.charAt(charIndex);
        charIndex++;
        setTimeout(typeLine, delay);
      } else {
        output.innerHTML += "\n";
        lineIndex++;
        charIndex = 0;
        setTimeout(typeLine, pause);
      }
    }

    function startTyping() {
      output.innerHTML = "";
      lineIndex = 0;
      charIndex = 0;
      setTimeout(typeLine, 1000);
    }

    // mulai otomatis saat halaman dibuka
    startTyping();
  </script>
</body>
</html>v
