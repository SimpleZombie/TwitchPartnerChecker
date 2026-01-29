# Twitch Partner Checker

A simple web application to check if Twitch users have partnered status. Built with vanilla JavaScript and the Twitch API.

![image](https://imgur.com/npdTyFx.png) 

## Quick Start

1. Download the HTML file:
2. Open the file in your web browser
3. Get your Twitch API credentials (see below)
4. Enter usernames and check their partner status!

## Getting Twitch API Credentials
To use this tool, you'll need Twitch API credentials:

1. Go to Twitch Developer Console
2. Log in with your Twitch account
3. Click "Register Your Application"
4. Fill in the form:

- Name: Choose any name (e.g., "Partner Checker")
- OAuth Redirect URLs: Enter http://localhost
- Category: Select any category (e.g., "Application Integration")


5. Click "Create"
6. Copy your Client ID
7. Click "New Secret" to generate a Client Secret (copy it immediately - you won't see it again!)

## Usage

1. **Enter API Credentials**
   - Paste your Client ID and Client Secret in the provided fields

2. **Add Usernames**
   - Enter Twitch usernames, one per line
   - Example:
     ```
     Ziggylata
     croakitoad
     simplezombie
     ```

3. **Check Status**
   - Click "Check Partner Status"
   - Wait for results to load

4. **Export Results** (optional)
   - Click "Export as TXT" for a text report
   - Click "Export as CSV" for spreadsheet format


## How It Works

The application uses the [Twitch Helix API](https://dev.twitch.tv/docs/api/) to:

1. Authenticate using OAuth 2.0 Client Credentials flow
2. Query user data via the `/helix/users` endpoint
3. Check the `broadcaster_type` field:
   - `"partner"` = Partnered streamer ✅
   - `"affiliate"` or `""` = Not partnered ❌
## Browser Compatibility

Works on all modern browsers:
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Opera 76+

## API Rate Limits

The Twitch API has rate limits:
- **800 requests per minute** per Client ID
- The app includes a 100ms delay between requests to stay within limits

For large batches (100+ users), the check may take a few minutes. (I typically run 1000+ at a time and it takes around 5 minutes)

## Troubleshooting

### "Failed to authenticate with Twitch API"
- Double-check your Client ID and Client Secret
- Make sure you copied them correctly (no extra spaces)
- Verify your app is registered at dev.twitch.tv/console

### "User not found"
- The username may not exist
- Check for typos in the username
- Twitch usernames are case-insensitive
## Acknowledgments

- Built with the [Twitch API](https://dev.twitch.tv/docs/api/)
- Fonts: [Google Fonts](https://fonts.google.com/)

## Support

If you encounter any issues or have questions:
- Open an issue on GitHub
- Check the [Twitch API Documentation](https://dev.twitch.tv/docs/api/)
- Follow [SimpleZombie on Twitch](https://twitch.tv/simplezombie)

---
**Note**: This tool is not affiliated with, endorsed by, or sponsored by Twitch.
