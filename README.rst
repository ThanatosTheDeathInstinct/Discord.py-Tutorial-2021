Discord.py-Tutorial-2021
==========
How to create a discord bot using discord.py

.. image:: https://discord.com/api/guilds/336642139381301249/embed.png
   :target: https://discord.gg/r3sSKJJ
   :alt: Discord server invite
.. image:: https://img.shields.io/pypi/v/discord.py.svg
   :target: https://pypi.python.org/pypi/discord.py
   :alt: PyPI version info
.. image:: https://img.shields.io/pypi/pyversions/discord.py.svg
   :target: https://pypi.python.org/pypi/discord.py
   :alt: PyPI supported Python versions


Docs
------

- `Documentation <https://discordpy.readthedocs.io/en/latest/index.html>`_

API
-----
- `Discord API <https://discord.gg/discord-api>`_

Getting Started
------------- 
*Installing on windows and linux*

**Python 3.5.3 or higher is required**

Run the following commands:

.. code:: sh

    # Linux/macOS
    python3 -m pip install -U discord.py

    # Windows
    py -3 -m pip install -U discord.py
Discord.py with [voice]:

.. code:: sh

    # Linux/macOS
    python3 -m pip install -U "discord.py[voice]"

    # Windows
    py -3 -m pip install -U discord.py[voice]

Installing on Repl.it:
---------------
for repl.it (Run the part after the: $):

.. code:: sh
    
    #repl.it 
    ~/ThanatosBot$ pip install discord.py

Other Packages
~~~~~~~~~~~~~~~~~~

* PyNaCl (for voice support)
    
.. code:: sh

    #repl.it
    ~/ThanatosBot$ pip install PyNaCl


Examples
--------------

.. code:: py
   
   import discord

    client = discord.client(command_prefix = '!')
    @client.event
    async def on_ready(self):
        print('Logged on as', self.user)
        
    @client.event
    async def on_message(self, message):
        if message.author == self.user:
            return

        if message.content == 'hello':
            await message.channel.send('hello there!')

      client = MyClient()
      client.run('token')
bot
-----
.. code:: py

    from discord.ext import commands
    import discord
     
    client = commands.Bot(command_prefix='!', case_insensitive=True)
    @client.command()
    async def hello(ctx):
        await ctx.send(f'{member.mention} Hello!')

    bot.run('token') 



