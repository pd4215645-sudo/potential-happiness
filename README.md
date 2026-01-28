css
body {
  text-align: center;
  font-family: Arial;
}

button {
  padding: 15px;
  margin: 10px;
  font-size: 18px;
}
let time = 10;
let coins = 100;
let selectedColor = "";
script)
setInterval(() => {
  if (time > 0) {
    time--;
    document.getElementById("timer").innerText = "Time: " + time;
  } else {
    showResult();
    time = 10;
  }
}, 1000);

function selectColor(color) {
  selectedColor = color;
}

function showResult() {
  let colors = ["Red", "Green", "Violet"];
  let result = colors[Math.floor(Math.random() * colors.length)];

  if (selectedColor === result) {
    coins += 10;
    document.getElementById("result").innerText =
      "You Win! Result: " + result;
  } else {
    coins -= 10;
    document.getElementById("result").innerText =
      "You Lose! Result: " + result;
  }

  document.getElementById("coins").innerText = coins;
}
