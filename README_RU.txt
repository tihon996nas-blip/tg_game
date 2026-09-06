ОСЕННИЙ ШКАФ — COMPACT V2

Что изменено:
- Игра остается Telegram Mini App, а НЕ Telegram HTML5 Game.
- Telegram.WebApp.close() продолжает работать для крестика и кнопок выхода.
- Нет TelegramGameProxy, sendData и shareScore, поэтому список контактов для репоста не вызывается.
- Из ссылки запуска убраны startapp=play и mode=compact — она теперь максимально простая для Telegram Desktop:
  https://t.me/autumn_cabinet_game_bot?startapp
- Compact mode нужно задать как режим запуска MAIN MINI APP в @BotFather.
- В сообщении оставлена резервная кликабельная ссылка на случай клиентского бага кнопки в Telegram Desktop.

НАСТРОЙКА:
1. GitHub Pages: заменить index.html на файл из этого архива.
2. @BotFather: открыть настройки autumn_cabinet_game_bot.
3. Для MAIN MINI APP оставить URL:
   https://tihon996nas-blip.github.io/tg_game/
4. В настройках режима запуска Main Mini App выбрать COMPACT.
   Важно: не Fullscreen и не Full size/default, а Compact.
5. На компьютере заменить run_bot.py на файл из архива.
6. Запустить:
   python run_bot.py
7. Проверить в любом чате через @autumn_cabinet_game_bot.

ВАЖНО ПРО TELEGRAM:
Если на Android после настройки Compact приложение всё равно открывается на всю высоту, обновите Telegram до актуальной версии. У Telegram был отдельный клиентский баг, при котором mode=compact игнорировался на Android. Это не исправляется JavaScript-кодом страницы: WebApp API умеет расширять окно через expand(), но не умеет принудительно уменьшать уже открытый full-height контейнер.
