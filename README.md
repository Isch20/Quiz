# Quiz

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>People in Power – UK Quiz</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f6f8;
      margin: 0;
      padding: 0;
    }
    .container {
      max-width: 700px;
      margin: 40px auto;
      background: #ffffff;
      padding: 30px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    h1 {
      text-align: center;
    }
    .question {
      margin-bottom: 20px;
    }
    button {
      display: block;
      margin: 30px auto;
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
    }
    .result {
      text-align: center;
      font-size: 18px;
      font-weight: bold;
    }
  </style>
</head>
<body>

<div class="container">
  <h1>People in Power – UK Government Quiz</h1>

  <form id="quizForm">

    <div class="question">
      <p><strong>1. Who is the current Prime Minister of the United Kingdom?</strong></p>
      <input type="radio" name="q1" value="A"> Boris Johnson<br>
      <input type="radio" name="q1" value="B"> Theresa May<br>
      <input type="radio" name="q1" value="C"> Keir Starmer<br>
      <input type="radio" name="q1" value="D"> David Cameron
    </div>

    <div class="question">
      <p><strong>2. Which of the following is NOT one of the Great Offices of State?</strong></p>
      <input type="radio" name="q2" value="A"> Prime Minister<br>
      <input type="radio" name="q2" value="B"> Chancellor of the Exchequer<br>
      <input type="radio" name="q2" value="C"> Home Secretary<br>
      <input type="radio" name="q2" value="D"> Mayor of London
    </div>

    <div class="question">
      <p><strong>3. Who officially appoints the Prime Minister?</strong></p>
      <input type="radio" name="q3" value="A"> The British public<br>
      <input type="radio" name="q3" value="B"> The Monarch<br>
      <input type="radio" name="q3" value="C"> House of Lords<br>
      <input type="radio" name="q3" value="D"> Supreme Court
    </div>

    <div class="question">
      <p><strong>4. What is the name of the British national legislature?</strong></p>
      <input type="radio" name="q4" value="A"> Congress<br>
      <input type="radio" name="q4" value="B"> Bundestag<br>
      <input type="radio" name="q4" value="C"> Parliament<br>
      <input type="radio" name="q4" value="D"> Senate
    </div>

    <div class="question">
      <p><strong>5. What is the main responsibility of the Chancellor of the Exchequer?</strong></p>
      <input type="radio" name="q5" value="A"> Foreign policy<br>
      <input type="radio" name="q5" value="B"> Domestic security<br>
      <input type="radio" name="q5" value="C"> Economy and finance<br>
      <input type="radio" name="q5" value="D"> Defence
    </div>

    <button type="button" onclick="checkAnswers()">Submit Quiz</button>
  </form>

  <div class="result" id="result"></div>
</div>

<script>
  function checkAnswers() {
    const answers = {
      q1: "C",
      q2: "D",
      q3: "B",
      q4: "C",
      q5: "C"
    };

    let score = 0;
    let total = 5;

    for (let question in answers) {
      const selected = document.querySelector(`input[name="${question}"]:checked`);
      if (selected && selected.value === answers[question]) {
        score++;
      }
    }

    document.getElementById("result").innerText =
      `You scored ${score} out of ${total}.`;
  }
</script>

</body>
</html>
