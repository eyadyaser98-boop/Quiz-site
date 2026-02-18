<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>HTML & CSS Quiz</title>
<style>
body {
  font-family: Arial, sans-serif;
  background: #f4f6f8;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 800px;
  margin: 40px auto;
  background: white;
  padding: 20px 30px;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}

h1 {
  text-align: center;
}

.question {
  margin-bottom: 20px;
}

button {
  display: block;
  width: 100%;
  padding: 12px;
  font-size: 18px;
  background: #007bff;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
}

button:hover {
  background: #0056b3;
}

#result {
  margin-top: 20px;
  font-size: 22px;
  font-weight: bold;
  text-align: center;
}
</style>
</head>
<body>

<div class="container">
<h1>HTML & CSS Quiz</h1>
<form id="quizForm">

<div class="question">1. What does HTML stand for?<br>
<label><input type="radio" name="q1" value="a"> Hyper Text Markup Language</label><br>
<label><input type="radio" name="q1" value="b"> Home Tool Markup Language</label><br>
<label><input type="radio" name="q1" value="c"> Hyperlinks Text Management Language</label>
</div>

<div class="question">2. Which tag is used to create a paragraph?<br>
<label><input type="radio" name="q2" value="a"> &lt;p&gt;</label><br>
<label><input type="radio" name="q2" value="b"> &lt;para&gt;</label><br>
<label><input type="radio" name="q2" value="c"> &lt;text&gt;</label>
</div>

<div class="question">3. Which tag is used to insert an image?<br>
<label><input type="radio" name="q3" value="a"> &lt;img&gt;</label><br>
<label><input type="radio" name="q3" value="b"> &lt;image&gt;</label><br>
<label><input type="radio" name="q3" value="c"> &lt;pic&gt;</label>
</div>

<div class="question">4. CSS stands for:<br>
<label><input type="radio" name="q4" value="a"> Creative Style Sheets</label><br>
<label><input type="radio" name="q4" value="b"> Cascading Style Sheets</label><br>
<label><input type="radio" name="q4" value="c"> Computer Style Sheets</label>
</div>

<div class="question">5. Which CSS property changes text color?<br>
<label><input type="radio" name="q5" value="a"> font-color</label><br>
<label><input type="radio" name="q5" value="b"> text-color</label><br>
<label><input type="radio" name="q5" value="c"> color</label>
</div>

<div class="question">6. Which symbol is used for ID selector in CSS?<br>
<label><input type="radio" name="q6" value="a"> .</label><br>
<label><input type="radio" name="q6" value="b"> #</label><br>
<label><input type="radio" name="q6" value="c"> *</label>
</div>

<div class="question">7. Which symbol is used for class selector?<br>
<label><input type="radio" name="q7" value="a"> .</label><br>
<label><input type="radio" name="q7" value="b"> #</label><br>
<label><input type="radio" name="q7" value="c"> &</label>
</div>

<div class="question">8. Which tag creates a heading?<br>
<label><input type="radio" name="q8" value="a"> &lt;h1&gt;</label><br>
<label><input type="radio" name="q8" value="b"> &lt;head&gt;</label><br>
<label><input type="radio" name="q8" value="c"> &lt;title&gt;</label>
</div>

<div class="question">9. Which tag is used for line break?<br>
<label><input type="radio" name="q9" value="a"> &lt;break&gt;</label><br>
<label><input type="radio" name="q9" value="b"> &lt;br&gt;</label><br>
<label><input type="radio" name="q9" value="c"> &lt;lb&gt;</label>
</div>

<div class="question">10. HTML files end with extension:<br>
<label><input type="radio" name="q10" value="a"> .html</label><br>
<label><input type="radio" name="q10" value="b"> .doc</label><br>
<label><input type="radio" name="q10" value="c"> .css</label>
</div>

<button type="button" onclick="checkQuiz()">Submit Quiz</button>
</form>

<div id="result"></div>
</div>

<script>
function checkQuiz() {
  const answers = {
    q1: 'a', q2: 'a', q3: 'a', q4: 'b', q5: 'c',
    q6: 'b', q7: 'a', q8: 'a', q9: 'b', q10: 'a'
  };

  let score = 0;

  for (let key in answers) {
    const selected = document.querySelector(`input[name="${key}"]:checked`);
    if (selected && selected.value === answers[key]) {
      score++;
    }
  }

  document.getElementById('result').innerText =
    `Your score: ${score} / 10`;
}
</script>

</body>
</html>
