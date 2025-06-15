# <!DOCTYPE html>
<html>
<head>
  <title>Rock Paper Scissors Game</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 50px;
    }
    button {
      font-size: 20px;
      padding: 10px 20px;
      margin: 10px;
    }
    #result {
      margin-top: 30px;
      font-size: 24px;
    }
  </style>
</head>
<body>

  <h1>Rock Paper Scissors</h1>

  <button onclick="play('rock')">🪨 Rock</button>
  <button onclick="play('paper')">📄 Paper</button>
  <button onclick="play('scissors')">✂️ Scissors</button>

  <div id="result"></div>

  <script>
    function play(playerChoice) {
      const choices = ['rock', 'paper', 'scissors'];
      const computerChoice = choices[Math.floor(Math.random() * 3)];

      let result = "";

      if (playerChoice === computerChoice) {
        result = "It's a draw!";
      } else if (
        (playerChoice === 'rock' && computerChoice === 'scissors') ||
        (playerChoice === 'paper' && computerChoice === 'rock') ||
        (playerChoice === 'scissors' && computerChoice === 'paper')
      ) {
        result = "You win!";
      } else {
        result = "You lose!";
      }

      document.getElementById("result").innerHTML =
        `<p>You chose <b>${playerChoice}</b>. Computer chose <b>${computerChoice}</b>.</p><p><strong>${result}</strong></p>`;
    }
  </script>

</body>
</html>
Rock-paper-scissors-game
