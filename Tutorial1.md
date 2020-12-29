## Кастомный help на Discord.py
Весь прикол в том, чтобы убрать встроеную help команду, но придётся самим писать help.
Вообще чтоб провернуть советую пользоваться кастомным пресетом, он есть в VSCode в плагинах на пресеты discord.py, но я просто попозже ещё сделаю чисто файл с пресетом этим.
## Ладно, приступаем
**1. Дописываем bot = commands.Bot(command_prefix=PREFIX, intents=INTENTS).** Тут всё легко, просто дописываем help_command=None и всё.
**2. Пишем help.** Я лично сделал так. Бот у меня маленький, терять нечего.

@bot.command()
async def help(ctx):
    embed = discord.Embed(title='Помощь', description='''
    say - Бот скажет это через Embed (не робит)
    about - О Боте
    help - Выводит данное сообщение''')
    embed.set_author(name='-- Galactic (Canary) --')
    embed.set_footer(name="Привет")
    await ctx.send( embed = embed )

Вообще вы можете ещё своего дописать, т.ч. похуй.

## ГОТОВО
