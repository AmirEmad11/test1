# Telegram Userbot Project

## Overview
This is a Python Telegram userbot that automatically handles join requests to a Telegram channel and sends welcome messages to new users.

## Core Components
- **bot.py**: Main bot script using Telethon library
- **requirements.txt**: Python dependencies (telethon, pyTelegramBotAPI, telethon-patch)
- **Procfile.bin**: Process configuration for deployment

## Architecture
- **Dual-client system**: User account + Bot account
- Uses Telethon-patch (enhanced Telethon) for Telegram API interaction
- **User client (@bet_store0)**: Monitors UpdatePendingJoinRequests events and auto-approves
- **Bot client (@betmanabot)**: Sends personalized welcome messages via private DM
- Separate entity resolution per client (prevents cross-session errors)
- Permission verification for both accounts

## Configuration Required
Environment variables needed:
- TELEGRAM_API_ID: Your Telegram API ID from my.telegram.org
- TELEGRAM_API_HASH: Your Telegram API hash from my.telegram.org  
- TELEGRAM_PHONE: Your phone number for authentication
- TELEGRAM_CHANNEL: Target channel ID (default: -1001672479948)

## Current Status
- ✅ **Dual-client system RUNNING** successfully in Replit environment
- ✅ **User account (@elharam110)**: Monitors and auto-approves join requests
- ✅ **Bot client (@Hacks6165_bot)**: Successfully sends private welcome messages
- ✅ Connected to channel "Cash Corner💰" (ID: 2879978778)
- ✅ Both accounts working with proper permissions
- ✅ **WORKING PERFECTLY**: Auto-approval + Private welcome messages
- ✅ **Tested successfully**: Bot operational and running
- ✅ **Setup complete**: Ready for production deployment
- ✅ **GitHub import completed**: Project fully configured in Replit environment (November 1, 2025)
- ✅ **Anti-duplication system**: Fixed duplicate welcome messages issue (November 1, 2025)

## Features Working
- ⚡ **Instant approval** of join requests via user client
- 🤖 **Dual-client architecture** - separate monitoring and messaging
- 💬 **Private welcome messages** from bot to new members
- 🛡️ **Robust error handling** and permission checking
- 📊 **Detailed logging** with client-specific tracking
- 🎆 **Rich welcome message** with channel branding and motivation
- 🔒 **Channel isolation**: Each bot instance only responds to its configured channel
- 🚫 **Duplicate prevention**: 60-second deduplication window prevents duplicate welcomes
- ✨ **Single welcome path**: Disabled ChatAction handler to prevent duplicate messages

## Deployment
- ✅ **Replit Environment Setup Complete**
- ✅ Python 3.11 installed with all dependencies
- ✅ Workflow configured as console application
- ✅ VM deployment target configured for persistent operation
- ✅ No frontend component - console-only application
- ✅ Bot running and operational in development
- ✅ Ready for production deployment

## Replit Configuration
- **Language**: Python 3.11
- **Dependencies**: telethon==1.27.0, pyTelegramBotAPI==4.12.0, telethon-patch, pytz
- **Workflow**: "Telegram Bot" - runs `python bot.py`
- **Output**: Console (shows bot logs and status)
- **Deployment**: VM target for persistent operation