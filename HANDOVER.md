# SYSTEM HANDOVER — Probal Portfolio Website

## Who
K M Abdullah Probal — BBA Marketing (University of Dhaka), research intern at Akij Ventures (FMCG), co-founder & CMO of dusupershop.com, CSCA 92%, published researcher, built StoryVocabs (storyvocabs.vercel.app — NOT netlify).
Contact: WhatsApp +8801627472887 · official.kmap@gmail.com · linkedin.com/in/k-m-abdullah-probal

## What exists (DONE — do not rebuild)
`F:\Freelancing\portfolio_site\`
- `index.html` — single-file site, all CSS/JS inline, no frameworks, no localStorage.
- `assets/` — probal.jpg (hero portrait, upscaled 2x, writings removed), duss-logo.png (DU SuperShop wordmark), bnb-logo.png, toma-cover.jpg, toma-process.jpeg, deliverables.jpeg, aggregator.jpg, ovc.jpg, tfj.jpg. (Unused leftovers: *.png copies of probal/toma-cover/aggregator — safe to delete manually.)

### Site structure
1. Hero — name, tagline, WhatsApp + "Book a Service" buttons, photo with 6 floating achievement chips (one chip auto-rotates via FEATS array: HSBC semi-finalist, EduPro Global 2nd Runner-up, Battle of Minds, 13 research teams) + nameplate.
2. Credentials marquee (infinite scroll).
3. Services ×3: Business Websites (BDT 15,000, 3 days) · Content Packages (BDT 4,000/mo) · Data Analysis & Dashboards (project-based). Each has "Book this" button.
4. Portfolio — `PROJECTS` JS array at top of file ({title, category, description, tools, result, image, logoThumb, badge, link}), rendered dynamically, comment template "// ADD NEW PROJECT" for editing in Notepad. 9 case studies, clients anonymised.
5. Process (4 steps), About (animated counters + collapsible "Competition record & honours" vault), Contact, footer.

### Booking system (frontend only — THIS IS WHERE BACKEND WORK STARTS)
- Modal: service picker + name/business/day/time/note → builds structured message → opens wa.me/8801627472887 prefilled, or mailto.
- `CALENDAR_URL` const at top of index.html: currently "". If set to a Google Calendar appointment-schedule link, a "Book a free 15-min call" button auto-appears in the modal.

## Rules (keep following)
- Anonymise client names; present client work as case studies (tools + outcome).
- Never mention assignments/theses/academic submissions — position as business/survey data analysis, content, websites.
- Design: deep teal accent (#0d5c5c / #14b8a6), premium, mobile-first.
- Token-efficient: minimal replies, no questions unless blocking.

## Next session goals (backend)
1. Google Calendar appointment schedule → paste link into `CALENDAR_URL`.
2. Optional: form backend (e.g., Formspree/Netlify Forms) so bookings also land in email without WhatsApp.
3. Deploy: drag `portfolio_site` folder to https://app.netlify.com/drop (or Vercel). Then update any hardcoded URLs if a custom domain is added.
4. SEO after deploy: submit to Google Search Console.

## Visual audit notes
Chrome extension can't open file:// URLs unless "Allow access to file URLs" is enabled (it was enabled on this machine). Hard-reload (ctrl+shift+r) needed after asset changes — images cache aggressively.
