# Sabahosh
Bot-sabamolodi
     git add .
     git commit -m "توضیح درباره تغییرات"
     git push origin main
from telegram import Update
from telegram.ext import ApplicationBuilder, CommandHandler, ContextTypes

async def start(update: Update, context: ContextTypes.DEFAULT_TYPE):
    await update.message.reply_text('سلام! من رباتم، چطور می‌تونم کمکت کنم؟')

app = ApplicationBuilder().token('توکن_ربات_تو_اینجا').build()

app.add_handler(CommandHandler('start', start))

app.run_polling()
     
