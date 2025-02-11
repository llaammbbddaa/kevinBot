# IMPORT DISCORD.PY. ALLOWS ACCESS TO DISCORD'S API.
import discord
from random import randint

# client is the same as bot
# ENABLE INTENTS
intents = discord.Intents.default()  # Enables default intents
intents.message_content = True  # Required to read message content
# INITIALIZE THE BOT WITH INTENTS
bot = discord.Client(intents=intents)

# EVENT LISTENER FOR WHEN THE BOT HAS SWITCHED FROM OFFLINE TO ONLINE.
@bot.event
async def on_ready():
    print("kevin is ready.")

# EVENT LISTENER FOR WHEN A NEW MESSAGE IS SENT TO A CHANNEL.
@bot.event
async def on_message(message):
    gifs = ["https://tenor.com/view/meme-cow-gif-17428338243821361151", "https://tenor.com/view/smooth-move-cow-gif-16191603673901327691", "https://tenor.com/view/treyreloaded-cow-gif-8292689251618958854"]
    
    # CHECKS IF THE MESSAGE THAT WAS SENT IS EQUAL TO "HELLO".
    formatted = (message.content).lower()
    if ("hi" in formatted or "hello" in formatted):
        # SENDS BACK A MESSAGE TO THE CHANNEL.
        await message.channel.send("greetings, i am **kevin the cow**")
        await message.channel.send(gifs[randint(0, len(gifs) - 1)])

# EXECUTES THE BOT WITH THE SPECIFIED TOKEN. TOKEN HAS BEEN REMOVED AND USED JUST AS AN EXAMPLE.
bot.run("put your token here")

