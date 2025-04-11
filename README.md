Here's a comprehensive combined README.md incorporating both the main bot features and pairing code setup:

```markdown
# 🤖 IMRAN WhatsApp Bot - Video Downloader

![Banner](https://i.ibb.co.com/mCLq42Nb/1744278640997.jpg)

A multifunctional WhatsApp bot with video downloading capabilities and AI chat features. Supports both QR code and pairing code authentication methods.

## ✨ Key Features
- 🎥 **Multi-platform Video Downloader** (Facebook, Instagram, TikTok, YouTube)
- 🔐 **Multiple Auth Methods** (QR Code/Pairing Code/Mobile Mode)
- 💬 **Smart AI Chat** (SimSimi integration)
- ⚡ **Quick Commands** (20+ built-in commands)
- 🔄 **Auto-session Management** (With backup/restore)
- 👥 **Group Management Tools** (Info, Moderation)

## 🚀 Installation

### Prerequisites
- Node.js v16+
- npm
- WhatsApp-enabled number
- Stable internet connection

```bash
git clone https://github.com/MR-IMRAN-60/WP-VIDDOWN-BOT.git
cd imran-whatsapp-bot
npm install
```

## 🔐 Setup Guide

### 1. Configuration
Create `config.json`:
```json
{
  "ownerNumber": "8801XXXXXXXXX",
  "botName": "IMRAN-BOT"
}
```

### 2. Authentication Methods

#### Method 1: Pairing Code (Recommended)
```bash
npm start
```
1. Enter number in international format when prompted:
   ```bash
   📞 Enter your WhatsApp number (with country code): +8801712XXXXXX
   ```
2. Get 8-digit pairing code:
   ```bash
   🔑 Your Pairing Code: 1234-5678
   ```
3. In WhatsApp:  
   `Settings → Linked Devices → Link a Device → Use Phone Number`
4. Enter code **without hyphens**

#### Method 2: QR Code
```bash
npm start
```
Scan generated QR code through:  
`WhatsApp → Linked Devices → Link a Device`

#### Method 3: Mobile Mode (Existing session)
```bash
npm start -- --mobile
```

## ⌨️ Basic Commands
| Command          | Description                  | Access     |
|------------------|------------------------------|------------|
| `ping`           | Check bot status             | All        |
| `time`/`সময়`     | Show current time            | All        |
| `owner`          | Display owner info           | All        |
| `groupinfo`      | Group metadata               | Groups     |
| `shutdown`       | Stop bot                     | Owner only |
| [Video URL]      | Auto-download video          | All        |

## 🎥 Video Download Guide
1. Send any supported platform link:
   ```bash
   https://www.facebook.com/reel/12345
   ```
2. Bot will process and send video within 1 minute

**Supported Platforms**:
- Facebook (Reels/Posts)
- Instagram (Reels/Posts)
- TikTok (All formats)
- YouTube (Shorts/Videos)

## ⚙️ Configuration Options
| Parameter        | Description                  | Default    |
|------------------|------------------------------|------------|
| `ownerNumber`    | Bot owner's number           | Required   |
| `botName`        | Display name                 | "IMRAN-BOT"|
| `sessionPath`    | Session storage location     | ./sessions |

## 🔄 Session Management
- Automatic daily backups
- Session stored in `./sessions/creds.json`
- Backup copy: `creds.backup.json`
- To reset: Delete session files and restart

## 🚨 Troubleshooting

### Common Issues
| Error                        | Solution                     |
|------------------------------|------------------------------|
| Invalid number format        | Use +[countrycode][number]   |
| Pairing code expired         | Generate new code            |
| Video download failed        | Check URL validity           |
| Session connection issues    | Delete session and re-auth    |

### Advanced Fixes
1. Update dependencies:
   ```bash
   npm update
   ```
2. Clear cache:
   ```bash
   rm -rf node_modules && npm install
   ```
3. Check API status:
   ```bash
   ping api.simsimi.com
   ```

## ⚠️ Important Notes
- Session files contain sensitive credentials - keep private
- Pairing codes expire in 2 minutes
- Mobile mode requires existing valid session
- Regular backups recommended

## 📜 License
MIT License - Use responsibly. Not affiliated with WhatsApp/Facebook.

---

**Maintained by Imran** | [Report Issues](https://github.com/MR-IMRAN-60/WP-VIDDOWN-BOT/issues)  
**Need Help?** Contact: [WhatsApp](https://wa.me/8801689903267)
```

This README combines:
1. Core bot functionality documentation
2. Detailed pairing code setup instructions
3. Comprehensive troubleshooting guide
4. Configuration references
5. Usage examples

Key improvements:
- Unified authentication methods section
- Combined troubleshooting table
- Clear command reference
- Video download specifics
- Better visual hierarchy
- Maintenance information

For deployment, remember to:
1. Replace placeholder URLs with actual repository links
2. Update contact information
3. Add proper license file
4. Include any required API keys documentation
