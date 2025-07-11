# Mobile Testing Setup

## Option 1: Using Live Server (Recommended)

The development server is already running on `http://localhost:3000`

### For iPhone/iPad:

1. Make sure your phone and computer are on the same WiFi network
2. Find your computer's IP address:
   ```bash
   ifconfig | grep "inet " | grep -v 127.0.0.1
   ```
3. On your phone, open Safari and go to: `http://[YOUR_IP]:3000/doubles_ping_pong.html`

### For Android:

1. Same steps as above, but use Chrome or any browser
2. Go to: `http://[YOUR_IP]:3000/doubles_ping_pong.html`

## Option 2: Using ngrok (Public URL)

If you want to test from anywhere:

1. Install ngrok: `npm install -g ngrok`
2. In a new terminal: `ngrok http 3000`
3. Use the provided public URL on any device

## Option 3: Python Server (Alternative)

If live-server doesn't work:

```bash
# Python 3
python3 -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

Then access: `http://[YOUR_IP]:8000/doubles_ping_pong.html`

## Development Workflow

1. The live server automatically reloads when you save changes
2. Test on desktop first, then mobile
3. Changes are reflected immediately on both devices

## Troubleshooting

- If connection fails, check firewall settings
- Make sure both devices are on same network
- Try using ngrok for public access
