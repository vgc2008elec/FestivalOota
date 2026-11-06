# Festival Oota – Daywise Menu

Mobile menu page for Festival Oota (Cafe Chowdiah · Chowdiah Utsava, 11–15 Nov 2026).
Scanning the QR opens today's menu automatically (India time), with a Book & Pay section (UPI + WhatsApp).

## Publish on GitHub Pages (about 5 minutes)

1. Sign in at github.com → **New repository** → name it `festival-oota` → **Public** → Create.
2. Click **Add file → Upload files**, drag in `index.html` (and this README), then **Commit changes**.
3. Go to **Settings → Pages** → *Source*: **Deploy from a branch** → Branch: **main**, folder **/ (root)** → **Save**.
4. Wait 1–2 minutes. Your link is: `https://<your-github-username>.github.io/festival-oota/`
5. Open it on your phone to check, then make a QR code for that link.

## Before going live — replace the dummy payment details

Open `index.html`, search for `EDIT THESE BEFORE GOING LIVE`, and change:

```js
var CONFIG = {
  upiId: "festivaloota.demo@upi",   // ← your real UPI ID
  payeeName: "Festival Oota",       // ← name shown in the payer's UPI app
  pricePerPerson: 700,
  whatsapp: "918971862828",
  isDemo: true                      // ← set to false to hide the yellow demo banner
};
```

Also replace the UPI ID text `festivaloota.demo@upi` near `id="upiId"` (the script overwrites it anyway, but this is what shows if JavaScript is off).

The payment QR is generated on the page from these values, so it updates on its own when guests / day / meal change — no image to replace.

## Handy links
- Open a specific day: `…/festival-oota/#14` (11–15), snacks: `…/#snacks`, payment: `…/#pay`
