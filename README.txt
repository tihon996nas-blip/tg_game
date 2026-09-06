V4 — DIRECT MINI APP

Why this version is different:
- It does NOT use Telegram HTML5 Game / InlineQueryResultGame.
- It does NOT use tg://resolve?startapp for the Main Mini App.
- It uses a named Direct Mini App link:
  https://t.me/autumn_cabinet_game_bot/autumn?startapp=play&mode=compact

Before running V4, create the named app in @BotFather:

1. Send /newapp
2. Choose @autumn_cabinet_game_bot
3. Title: Осенний Шкаф
4. Description: Игра — найдите промокод за 3 попытки
5. Upload any suitable app image when BotFather requests it
6. GIF/video: /empty if you do not want to add one
7. Web App URL:
   https://tihon996nas-blip.github.io/tg_game/
8. Short name: autumn

The short name MUST be exactly:
autumn

Then:
- Keep the existing Main Mini App if you want; it does not need to be removed.
- Replace run_bot.py with this V4 file.
- Restart the bot:
  python run_bot.py
- Send a NEW inline game message before testing.

Important about mobile height:
mode=compact requests compact/partial height from Telegram.
HTML/CSS cannot resize Telegram's native WebView container itself.
If a Telegram client ignores compact mode, making .game-container shorter
will only make the page content shorter; it will not reveal the real chat
behind the WebView.
