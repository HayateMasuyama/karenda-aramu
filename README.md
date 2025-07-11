<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>アラーム設定</title>
  <style>
    body {
      font-family: sans-serif;
      text-align: center;
      padding: 50px;
    }
    input, button {
      font-size: 1.2em;
      padding: 10px;
      margin: 10px;
    }
  </style>
</head>
<body>
  <h1>アラームを設定する</h1>

  <label for="alarmTime">アラーム時間を選んでください：</label><br>
  <input type="time" id="alarmTime"><br>
  <button onclick="setAlarm()">アラームを設定</button>

  <p id="message"></p>

  <button onclick="location.href='karenda.html'">カレンダーに戻る</button>

  <script>
    function setAlarm() {
      const time = document.getElementById('alarmTime').value;
      if (!time) {
        document.getElementById('message').textContent = "時間を選んでください。";
        return;
      }

      document.getElementById('message').textContent = "アラームを " + time + " に設定しました（※実際の音は鳴りません）。";
      // 実際の通知機能をつける場合は、Service Worker などが必要です
    }
  </script>
</body>
</html>
