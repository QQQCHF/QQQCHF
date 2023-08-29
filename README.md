- 👋 Hi, I’m @QQQCHF
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
QQQCHF/QQQCHF is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

   pip install python-telegram-bot

   python
   from telegram.ext import Updater, CommandHandler

   def start(update, context):
       context.bot.send_message(chat_id=update.effective_chat.id, text="Welcome to the Quiz Vote Bot!")

   def vote(update, context):
       # Vote logic here
       context.bot.send_message(chat_id=update.effective_chat.id, text="Thank you for voting!")

   def main():
       updater = Updater(token='YOUR_BOT_TOKEN', use_context=True)
       dispatcher = updater.dispatcher

       start_handler = CommandHandler('start', start)
       vote_handler = CommandHandler('vote', vote)

       dispatcher.add_handler(start_handler)
       dispatcher.add_handler(vote_handler)

       updater.start_polling()

   if __name__ == '__main__':
       main()

   
