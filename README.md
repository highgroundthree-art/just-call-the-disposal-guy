# Just Call the Disposal Guy

Phoenix-metro garbage disposal swap-out service. Two models, flat installed price, plug-in units only, booked online with a deposit.

**Business name (decided 2026-11-16):** Just Call the Disposal Guy. Older plan documents still say "Just the Disposal Guy" and should be updated.

## In this repo

| Path | What it is |
|---|---|
| `site/` | **The live website.** `index.html` (home page and booking form) and `booked.html` (thank-you page). Hosted on Netlify; see Going live below. |
| `netlify.toml` | Tells Netlify to publish the `site/` folder. |
| `docs/business-plan.md` | Business plan and SBA loan request (draft, Nov 15, 2026): pricing, $200/$100 split, 3-year projections, sensitivity, $16,000 loan. |
| `website/design-source/landing-page.dc.html` | Landing page design (hero, two-model pricing, how it works, rules, under-sink photo guide, booking). Design-canvas source with template fields; it becomes the public site in the next step. |

## Working documents (private, kept as living docs in Claude)

These stay in Claude where they can still be edited. They do not belong on a public site.

- Business Plan and Loan Request: https://claude.ai/artifact/3uG4zvdTh5q7QmaW1stj5u
- Business Handoff: https://claude.ai/artifact/QsNvQ1ZtSzXMdC2XUqeVUW
- Operations Structure: https://claude.ai/artifact/RfeYoqUXY546bExmkJymDt
- Automation Map & Amazon Business API Application: https://claude.ai/artifact/8pxx6EtLy57KnZNXoKTKmn
- Operator Scope of Work, Phased Rollout: https://claude.ai/artifact/Mg1iJrhRSHNaw1mXwbDHkw

To keep a frozen copy here, open a doc, use Export → PDF, then upload it to `docs/` on GitHub (Add file → Upload files).

## Open before launch

- ROC license number (page shows a placeholder)
- Update the business name in the plan documents and on the business filing
- Booking and deposit payment provider

## Going live (one-time setup, about 30 minutes)

1. **Netlify (free hosting + form inbox).** Sign up at netlify.com with GitHub → Add new site → Import from GitHub → pick `just-call-the-disposal-guy` → Deploy. Netlify reads `netlify.toml` and publishes `site/`.
2. **Turn on form email alerts.** In Netlify: Site configuration → Forms → enable form detection, then Form notifications → Email → your address. Every booking, with its photos, lands there.
3. **Deposit links.** In Square or Stripe, create a $100 payment link for each option. Paste them into the four-line `CONFIG` block at the bottom of `site/index.html`, along with your phone and ROC number. Until the links are added, customers land on a thank-you page that says you'll text the deposit link.
4. **Domain.** Buy the domain, then in Netlify: Domain management → Add a domain. Netlify adds free HTTPS.
5. **Test it.** Submit one fake booking with photos, check the email, then delete it in Netlify → Forms.
