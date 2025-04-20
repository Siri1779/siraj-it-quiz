<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Siraj Garakhanov – IT Ausbildung</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; background-color: #111; color: #fff; }
    header { background-color: #1a1a1a; padding: 2rem; text-align: center; }
    h1 { font-size: 2.5rem; color: #4dd0e1; }
    nav { text-align: center; margin-bottom: 2rem; }
    nav a { color: #4dd0e1; margin: 0 1rem; text-decoration: none; }
    section { max-width: 800px; margin: auto; padding: 2rem; }
    .button { display: inline-block; padding: 0.8rem 1.5rem; background-color: #4dd0e1; color: #000; border: none; text-decoration: none; border-radius: 8px; }
    .quiz-container { background: #222; padding: 1rem; border-radius: 10px; }
    .question { margin: 1rem 0; }
    .result { margin-top: 1rem; font-weight: bold; color: #4dd0e1; }
  </style>
</head>
<body>

<header>
  <h1>Siraj Garakhanov</h1>
  <p>IT-begeistert & auf der Suche nach einer Ausbildung im Bereich Informationstechnologie</p>
  <nav>
    <a href="#about">Über mich</a>
    <a href="#quiz">IT-Quiz</a>
    <a href="#cv">Lebenslauf</a>
    <a href="#contact">Kontakt</a>
  </nav>
</header>

<section id="about">
  <h2>Über mich</h2>
  <p>Ich heiße Siraj Garakhanov und bin begeistert von allem, was mit IT zu tun hat. Schon während meiner Schulzeit habe ich mich intensiv mit Informatik beschäftigt. Ich liebe es, kreative Ideen in funktionierende digitale Lösungen zu verwandeln. Mein Ziel ist es, eine Ausbildung im Bereich Informationstechnologie zu absolvieren und meine Fähigkeiten weiterzuentwickeln.</p>
</section>

<section id="quiz">
  <h2>IT-Quiz</h2>
  <div class="quiz-container">
    <div class="question">
      <p>1. Wofür steht die Abkürzung "IP"?</p>
      <button onclick="checkAnswer(this, true)">Internet Protocol</button>
      <button onclick="checkAnswer(this, false)">Internal Program</button>
    </div>
    <div class="question">
      <p>2. Welche Sprache wird typischerweise für Webentwicklung genutzt?</p>
      <button onclick="checkAnswer(this, true)">HTML</button>
      <button onclick="checkAnswer(this, false)">C++</button>
    </div>
    <div class="question">
      <p>3. Was ist RAM?</p>
      <button onclick="checkAnswer(this, true)">Ein flüchtiger Speicher</button>
      <button onclick="checkAnswer(this, false)">Ein dauerhaftes Speichergerät</button>
    </div>
    <div class="result" id="result"></div>
  </div>
</section>

<section id="cv">
  <h2>Lebenslauf</h2>
  <p>Hier können Sie meinen Lebenslauf als PDF herunterladen:</p>
  <a class="button" href="Lebenslauf.Sirac%2052.pdf" download>PDF herunterladen</a>
</section>

<section id="contact">
  <h2>Kontakt</h2>
  <p>Email: <a href="mailto:siradzgarahanov8@gmail.com">siradzgarahanov8@gmail.com</a></p>
  <p>Telefon: +49 176 17959839</p>
  <p>Ort: Gießen</p>
</section>

<script>
  let score = 0;
  let total = 3;

  function checkAnswer(button, correct) {
    if (button.classList.contains("answered")) return;
    button.classList.add("answered");
    if (correct) score++;
    button.style.backgroundColor = correct ? '#4caf50' : '#e57373';

    const all = document.querySelectorAll(".question button");
    const answered = [...all].filter(btn => btn.classList.contains("answered"));
    if (answered.length === total * 2) {
      document.getElementById("result").innerText = `Dein Ergebnis: ${score}/${total} korrekt!`;
    }
  }
</script>

</body>
</html>
