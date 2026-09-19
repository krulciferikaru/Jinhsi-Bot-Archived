# Jinhsi Bot (Archived)

A Discord bot providing information about **Wuthering Waves** — resonators, builds, weapons, echoes, and skills — via slash commands. Inspired by Cogs Bot.

> **Archived:** this project is no longer actively maintained.

## Features

- `/build <resonator>` — Shows a resonator's recommended build (echo set, main/sub echoes, stats priority), with a dropdown to switch between build variants. Includes Rover element/path selection.
- `/echo <name>` — Shows an echo's cost, class, sonata effect, and description.
- `/weapon <name>` — Shows a weapon's stats and description.
- `/skill <resonator> [skill]` — Shows a resonator's skills (Basic Attack, Resonance Skill, Liberation, Forte Circuit, Inherent Skills, Intro/Outro, Resonance Chain), with category/skill selectors.
- `/resonatorlist [sort_by]` — Paginated list of all resonators, sortable by element, weapon, or star.
- `/echolist [sort_by]` — Paginated list of all echoes, sortable by class, cost, or sonata effect.
- `/weaponlist [sort_by]` — Paginated list of all weapons, sortable by weapon type or star.
- `/help` — Overview of available commands.
- `/ping` — Bot latency.
- `/sync` — Manually re-syncs slash commands with Discord.

All character/echo/weapon data is defined in [data/](data/), and each feature is implemented as a separate cog in [cogs/](cogs/).

## Requirements

- Python 3.12+
- [discord.py](https://discordpy.readthedocs.io/)
- python-dotenv

Install dependencies:

```bash
pip install discord.py python-dotenv
```

## Setup

1. Create a `.env` file in the project root with your bot token:

   ```
   bottoken=YOUR_DISCORD_BOT_TOKEN
   ```

2. Run the bot:

   ```bash
   python wuwabot.py
   ```

On startup, the bot loads every cog in [cogs/](cogs/) and syncs its slash commands with Discord. The default command prefix for legacy/hybrid commands is `=`.

## Project Structure

```
wuwabot.py     # Entry point: loads cogs, starts the bot
config.py      # Loads the bot token from .env
cogs/          # One file per slash command / feature
data/          # Static game data (resonators, echoes, weapons, skills, emojis)
```
