# Python-Discord-Bot
```py
import discord
from discord.ext import commands

bot = commands.Bot(command_prefix='!', intents=discord.Intents.all())

@bot.event
async def on_ready():
    print("Bot is up")
  
@bot.command()
async def test(ctx): 
        embed = discord.Embed(title='', description='the bot is working')
        await ctx.send(embed=embed)

@bot.command()
async def ping(ctx):
    latency = bot.latency
    embed = discord.Embed(title='Pong!', description=f'Latency: {round(latency * 1000)}ms')
    await ctx.send(embed=embed)

bot.run("your bot token") # https://discord.com/developers/applications
```
