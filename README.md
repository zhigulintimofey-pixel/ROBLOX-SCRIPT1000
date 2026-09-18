<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<title>Вирус 😈</title>
<style>
  body {
    background: black;
    color: red;
    font-family: monospace;
    text-align: center;
    padding-top: 20vh;
  }
  #box {
    font-size: 28px;
  }
  #bar {
    width: 70%;
    height: 30px;
    border: 2px solid red;
    margin: 30px auto;
  }
  #progress {
    height: 100%;
    width: 0%;
    background: red;
  }
</style>
</head>
<body>

<div id="box">⚠️ ОБНАРУЖЕН ВИРУС ⚠️</div>
<div id="bar"><div id="progress"></div></div>
<div id="percent">Сканирование: 0%</div>

<script>
let p = 0;

let timer = setInterval(() => {
  p++;
  document.getElementById("progress").style.width = p + "%";
  document.getElementById("percent").textContent =
    "Сканирование: " + p + "%";

  if (p >= 100) {
    clearInterval(timer);
    document.getElementById("box").textContent =
      "😂 ЭТО БЫЛ ПРИКОЛ! ВИРУСА НЕТ";
    document.getElementById("box").style.color = "lime";
    document.getElementById("percent").textContent =
      "Ваш компьютер в безопасности 👍";
  }
}, 50);
</script>

</body>
</html>
