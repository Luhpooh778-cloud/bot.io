# bot.io
python-telegram-bot==20.7
from telegram import Update
from telegram.ext import ApplicationBuilder, CommandHandler, ContextTypes

BOT_TOKEN = "8250106450:AAFkzjLhAxihUlKxPhMueaTCOY3xv9njNdM"

async def start(update: Update, context: ContextTypes.DEFAULT_TYPE):
    await update.message.reply_text("Bot is running! 🚀")

app = ApplicationBuilder().token(BOT_TOKEN).build()

app.add_handler(CommandHandler("start", start))

print("Bot running...")

app.run_polling()