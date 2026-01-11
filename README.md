# HouseCare Saudi Arabia — Welcome Reward

A responsive, bilingual (English/Arabic) landing page for HouseCare's welcome reward campaign.

## Features

- **Bilingual Support**: Seamless language toggle between English and Arabic (RTL layout)
- **Responsive Design**: Optimized for mobile, tablet, and desktop screens
- **Brand Cohesion**: Uses a custom color palette derived from `hclogo.jpg`
- **Modern Icons**: Font Awesome 6 icons with proper RTL support
- **Form Validation**: Client-side validation with duplicate-checking (localStorage)
- **Social Integration**: Links to HouseCare's social media (Facebook, Instagram, Snapchat, TikTok)
- **Follow Enforcement**: Snapchat follow requirement before reward eligibility
- **Success Animation**: Confetti and celebratory feedback on form submission
- **Google Sheets Integration**: Form submissions saved to a Google Apps Script endpoint

## File Structure

```
c:\Users\Lenovo\Desktop\hc
├── index.html           # Main landing page (HTML, CSS, JavaScript)
├── hclogo.jpg           # Logo/favicon image
├── README.md            # This file
└── .gitignore           # Git ignore rules
```

## Tech Stack

- **HTML5** — semantic markup
- **Tailwind CSS** (via CDN) — utility-first styling
- **Vanilla JavaScript** — form logic, translations, animations
- **Font Awesome 6** (via CDN) — professional icon library
- **Google Fonts** — Poppins (English) and Noto Kufi Arabic (Arabic)

## Responsive Breakpoints

- **Desktop**: Full layout with side-by-side elements
- **Tablet (≤768px)**: Adjusted spacing and touch-friendly controls
- **Mobile (≤640px)**: Stacked header, language toggle repositioned to top corner
- **Very small (≤380px)**: Further padding/font reductions for narrow screens

## Language & Localization

The page automatically:
- Detects and applies saved language preference (stored in localStorage)
- Switches HTML `dir` attribute (LTR ↔ RTL) when language toggles
- Translates all UI text and placeholders in real time
- Positions the language toggle on the right (LTR) or left (RTL) on mobile

## Form Features

- **Real-time Validation**: Fields validate as user types (with error messages)
- **Duplicate Prevention**: Checks if email or WhatsApp number already submitted
- **Country Code Selection**: Pre-populated dropdown with country codes for 150+ nations
- **Follow Requirement**: Checkbox enforces Snapchat follow before submission
- **Success Flow**: Displays animated success card with confetti effect
- **Demo Mode**: Restart button to submit another response

## Usage

### Local Preview

```powershell
cd c:\Users\Lenovo\Desktop\hc
python -m http.server 8000
```

Then open http://localhost:8000 in your browser.

### Language Toggle

- Click the language button (top-right on desktop, top-right/left on mobile depending on RTL) to switch between English and Arabic
- Your preference is saved to localStorage and persists across sessions

### Form Submission

1. Fill in all required fields (Full Name, Email, WhatsApp)
2. Optionally select nationality
3. Confirm you follow HouseCare on Snapchat
4. Click "Claim My Welcome Reward" to submit
5. Success card appears with animated checkmark and confetti
6. Contact information is sent to the configured Google Apps Script endpoint

## Customization

### Brand Colors

Edit the CSS `:root` variables in `index.html` to update the brand palette:

```css
:root {
    --brand-1: #0d9488; /* deep teal */
    --brand-2: #0891b2; /* cyan */
    --brand-3: #0284c7; /* sky */
    --brand-accent: #0f766e; /* darker teal */
    --brand-muted: #6b7280; /* muted gray */
}
```

### Translations

Update the `translations` object in the `<script>` section to add or modify English and Arabic strings.

### Google Apps Script Endpoint

Update `GOOGLE_SHEETS_URL` constant in the script to point to your own Google Apps Script URL for form submissions.

## Deployment

### GitHub Pages

1. Push to the `main` branch (already set up)
2. Go to **Settings** → **Pages**
3. Select **Source**: Deploy from branch → `main` → `/ (root)`
4. Click **Save** — your site will be live at `https://engrabdul.github.io/hc`

### Other Platforms

- **Netlify**: Connect repo, default settings work automatically
- **Vercel**: Connect repo, one-click deployment
- **Traditional Hosting**: Upload `index.html` and `hclogo.jpg` via FTP/SFTP

## Recent Updates

- Rebranded using hclogo color palette (CSS variables)
- Replaced inline SVGs with Font Awesome icons for better scalability
- Added comprehensive mobile responsiveness with proper RTL handling
- Made brand name translatable (shows Arabic "هاوس كير" in Arabic mode)
- Centered hero scroll indicator
- Language toggle auto-repositions based on text direction
- Fixed icon rendering in RTL mode (preserve Font Awesome fonts)
- Optimized form and button layouts for small screens

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Support

For issues or feature requests, create an issue in the GitHub repository.

---

**Repository**: [engrabdul/hc](https://github.com/engrabdul/hc)  
**Created**: January 2025  
**Last Updated**: January 11, 2026
