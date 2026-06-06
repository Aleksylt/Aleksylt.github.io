<!DOCTYPE html>
<html>
<head>
  <script src="https://telegram.org/js/telegram-web-app.js"></script>
</head>
<body>
  <script>
    const tg = window.Telegram.WebApp;
    tg.ready(); // сообщить Telegram, что приложение загрузилось
    
    // Данные пользователя
    const user = tg.initDataUnsafe?.user;
    console.log(user.first_name);
    
    // Кнопка внизу экрана
    tg.MainButton.setText("Отправить").show();
    tg.MainButton.onClick(() => {
      tg.sendData("hello from mini app");
    });
  </script>
</body>
</html>
