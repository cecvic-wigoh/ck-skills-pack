---
name: ck-social-content-calendar
description: >-
  Use when building a monthly Facebook or Instagram content calendar for a
  Comfort Keepers office: weekly themes, captions, CTAs, and static, carousel,
  and reel creatives with on-creative copy in plain, warm language for readers
  aged 60 to 80. Also use when the user asks for CK social posts, service
  explainers, holiday social content, sample creatives, or a reusable posting
  plan for a Comfort Keepers franchise.
license: MIT
metadata:
  author: AiMT / Wigoh
  version: "1.0"
---

# CK Social Content Calendar

Builds one month of Facebook and Instagram posts for one Comfort Keepers office. Every post gets a format (static, carousel or reel), the words that go ON the creative, the caption, and one CTA. Language is simple, warm and direct, written to the reader as "you", and explains each service so the reader thinks "this is exactly what I need." Draft only: never post, schedule or spend.

## When to use

- The user asks for a content calendar, social posts, captions, or creatives for a Comfort Keepers office and a given month.
- The user wants statics, carousels or reels with on-creative copy in senior-friendly language.
- The user wants a reusable posting plan that can be handed to a designer or social manager.

## Inputs (ask only for what's missing)

- Office (city + state) and month.
- Primary reader: the senior (default, ages 60 to 80) or the adult child / family caregiver.
- Posts per week (default 3: Tue, Thu, Sat).

## References (read both in full first)

- [references/ck-copy-guide.md](references/ck-copy-guide.md): the Comfort Keepers copywriting guide (brand promise, Interactive Caregiving, audiences, tone, avoid list incl. no em dashes, content types, CTAs, final checks, per-post workflow). It is the house rulebook; follow it over generic advice.
- [references/formats-and-creative.md](references/formats-and-creative.md): format definitions, on-creative copy rules, layout specs, voice rules for 60 to 80 year olds, say-this-not-this list, and the post template.

If the optional Boring Marketing skills `bm-social-content`, `bm-creative` and `bm-brand-voice` are installed, load and follow them. If `bm-audience-research` is installed and there are no brand files, do a light pass on public reviews. If those skills are not installed, skip them and work from this skill plus the office's public site and reviews.

## Output location

Use a lowercase kebab-case office slug, such as `ck-lexington-ky`. Save all deliverables under `./<office-slug>/` in the current project (create the folder if needed):

- `./<office-slug>/brand/` — reused or newly built brand files
- `./<office-slug>/creative/` — sample creatives
- `./<office-slug>/<month-year>-content-calendar.md` — the full calendar (required)
- `./<office-slug>/<month-year>-content-calendar.html` — optional self-contained HTML page of the same calendar
- `./<office-slug>/posts.json` — structured post data

If the user already has brand or office files in another folder, reuse that path instead of inventing a parallel one.

## Steps

1. **Confirm the office.** Find it on the Comfort Keepers office locator (`https://www.comfortkeepers.com/offices/<state>/<city>/`). Take address, phone and services only from that page. Watch for same-name towns in other states. Note any errors on the office page (wrong owner story, other towns) for the confirm list.
2. **Brand files.** Reuse `./<office-slug>/brand/` if it exists; otherwise build a lean set (voice, audience, verified services, creative kit). Free sources only unless the user approves spend.
3. **Plan the month.** One big idea for the month; a theme per week tied to real moments of that month (holidays, weather and safety, family visits, local events checked with dates). Write a launch arc from "what care is" to "how to start" to an invitation to call.
4. **Assign formats.** Mix roughly 40% statics, 30% carousels, 30% reels. Steps and lists become carousels; emotional moments become reels; one clear message becomes a static.
5. **Write each post** using the post template in [references/formats-and-creative.md](references/formats-and-creative.md): date, audience, theme, format, visual idea, on-creative copy, caption, CTA with the phone number written out, hashtags, franchise line ("Each office is independently owned and operated." or the office's required wording).
6. **Sample creatives.** Make 3 samples (one static, first 2 to 3 slides of a carousel, one reel cover). Generate the photo, set the text in HTML over it so wording matches exactly, check faces aren't covered and the phone number is letter-perfect. Save the images and any overlay HTML under `./<office-slug>/creative/`. Label them AI stand-ins to replace with real, consented office photos.
7. **Confirm-with-office list.** Every unverified claim, service, hours, offer, event detail, photo consent, testimonial permission, logo/colors, VA wording, and website errors found.
8. **Deliver.** Write the markdown calendar (required) and, when useful, a self-contained HTML page. Include strategy, voice rules, word list, formats, a calendar view, all posts with on-creative copy, samples and the confirm list. Also save `posts.json`. In the chat reply: the file paths, one line per weekly theme, the format mix, and the top confirm items.

## Hard rules

- Never invent stats, testimonials, client stories, quotes, prices, insurance or Medicare claims, or services not listed for that office.
- Non-medical care: caregivers remind about medicine, they don't give it.
- No fear, guilt or fake urgency. Never infantilize seniors.
- Brand-level awards or rankings are not office claims.
- Draft only; nothing gets posted, boosted or sent without an explicit yes.
