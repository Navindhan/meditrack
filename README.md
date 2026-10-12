# MediTrack 360 – Smart Digital Patient History Management System

Student prototype for a State-Level Science Exhibition.
All patients, doctors, phone numbers and lab results are **fictional**.
Not clinically validated and not connected to any hospital database.

## Files

```
MediTrack360/
├── index.html        The complete website (all pages, styles and logic)
├── js/
│   ├── chart.umd.js  Chart.js 4.4.1 – lab and visit charts
│   ├── qrcode.min.js QRCode.js 1.0.0 – QR code generation
│   └── jsQR.js       jsQR 1.4.0 – reading uploaded QR images
└── README.md
```

The libraries are included, so the site also works **without internet**
(only the Google Fonts typeface falls back to the system font when offline).

## Run it on a laptop (no hosting needed)

1. Unzip the file.
2. Open the `MediTrack360` folder.
3. Double-click `index.html`. It opens in Chrome, Edge or Firefox.

## Demo logins

| Role | Staff ID | PIN | Access |
|---|---|---|---|
| Physician | `DR-2041` | `4321` | Full record, history, labs, emergency summary |
| Front desk | `FD-1107` | `2468` | Registration, identity, contact details, allergies only |

Demo Patient IDs: `PT1001`, `PT1002`, `PT1003`. New registrations get `PT1004`, `PT1005`, …

## Host it free on the internet

### Option 1 – Netlify Drop (easiest, about 2 minutes)

1. Unzip the file.
2. Go to https://app.netlify.com/drop
3. Drag the whole **MediTrack360** folder onto the page.
4. Netlify gives you a link like `https://random-name.netlify.app`.
5. Sign up for a free Netlify account (or click the claim link) so the site
   is not deleted, then in **Site configuration → Change site name** pick a
   name such as `meditrack360-demo` → `https://meditrack360-demo.netlify.app`.

To update later: open the site in Netlify → **Deploys** → drag the folder again.

### Option 2 – GitHub Pages

1. Create a free GitHub account and a new **public** repository, e.g. `meditrack360`.
2. Click **Add file → Upload files** and upload `index.html`, `README.md`
   and the `js` folder (keep the folder name). Commit.
3. Go to **Settings → Pages**, set **Source: Deploy from a branch**,
   branch **main**, folder **/ (root)**, and save.
4. After a minute the site is live at
   `https://<your-username>.github.io/meditrack360/`.

### Showing it at the exhibition

- Open the link on the laptop and press F11 for full screen.
- Make a QR code of the website link (any free QR generator) and print it
  on the stall poster so visitors can open it on their phones.
- Keep a copy on a pen drive and run `index.html` directly in case the
  venue Wi-Fi fails.

## Notes

- Registrations and the audit log are kept only in the open browser tab and
  clear when the page reloads, so no visitor data is stored anywhere.
- Sign-in runs in the browser to demonstrate the workflow. A real hospital
  system needs server-side authentication, encrypted storage and audited access.
- Ask visitors to use fictional details only when trying the registration form.
