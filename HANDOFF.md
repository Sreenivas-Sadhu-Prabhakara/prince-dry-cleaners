# Prince Dry Cleaners — site handoff & notes

A self-contained, single-file premium website (`index.html`) for Prince Dry Cleaners, Rajajinagar, Bengaluru. No build step, no dependencies to install — it runs by opening the file or serving the folder.

## Where the facts came from
Researched from public business listings (not invented):
- **Justdial** — Prince Dry Cleaners, near Lulu Global Mall, Rajajinagar.
- **magicpin** — Prince Dry Cleaners, Global Malls, Rajajinagar.

**Used on the site (verify before publishing):**
| Fact | Value | Confidence |
|------|-------|-----------|
| Established | 1990 | listing-sourced |
| Address | #1023, 4th M Block, Dr Rajkumar Road, near Global Mall, Rajajinagar | listing-sourced |
| Pincode | **560010** used on site | ⚠️ ambiguous — Justdial says 560010, magicpin says 560023 (Gopalapura). **Confirm the correct one.** |
| Phone | +91 80 2310 7786 | listing-sourced — **this is a landline** |
| Hours | Open 24 hours | listing-sourced |
| Rating | 4.1–4.2★, ~75 ratings | listing-sourced |
| Payments | UPI & Cash | listing-sourced |
| Services | dry cleaning, laundry, suits/blazers, curtains, blankets, carpets, mattresses, bags, soft toys | listing-sourced |

## Owner action items before going live
1. **WhatsApp (optional add)** — WhatsApp CTAs were **removed** because the listed number `+91 80 2310 7786` is a landline (WhatsApp click-to-chat needs a mobile). To add it back, wire a WhatsApp-enabled **mobile** into a `https://wa.me/91XXXXXXXXXX` button in the contact section. Until then, **Call** is the working booking channel.
2. **Testimonials** — fabricated named reviews were **removed**. The Reviews section now shows the real aggregate (4.1★, 75+ ratings) and links to the live **Justdial** listing. Optionally paste 2–3 verbatim real Google/Justdial quotes (with permission) into that section for stronger social proof.
3. **Real photos** — two marked slots (`.why-media` emblem panel; optional service imagery) are ready for real store / press-floor photos. Everything else is intentional CSS/SVG art.
4. **Confirm the pincode** (560010 vs 560023) and the exact address line.
5. **Rate card** — the pricing section says "Ask for rate." Either drop in live prices or keep the enquiry-first premium model.
6. **Contact form** — currently falls back to opening a pre-filled WhatsApp message. To collect submissions by email instead, create a free [Formspree](https://formspree.io) form and replace `your-form-id` in the form `action`.

## Deploy to GitHub Pages
```bash
cd ~/Code/Code/prince-dry-cleaners
gh repo create prince-dry-cleaners --public --source=. --remote=origin --push
# then enable Pages on the default branch:
gh api -X POST repos/:owner/prince-dry-cleaners/pages -f source[branch]=main -f source[path]=/ 2>/dev/null || \
  echo "Enable Pages in the repo Settings → Pages → Branch: main / root"
```
Live URL will be `https://<your-username>.github.io/prince-dry-cleaners/`.
