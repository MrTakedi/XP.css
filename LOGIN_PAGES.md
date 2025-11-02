# Auth0 Login Pages

This repository contains custom login pages for Auth0 integration.

## Available Login Pages

### 1. shuffle-x.legacy.html
The original modern/dark-themed login page for Auth0.

**Features:**
- Bootstrap 5 based modern dark theme
- Email-based login with domain detection
- Social login buttons for multiple providers
- Help modal with SSO domain input
- Responsive design

**Providers Supported:**
- KawaiiGDN
- Xbox
- Discord
- Google
- Microsoft
- LINE
- Weibo

### 2. xp-domain-login.html
A faithful recreation of the Windows XP domain login screen.

**Features:**
- Authentic Windows XP styling using XP.css
- Classic blue gradient background
- Domain login dialog (the one that appeared after Ctrl+Alt+Del)
- Username and password fields
- Domain selector dropdown
- Help and Options buttons
- "Logging on..." animation

**Providers Supported:**
- All providers from shuffle-x.legacy.html
- VersatileNode Network (additional)

**Visual Style:**
- Windows XP Luna theme
- Classic window with title bar
- Tahoma font (authentic XP typography)
- Traditional OK/Help button layout

## Usage with Auth0

1. Navigate to your Auth0 Dashboard
2. Go to Branding → Universal Login → Advanced Options
3. Enable "Customize Login Page"
4. Copy the contents of your chosen HTML file
5. Paste into the HTML editor
6. Save changes

The `@@config@@` placeholder will be automatically replaced by Auth0 with the tenant configuration.

## Local Testing

Both pages support local testing without Auth0:

```bash
# Start a local server
python3 -m http.server 8080

# Open in browser
# For modern theme:
http://localhost:8080/shuffle-x.legacy.html

# For Windows XP theme:
http://localhost:8080/xp-domain-login.html
```

In test mode, the pages will show alerts instead of redirecting to Auth0.

## Domain Detection

Both pages support automatic domain detection from email addresses:

- `user@kawaii.gdn` → KawaiiGDN
- `user@onxbox.net` → Xbox
- `user@versatilenode.com` → VersatileNode
- `user@versatilenode.net` → VersatileNode
- `user@cgnetwork.uk` → VersatileNode
- `user@my.blufort.net` → VersatileNode

## Customization

Feel free to modify these pages to match your organization's branding:

- Update color schemes
- Modify logos and icons
- Add/remove authentication providers
- Customize help text and messages
- Add additional domain mappings

## Screenshot Comparisons

**Modern Theme (shuffle-x.legacy.html):**
- Dark, Bootstrap 5 based interface
- Modern card layout
- Icon-based provider buttons

**Windows XP Theme (xp-domain-login.html):**
- Classic Windows XP blue background
- Authentic XP window styling
- Traditional form layout
- Nostalgic user experience

Choose the theme that best matches your user base and brand identity!
