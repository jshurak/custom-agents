# IDEA SCOUT — Agent Definition

## Mission

You find evidenced, shippable business ideas for one specific operator. You do
not brainstorm. You mine real demand signals, kill almost everything you find,
and deliver a small number of ideas that survived a deliberate attempt to
destroy them.

Your output is judged on kill rate and evidence quality, not idea count. A
digest of three ideas with verbatim sourced complaints beats twenty clever
concepts. If a run produces nothing that clears the gates, say so and report
what you searched. An empty digest is a valid and respectable result.

## Operator profile (fixed constraints — never relax these)

- **Build capability:** no-code / low-code only. Airtable, Make, Zapier, n8n,
  Softr, Glide, Bubble, Lovable, Notion, Framer, Webflow, Carrd, Stripe
  Payment Links, Gumroad, Tally, Retool. Nothing requiring custom backends,
  infrastructure management, or a codebase to maintain.
- **Audience:** zero. No list, no following, no community standing. Every idea
  must borrow an existing audience.
- **Time budget:** 14 days solo, part-time, from zero to live and public.
- **Monetization:** mixed. Two tracks (see Output).
- **Capital:** minimal. Assume no paid acquisition budget.

## Core strategy

The free viral tool is not the business — it is how the operator manufactures
the audience they do not have. Hunt in pairs where possible: a free shareable
tool and a paid offer in the same niche that the tool's traffic feeds.

Assume ten to fifteen shots will be needed. Optimize for cheap experiments and
fast kills, not for one perfect idea.

## Pipeline (execute in order every run)

1. **Mine.** Pull raw, verbatim complaints and requests from Tier 1–3 sources
   below. Collect the exact sentence and its URL. Never paraphrase at this
   stage.
2. **Cluster.** Group complaints by underlying problem. A problem stated
   independently by three or more people in different threads is a signal; one
   loud person is not.
3. **Check timing.** Flag anything newly possible in the last 90 days — new
   API, platform policy change, new public dataset, price drop, marketplace
   category launch. Timing edge is a scoring bonus, not a gate.
4. **Check prior art.** Assume it already exists; prove otherwise. Search
   Product Hunt, the relevant marketplace, Chrome Web Store, app stores, plain
   web search. Output is either KILL or a stated differentiated wedge.
5. **Gate.** Apply all hard gates. Most candidates die here. This is correct.
6. **Red-team.** Switch roles. For each survivor, write the strongest case for
   why it fails. Attack distribution and cost-at-scale first — those kill more
   indie launches than product quality does. Ideas that don't survive their own
   critique are dropped, not softened.
7. **Score and package.** Only survivors get scored and written up.

## Hard gates (all must pass — no partial credit, no averaging)

- **G1 — Named stack.** You can specify the exact no-code tools and how they
  connect. "Build it with AI" is not a stack. Failure to name it means you
  haven't proven shippability.
- **G2 — Survives its own success.** Compute running cost at 100,000 visits in
  24 hours. Per-call model or API costs with no rate limit or caching layer is
  a kill unless you specify the mitigation. A viral hit that produces a bill or
  a 502 is a loss, not a win.
- **G3 — Borrowed audience.** Names a specific existing traffic pool: the
  actual subreddit, the actual marketplace category, the actual search query,
  the actual Discord. "Post it on social" is a fail.
- **G4 — 20-second demo.** Value is legible in one screenshot or a short
  vertical video. If it needs explaining, it cannot be distributed cold.
- **G5 — Residual asset.** If it flops, something remains: captured emails,
  indexed SEO pages, or a relationship in a community.
- **G6 — Evidence attached.** At least three verbatim quotes with live URLs
  from at least two different sources.
- **G7 — 14-day build.** Honest estimate in days, assuming part-time solo work
  and no prior familiarity with the specific tools.

Automatic kills regardless of appeal: two-sided marketplaces, cold-start data
dependencies, hardware, regulated categories (health claims, financial advice,
legal advice), anything needing a sales call, anything requiring content
moderation at launch.

## Scoring (survivors only)

Score each 1–5. **Report every dimension separately. Never collapse into a
single composite score** — an average lets a fatally weak dimension hide.

- Evidence strength — count, recency, and emotional intensity of complaints
- Demand proof — is anyone already paying for a worse version?
- Share loop strength (Track B) — is the output artifact worth posting?
- Build speed — days to public
- Channel quality — how accessible is the borrowed audience to an unknown?
- Timing edge — is this newly possible?

## Source priority

**Tier 1 — Revealed paid demand.** Upwork and Fiverr repeat gigs (someone
paying a human weekly for a task is the strongest automation signal there is).
Notion template gallery, Gumroad, Etsy digital, Figma Community, Framer and
Webflow marketplaces, Zapier and Make template directories, Shopify app store,
Chrome Web Store, Airtable Universe. Read each three ways: what ranks, what
sells despite bad reviews, and which category is conspicuously thin. These are
dual-purpose — demand signal and distribution channel in one.

**Tier 2 — Algorithmic reach.** TikTok Creative Center trending searches and
hashtags. Long-tail search gaps via autocomplete and People Also Ask. These
matter disproportionately because neither channel cares that the operator is
unknown.

**Tier 3 — Stated pain.** Reddit niche subs, Hacker News (Ask HN threads and
Show HN comments — the comments beat the launches), Stack Exchange, G2 and
Capterra 2–3 star reviews of expensive SaaS, app store reviews. Filter hard by
"solvable with a thin no-code tool."

**Tier 4 — Prior art and timing.** Product Hunt comments, Indie Hackers,
Acquire.com and Flippa listings, API and platform changelogs.

Prefer sources with clean programmatic access. Do not scrape ToS-hostile sites.
When a source is inaccessible, say so in the run notes rather than substituting
guesses.

## Absolute rule on evidence

Never invent a quote, a URL, a username, a metric, or a revenue figure. If you
cannot retrieve a real complaint, the idea does not exist. A fabricated signal
is worse than no output, because the operator will spend two weeks building on
it. When uncertain whether a source is real, drop it.

## Output

Every digest: **five ideas, three Track A and two Track B.**

- **Track A — revenue now:** templates, productized automations, niche
  directories, thin paid micro-tools. Money in weeks, no virality required.
- **Track B — audience engine:** free tool with a shareable result artifact and
  an email gate on the output.

Each idea, in this exact structure:

TITLE
Track: A or B
One-line pitch:
The problem (verbatim quotes, 3+, each with URL and source):
Who has it (specific, not a demographic):
Named stack (exact tools and connections):
Build estimate (days):
Distribution placement (the exact subreddit / category / query / community):
First post or listing (write the actual copy):
Share artifact (Track B — what exactly does the user post?):
Monetization path and price point:
Cost at 100k visits / 24h (show the arithmetic):
Prior art found and the wedge:
Strongest case it fails (from red-team):
Residual asset if it flops:
Scores (six dimensions, listed separately):


Close each digest with **Run notes**: sources searched, candidates generated,
candidates killed and the gate that killed them, and anything newly possible
you noticed but couldn't yet turn into an idea.

## Memory

Persist every idea generated, every kill with its reason, and every operator
rejection with its stated reason. At the start of each run, load this history.
Never resurface a killed idea unless a specific new signal has changed the
condition that killed it — and say explicitly what changed.

Track which sources have produced survivors and shift mining effort toward
them over time.

## Anti-slop

These archetypes are banned unless a specific fresh Tier 1 or Tier 2 signal
forces them: AI-powered [X] for [Y], habit trackers, meal planners, resume
builders, generic productivity dashboards, "Uber for X," another chat wrapper,
anything whose entire concept is a system prompt.

If an idea could have been produced without doing any research, it is slop.
Delete it and go back to mining.
hermes@hermes:~/.hermes/profiles/idea-scout$ vi AGENTS.md
hermes@hermes:~/.hermes/profiles/idea-scout$ rm ./AGENTS.md
hermes@hermes:~/.hermes/profiles/idea-scout$ vi AGENTS.md
hermes@hermes:~/.hermes/profiles/idea-scout$ cat workspace/digest-2026-08-12.md
# IDEA SCOUT DIGEST — 2026-08-12

Five ideas: three Track A, two Track B. All quotes verbatim from retrieved sources; URLs live. Spec-compliant structure per AGENTS.md "Output" section.

---

# 1. SLEEP & STORY READY-PACKS

**Track:** A

**One-line pitch:** Downloadable packs that solve the two loudest MYO-card complaints — sleep sounds with no audible loop point, and public-domain audiobooks already converted, split to Yoto's limits, with icons and printable card labels included.

**The problem (verbatim quotes, 3+, each with URL and source):**
- "I absolutely love these players, but my biggest request is they fix the looping on the sleep sounds! … when the track loops it cuts out for a split second while it restarts" — r/YotoPlayer, thread "sleep_sounds_looping", archived 2023-01-04. URL: https://www.reddit.com/r/YotoPlayer/comments/103epv6/sleep_sounds_looping/
- "Yes! I've thought the same, we use the train track sounds when we're away from home, and it wakes us up sometimes." — same thread, same URL.
- "Glad it's not just me! I can't even find a track and put it on a MYO card" — same thread, same URL.
- "How often does it loop? This is what's stopped me buying the card." — same thread, same URL.
- "Hi, I wanted to put Percy Jackson onto yoto, but the US yoto store doesn't sell the Percy Jackson books. I bought the audiobook through apple, and it's about 450mb in m4a format, and 16 hours long. The max for a make your own card is 100mb and 10 hours, I think." — r/YotoPlayer, thread "how_can_i_convert_a_large_apple_audiobook_m4a_so", archived 2023-01-13. URL: https://www.reddit.com/r/YotoPlayer/comments/10a5ks2/how_can_i_convert_a_large_apple_audiobook_m4a_so/
- "I tried to convert apple audiobook and could never find away I tried several software that claimed to convert but they didn't do it's locked to apple" — same thread, same URL.
- "creating a new playlist fails with no work-around; uploads miss many recordings, online guidance is useless" — Yoto app, Apple App Store review "Disappointed but trying", 3★, 2026-06-08. URL: https://apps.apple.com/us/app/id1412039719
- "We make our own cards and update them with new books and music whenever we want. You can add a custom icon that displays for each track." — Hacker News comment, 2024-12-06. URL: https://news.ycombinator.com/item?id=42340864

**Who has it (specific, not a demographic):** Yoto households that already make MYO cards but hit three walls: the loop-click on sleep audio, file conversion/size limits, and finding content worth putting on a card. The Yoto app has ~27k App Store ratings; every buyer already owns the hardware — zero education needed.

**Named stack (exact tools and connections):** Audacity (free, no code — generate 60-min seamless brown/pink noise and rain loops; split/trim audiobook MP3s to ≤100MB and ≤10h per Yoto limits) → LibriVox (public-domain audiobook MP3s: Winnie-the-Pooh, Beatrix Potter, Just So Stories, fairy tales) → Canva (card label sheets + track icons) → Gumroad (payment + file delivery + CDN). Marketing asset: 60-second vertical demo (CapCut) showing "download → drag → card works."

**Build estimate (days):** 9, part-time solo. 3 days: record/render seamless sleep loops and verify no click at the loop point. 4 days: download, trim, split 3 audiobooks into kid-friendly chapter tracks. 2 days: Canva labels/icons + Gumroad page.

**Distribution placement (the exact subreddit / category / query / community):** Gumroad discover search "yoto" (8 products total in the entire catalog — a new listing is instantly top-3); Etsy search "yoto card"; r/YotoPlayer; Yoto Families Facebook groups (ask-mod-first); the email list built by Idea #4 (YotoShare) in this same digest.

**First post or listing (write the actual copy):** "Yoto Sleep Pack — 8 seamless sleep sounds (brown noise, rain, ocean, train, womb hum) recorded so there's no click at the loop point. Drag onto any MYO card and it's done. $14, includes the card labels."

**Share artifact (Track B — what exactly does the user post?):** n/a — Track A. The 60-second demo video doubles as the shareable.

**Monetization path and price point:** Sleep Pack $14; Story Packs (one audiobook, kid-ready) $12; "Bedtime Bundle" $29. Gumroad fees ~10% + $0.50 — margins >85%.

**Cost at 100k visits / 24h (show the arithmetic):** Files are delivered by Gumroad's CDN — $0 infrastructure at any volume. 100,000 visits × 2% conversion = 2,000 sales × $14 avg = $28,000 revenue; fees = $0.50 × 2,000 + 10% × 28,000 ≈ $3,800. No server, no per-call model cost. Survives its own success.

**Prior art found and the wedge:** Tiny Print Studio sells free-to-use "Yoto Icon Maker" and "Yoto Sticker Maker" on Gumroad (5.0★, 3 and 2 reviews — product pages retrieved 2026-08-12). This proves the niche pays, but they monetize the *look* of cards, not the *audio*. Nobody sells pre-formatted seamless sleep loops or conversion-done audiobook packs. Wedge: the three verbatim walls (loop click, conversion, content) solved in one download.

**Strongest case it fails (from red-team):** Sleep loops are commoditized (free on YouTube); Tiny Print Studio, with "Top creator" status and existing audience, can extend into audio packs in a week; parents are price-sensitive ($12 ≈ one Yoto card); public-domain catalog is limited and the biggest demand (Percy Jackson) is copyrighted and unsellable. Defense: "no loop click" is a real, testable differentiator; bundle labels/icons so the incumbent's strength (looks) is bundled-in; ship in 9 days before they notice; the directory (Idea #4) provides launch traffic.

**Residual asset if it flops:** Gumroad store with reviews + the email list from YotoShare; every sale is a documented paid-demand datapoint for the next pack.

**Scores (six dimensions, listed separately):**
- Evidence strength: 5
- Demand proof: 4
- Share loop strength: n/a (Track A)
- Build speed: 3
- Channel quality: 4
- Timing edge: 4

---

# 2. HOST BRIEF

**Track:** A

**One-line pitch:** A one-time $29 Notion/Airtable operations kit for 1–3 unit Airbnb hosts — pre-written guest message sequences, turnover checklists, booking tracker, review cadence — aimed at hosts who refuse to pay $60/mo for buggy PMS software.

**The problem (verbatim quotes, 3+, each with URL and source):**
- "Just started charging $60/mo for this garbage." — Hospitable.com app, Apple App Store review "Bait and switch garbage", 1★, 2026-06-06. URL: https://apps.apple.com/us/app/id1475679185
- "Believe all the negative reviews you see here. The customer service for this app is nonexistent. If you submit a ticket, even as a paying user, expect to not hear back for about a week" — Hospitable.com app, review "Very disappointed", 1★, 2026-08-04. URL: https://apps.apple.com/us/app/id1475679185
- "Just use the Airbnb app to communicate on your phone. Messages take ages to get onto the platform. When you type something the whole app will crash" — Hospitable.com app, review "Crashes constantly. Slow. Wastes time.", 1★, 2026-04-16. URL: https://apps.apple.com/us/app/id1475679185
- "Automated messaging is great. Most of the other features are not. I keep having to contact over missing reservations." — Guesty For Hosts app, Apple App Store review "Scammy Damage protection charges", 1★, 2024-06-30. URL: https://apps.apple.com/us/app/id1032870693
- "I got this App to manage my STR over several platforms. Unfortunately had to switch to manually blocking the dates everytime I got a booking (rendering this app useless) as I was getting constantly double booked." — Guesty For Hosts app, review "Canceling Subscription - Constant Double Bookings", 2★, 2023-11-09. URL: https://apps.apple.com/us/app/id1032870693

**Who has it (specific, not a demographic):** Part-time hosts with 1–3 listings who run everything on Airbnb's free tools and read PMS pricing ($20–60/mo/unit) as absurd. The angry Hospitable/Guesty reviewers are the adjacent evidence; the target is the host one step below them who never subscribed.

**Named stack (exact tools and connections):** Notion (template: booking pipeline board, per-guest folder holding the message sequence, turnover checklist with photo-log prompts, review reminders) → Canva (printable house manual + QR signs) → Gumroad (payment + delivery). Message sequences are copy-paste into Airbnb's own free scheduled-messages feature — no integrations, no API, no automation dependency. Airtable + Softr variant for hosts who refuse Notion.

**Build estimate (days):** 6, part-time solo. 2 days: write message sequences (6 touchpoints × 3 tones). 2 days: Notion/Airtable build. 1 day: Canva house manual. 1 day: Gumroad page + demo video.

**Distribution placement (the exact subreddit / category / query / community):** r/airbnb_hosts (host-tool posts are normal there); Airbnb host Facebook groups (active link-sharing culture); Gumroad discover search "airbnb host" (755 products but the top results are PLR welcome-book spam — a messaging-first kit is visually distinct); Etsy search "airbnb host template".

**First post or listing (write the actual copy):** "You don't need a $60/mo PMS for 2 listings. I packaged everything I automate as a host — the 6-message guest sequence (booking→checkout), turnover checklist, booking tracker, review reminders — into one $29 kit that works with Airbnb's free tools."

**Share artifact (Track B — what exactly does the user post?):** n/a — Track A. The demo video ("paste message → guest answers the same 3 questions") is the shareable.

**Monetization path and price point:** $29 one-time on Gumroad; upsell $19 "Digital House Manual" Canva pack. Later, only if the base sells: $49/year Airtable+Make variant that auto-sends review reminders (Make recipe included).

**Cost at 100k visits / 24h (show the arithmetic):** Gumroad-delivered files, $0 marginal. 100,000 visits × 0.3% conversion = 300 sales × $29 = $8,700; fees ≈ $0.50 × 300 + 10% × 8,700 ≈ $1,020. No infrastructure. Survives.

**Prior art found and the wedge:** Gumroad's airbnb category holds 755 products — dominated by welcome-book templates and PLR/MRR spam (e.g., "Short Term Rental Welcome Book | PLR MRR", retrieved 2026-08-12). One "Airbnb Manager - Multiple Properties" Notion product exists (page wouldn't load for inspection — noted honestly). Wedge: messaging-first (the one feature the angry reviews say *works* and matters), built to run on Airbnb's free scheduled messages, priced one-time vs $60/mo.

**Strongest case it fails (from red-team):** Hosts don't search for "ops kit" — they search "welcome book"; the PLR flood proves the category gets spam-clicked rather than bought; 1–3 unit hosts may be fine with Airbnb defaults; the angry PMS reviewers are multi-property pros who need real software, not templates. Defense: lead with the price pain in the title ("$60/mo" appears in the listing copy); seed via host FB groups with a free sample sequence; be the quality answer to a spam category.

**Residual asset if it flops:** Gumroad store + host email list (adjacent buyers: cleaners, co-hosts) + house-manual templates resellable separately.

**Scores (six dimensions, listed separately):**
- Evidence strength: 4
- Demand proof: 3
- Share loop strength: n/a (Track A)
- Build speed: 4
- Channel quality: 3
- Timing edge: 4

---

# 3. THE DAY-OF PACK

**Track:** A

**One-line pitch:** Canva-template wedding printables for the two moments couples search by exact phrase — "wedding day timeline for 4pm ceremony" and seating-chart sheets — sold cheap on Etsy/Gumroad and fed by the free Table Talk tool's email list (Idea #5, this digest).

**The problem (verbatim quotes, 3+, each with URL and source):**
- Google autocomplete, retrieved 2026-08-12 (firefox suggest): "wedding day timeline for 4pm ceremony", "wedding day timeline for 5pm ceremony", "wedding day timeline for 3pm ceremony", "wedding day timeline 2pm ceremony" — four ceremony-time variants of the same intent. Source: suggestqueries.google.com (live queries).
- Google autocomplete, retrieved 2026-08-12: "canva template for wedding seating chart", "seating chart maker", "seating chart template". Source: suggestqueries.google.com (live queries).
- "All their 'help' is about registry and vendors, their focus is not helping you keep track of guests or preparing invitations." — Zola Wedding Planner app, Apple App Store review "Find Another Planner - do not go here!", 1★, 2026-07-05. URL: https://apps.apple.com/us/app/id852691916
- "Pay to add use the seating chart feature? Are you kidding? Just use a pen and paper, don't waste your time or money." — Zola Wedding Planner app, review "Premium just to use seating chart?", 1★, 2026-08-03. URL: https://apps.apple.com/us/app/id852691916
- Marketplace supply gap: Gumroad discover search "wedding seating chart" returns only 28 products total (retrieved 2026-08-12) — seating-chart-specific results are a handful of generic templates, and none answer the ceremony-time timeline queries.

**Who has it (specific, not a demographic):** DIY couples (wedding under ~$15k — the segment generating Zola's review-wall anger) who want print-ready, editable templates instead of learning Canva from zero in the final 4–6 weeks.

**Named stack (exact tools and connections):** Canva (design 6 seating-chart layouts × sizes, 4 day-of timelines — one per ceremony time, escort cards) → Etsy (digital download listings) + Gumroad (second channel, lower fees) → Tally (free 4pm-timeline PDF as email-gated lead magnet). No code, no server, no integrations.

**Build estimate (days):** 4, part-time solo. 2 days: seating charts + escort cards. 1.5 days: timeline PDFs for 2pm/3pm/4pm/5pm ceremonies with vendor handoff times. 0.5 days: listings + lead magnet.

**Distribution placement (the exact subreddit / category / query / community):** Etsy search "seating chart template" and "day of timeline" (both live queries); Gumroad discover search "wedding"; the Table Talk email list (Idea #5); wedding-planning Facebook groups via the free 4pm-timeline PDF.

**First post or listing (write the actual copy):** "Day-Of Timeline Templates for every ceremony time — 2pm, 3pm, 4pm, 5pm — editable in Canva, print-ready, with photographer/hair/makeup/catering handoff times already mapped. $12 or all four for $19."

**Share artifact (Track B — what exactly does the user post?):** n/a — Track A. The free 4pm timeline PDF is the lead magnet.

**Monetization path and price point:** $12–19 per set, $29 full bundle. Etsy fees ~10–15%. Pure digital margin.

**Cost at 100k visits / 24h (show the arithmetic):** Etsy/Gumroad host and deliver everything — $0 marginal at any volume. 100,000 visits × 0.5% conversion = 500 sales × $15 avg = $7,500; Etsy fees ≈ 10–15% ≈ $750–1,100. No infrastructure. Survives trivially.

**Prior art found and the wedge:** Generic Canva seating-chart templates exist on Etsy/Gumroad (one-size, no ceremony-time variants); Zola paywalls the interactive version and its reviews are the rage funnel. The ceremony-time-specific day-of timeline is conspicuously absent from top results. Wedge: answering the exact autocomplete query verbatim, plus borrowed traffic from Table Talk's email list — never launched cold.

**Strongest case it fails (from red-team):** Etsy printables is one of the most competitive categories on the internet; Canva templates are trivially copyable within days; without Table Talk's traffic this is a cold Etsy start among thousands of near-identical listings; wedding buyers churn after one purchase. Defense: it exists as the monetization arm of Table Talk (paired per core strategy); the ceremony-time angle gives searchable specificity; residual value in the designs themselves.

**Residual asset if it flops:** Etsy store with reviews + the email list from Table Talk + the designs themselves (resellable to other event niches, e.g., corporate offsites).

**Scores (six dimensions, listed separately):**
- Evidence strength: 2
- Demand proof: 3
- Share loop strength: n/a (Track A)
- Build speed: 5
- Channel quality: 3
- Timing edge: 3

---

# 4. YOTOSHARE

**Track:** B

**One-line pitch:** A searchable directory of parent-shared Yoto "Make Your Own" card playlists, seeded with the share links already floating around r/YotoPlayer — the structured pin-thread parents keep asking each other to start.

**The problem (verbatim quotes, 3+, each with URL and source):**
- "I'm not too familiar with Reddit subs, but is there a way to start a pinned thread of people's links and a description of that the card is?" — r/YotoPlayer, thread "anyone_here_interested_in_sharing_their_myo_mp3", archived 2023-03-21. URL: https://www.reddit.com/r/YotoPlayer/comments/11xsatj/anyone_here_interested_in_sharing_their_myo_mp3/
- "I made a lot of MYO content and have a library of mp3s. I've got mostly toddler stuff like cocomelon, sesame st, dr suess and disney Looking to potentially swap some mp3s with others who'd like to share" — same thread, same URL.
- "I have loads of content and would be interested in more. What's the best way to share?" — same thread, same URL.
- "How do we share them? I would be interested!" — same thread, same URL.
- "It's virtually impossible to get the cards downloaded for offline play. And it's super hard to share cards with your friends." — Yoto app, Apple App Store review "So frustrating", 1★, 2026-07-17. URL: https://apps.apple.com/us/app/id1412039719
- Google autocomplete, retrieved 2026-08-12: "yoto content library share", "yoto content free", "yoto card ideas". Source: suggestqueries.google.com (live queries).

**Who has it (specific, not a demographic):** Yoto households (kids 0–10) that already make MYO cards and share yoto.io links by hand. The app has ~27k App Store ratings; HN parents evangelize the device unprompted ("Yoto players pretty neatly reproduce the old experience of putting something physical into a player…", https://news.ycombinator.com/item?id=48400588).

**Named stack (exact tools and connections):** Softr (public directory: list page + detail pages) ← Airtable (playlist records: title, age range, runtime, source, yoto.io link, submitter email) ← Tally ("submit your playlist" form, 60 seconds, webhook) → Make (append to Airtable, dedupe, manual-review flag before publish). Email capture via Buttondown. No server code anywhere.

**Build estimate (days):** 4, part-time solo. Day 1: Airtable schema + Softr list/detail pages. Day 2: Tally form + Make webhook. Day 3: seed 30 playlists from archived/community links. Day 4: launch post + submission guidelines.

**Distribution placement (the exact subreddit / category / query / community):** r/YotoPlayer ("yoto card ideas reddit" is a live autocomplete query); Yoto Families Facebook groups (raw yoto.io links are already posted there); Google long-tail "yoto card ideas" / "yoto content free" (competition is thin blog posts, not tools); TikTok #yoto (strong per HN's recurring Yoto threads — TikTok Creative Center was inaccessible this run; noted in run notes).

**First post or listing (write the actual copy):** "My kids' Yoto player has 9 blank cards and I never know what to put on them, so I made a searchable directory of community-shared MYO playlists — sorted by age, runtime, and what's actually on the card. It's free, no signup, and if you have a card you're proud of you can add it in 60 seconds: [link]."

**Share artifact (Track B — what exactly does the user post?):** Each playlist detail page — title + "what's on this card" + age range + runtime + the share link. Parents already paste raw yoto.io links into Facebook groups; the directory page is the cleaner version of that exact post, with a "shared from YotoShare" footer.

**Monetization path and price point:** Free tool, no ads. Email capture on every submission plus "get 5 new card ideas weekly" opt-in. The list feeds Idea #1 (Sleep & Story Ready-Packs) in this digest. Yoto referral program later ("10 referral code for uk" thread shows it exists).

**Cost at 100k visits / 24h (show the arithmetic):** 100,000 page loads × $0/load (Softr serves static pages; zero API calls per view) + Airtable row writes only on submissions (~100/day worst case, free tier 1,200 rows is ample) + Tally free tier = $0. Worst case, Softr Business at a flat $59/mo if the free tier caps traffic — still $0 marginal per visit. No per-call model costs. Survives its own success.

**Prior art found and the wedge:** No Yoto playlist directory exists. Gumroad's entire "yoto" catalog is 8 products (retrieved 2026-08-12); HN Algolia search "yoto share playlist" returns nothing relevant; App Store has no such app (only Cardaroo, a paid emulator, and "Stories for Toniebox and Yoto" audio packs). Wedge: it is the community pin-thread parents keep requesting, with structured metadata (age/runtime) Reddit threads cannot provide.

**Strongest case it fails (from red-team):** Cold-start — a directory seeded with 30 playlists can feel empty and die; Yoto could ship official sharing and kill the niche; r/YotoPlayer self-promo rules may cap distribution; new-account Reddit posts get filtered as spam. Defense: seed 30+ real links before launch; lead with Facebook groups where link-sharing is the norm; SEO long-tail compounds independently of any community's rules.

**Residual asset if it flops:** Indexed pages for "yoto card ideas" variants + an email list of exactly the buyers for Idea #1.

**Scores (six dimensions, listed separately):**
- Evidence strength: 4
- Demand proof: 3
- Share loop strength: 5
- Build speed: 5
- Channel quality: 4
- Timing edge: 4

---

# 5. TABLE TALK

**Track:** B

**One-line pitch:** A free, no-account wedding seating chart tool — paste your guest list, drag people to tables, mark "keep apart" pairs, export a printable chart and escort-card sheet — launched into the middle of Zola's paywalled-seating-chart backlash.

**The problem (verbatim quotes, 3+, each with URL and source):**
- "Pay to add use the seating chart feature? Are you kidding? Just use a pen and paper, don't waste your time or money." — Zola Wedding Planner app, Apple App Store review "Premium just to use seating chart?", 1★, 2026-08-03. URL: https://apps.apple.com/us/app/id852691916
- "Seating chart is a scam … It let me add all the tables I wanted and arranged them. Then, once I started adding guests, I got the option to 'upgrade to premium to seat mo[re]'" — Zola Wedding Planner app, review "Seating chart is a scam", 1★, 2026-06-28. URL: https://apps.apple.com/us/app/id852691916
- "'You have enough quotes and bills to handle for your wedding, so we made Zola entirely FREE. For real.' -Zola Claiming the app is entirely free and then charging to make a seating chart is wild" — Zola Wedding Planner app, review "Not Entirely FREE. For Real.", 1★, 2026-06-23. URL: https://apps.apple.com/us/app/id852691916
- "I built a tiny tool to help decide the seating chart for my small wedding. It was a cute GUI on top of a simple constraint solver. It wasn't perfect, but it helped me feel confident in the final result." — Hacker News, Ask HN "What are tools you have made for yourself", 2026-06-08. URL: https://news.ycombinator.com/item?id=48453838
- Google autocomplete, retrieved 2026-08-12: "seating chart maker", "canva template for wedding seating chart", "seating chart template". Source: suggestqueries.google.com (live queries).

**Who has it (specific, not a demographic):** Engaged couples 2–4 weeks out (that's when seating charts get built) who are rage-quitting Zola right now. They don't want an account or a premium tier — they want a printable.

**Named stack (exact tools and connections):** Lovable (generates the app from prompts — client-side React, no backend) → Netlify free tier (hosting) → Tally (email gate on the printable export). All seating logic runs in the browser (guest names, tables, constraints in localStorage) — no server, no per-call cost. Canva-template upsell link (Idea #3) on the export screen.

**Build estimate (days):** 8, part-time solo. 2 days: Lovable scaffold + drag-drop table layout. 2 days: constraint flags (keep-apart/sit-together) + localStorage. 2 days: printable export + escort-card sheet. 2 days: landing page, Tally gate, demo video.

**Distribution placement (the exact subreddit / category / query / community):** r/weddingplanning and r/weddingsunder10k (value posts are within their rules); TikTok #weddingtok ("Zola made their seating chart $30 — this is free"); Google search "seating chart maker" (Zola's own unhappy reviewers are the ranking context you're outranking); wedding-planning Facebook groups.

**First post or listing (write the actual copy):** "Zola just put their seating chart behind a paywall, so I built a free one. No account, no app — paste your guests, drag them to tables, mark who can't sit together, and print. Made it for my own wedding in October: [link]."

**Share artifact (Track B — what exactly does the user post?):** The finished printable seating-chart PDF. Couples post their table plans in planning groups constantly; the export carries a small "made with Table Talk" footer.

**Monetization path and price point:** Free tool; Tally email gate on the printable export. The list feeds Idea #3 (The Day-Of Pack). Optional later: $9 "pro export" (per-table cards + menu place cards) via Stripe Payment Link — only after the free tier proves traffic.

**Cost at 100k visits / 24h (show the arithmetic):** Netlify free tier = 100 GB bandwidth/month. Page ≈ 250 KB × 100,000 visits = 25 GB → $0. Zero compute (all client-side). Tally free tier (100 submissions/mo) → flat $29/mo Pro if exceeded. Total worst case ≈ $29 flat, not per-visit. Survives its own success.

**Prior art found and the wedge:** Better Seater (HN, 132 pts, 2024) — free but built by an engineer for engineers: constraint-solver UI, no printables, no wedding-community distribution. Zola's paywalled tool (the literal source of the anger). Canva templates (manual, no constraint help). Two 2025 App Store entrants rated 1–2★. Wedge: free + no account + constraints + printable, distributed into the exact communities where Zola's backlash lives.

**Strongest case it fails (from red-team):** Zola un-paywalls after the backlash and the wedge evaporates; Lovable apps get cloned in days by copycats; wedding tools have a one-shot lifecycle (every user churns after the wedding). Defense: ship before Zola reacts; own the printable + the email list; the list converts into the evergreen printables store (Idea #3) regardless of the tool's lifecycle.

**Residual asset if it flops:** The email list of couples (direct buyers for Idea #3) + indexed pages for seating-chart queries.

**Scores (six dimensions, listed separately):**
- Evidence strength: 4
- Demand proof: 4
- Share loop strength: 4
- Build speed: 4
- Channel quality: 4
- Timing edge: 5

---

# RUN NOTES

**Sources searched this run.** HN Algolia API (dozens of full-text comment/story/Show-HN searches), Google autocomplete (three seed batches: general niches, Yoto, wedding/small-biz), Stack Exchange API (softwarerecs — dev-skewed, low yield), Apple iTunes Search + App Store review RSS (~1,300 recent reviews pulled across Yoto, Zola, The Knot, Hospitable, Guesty, eRank/Etsy Seller, TPT, BambooHR, Gusto, Rippling, SportsEngine, TeamSnap, TurboTenant, Zillow Rental Manager, HoneyBook, Pixieset), Wayback CDX + archived pages (r/YotoPlayer 689 threads, r/EtsySellers 387, r/airbnb_hosts 419, r/Landlord 324, r/Screenwriting 57, r/Teachers ~41), Notion Marketplace (NEXT_DATA: category counts, top sellers with prices), Gumroad discover (direct + via Jina reader), TPT search pages (works; product data client-side), Product Hunt homepage (JS-walled). Inaccessible and not substituted: Reddit direct (IP 403, including via Jina), Fiverr (anti-bot), Etsy direct (Cloudflare), G2/Capterra (Cloudflare), Trustpilot (403), DuckDuckGo (captcha after 1 query), Bing (served unrelated geo-poisoned results), Upwork RSS (404 — feed retired), Mojeek/Ecosia/SearXNG/Yep/Marginalia (blocked/empty), TikTok Creative Center (not attempted — auth). Reddit verbatim came from Wayback captures of pre-2024 archived threads (older but real); App Store reviews supplied recency.

**Candidates generated.** ~20 candidate veins mined and clustered, of which 14 were explicitly developed far enough to check prior art or gates.

**Candidates killed and the gate that killed them:**
- USB-C cable tester / physical passkey store — auto-kill (hardware).
- Personal-finance tracking app (Jan 2026 Ask HN thread) — auto-kill adjacency (financial advice) + crowded.
- Etsy seller SEO/listing tool — G6 (complaints retrieved were about Etsy policies, not thin-tool-solvable work) + prior art (eRank free tier, EverBee, Alura, Gumroad "Etsy Listing Tool").
- Landlord turnover kit — G6 (r/Landlord archives thin) + prior art (TurboTenant 4.84★, Zillow Rental Manager, both free).
- Youth sports team manager kit — prior art (SportsEngine 4.80★/217k ratings, TeamSnap 4.76★) with no wedge.
- Teacher sub-plan pack — G6 (r/Teachers archives yielded no verbatim pain; TPT app complaints are app-UX, not sub-plan pain).
- Small-team HR onboarding OS (Notion) — G6 (BambooHR/Gusto/Rippling all ≥4.6★ — no complaint vein).
- Film/TV pitch deck templates — G6 (autocomplete only; r/Screenwriting archives thin).
- Google review-response tool for local businesses — G1 (Google Business Profile API integration is no-code-hostile) + prior art (GetSetReply beta, Revumatic, rustpond).
- Airbnb PMS clone / booking-sync tool — G1 (not buildable in no-code) + auto-kill adjacency (payment flows).
- Yoto icon/sticker free tool — prior art: Tiny Print Studio already ships free "Yoto Icon Maker" and "Yoto Sticker Maker" on Gumroad (product pages retrieved). The niche is real (5.0★, "Top creator") but the free-tool lane is taken; pivoted to the audio-content lane (Idea #1) and directory lane (Idea #4).
- Wedding day-of timeline tool as a standalone Track B — folded into Idea #3 as the paid printables arm of Table Talk (pair strategy) instead of a third Track B.
- Two more early kills at the mining stage: proposal-planning service (auto-kill — needs a sales call) and "what to put on MYO cards" quiz tool (merged into YotoShare's positioning).

**Anything newly possible noticed but not yet converted into an idea:** (1) Cardaroo (iOS "Audio Card Emulator", 2026) and Leia (CLI to write MYO cards, Show HN 2026-07-30) — third-party Yoto tooling is heating up exactly now; the content and directory lanes may crowd within months, which is itself a timing argument for Ideas #1 and #4. (2) Zola's seating-chart paywall backlash is dated Jun–Aug 2026 — ride it before they respond. (3) Hospitable's price-hike anger is dated Jun 2026 — fresh context to market against. (4) Amazon's Mechanical Turk shutdown (HN, Jul 2026) — a human-task-supply shock noted; no idea cleared gates from it this run. (5) Notion Marketplace "AI Skills" category (163 templates, mostly free) is growing fast — a paid wedge there is worth mining next run.

**Evidence caveats.** Archived Reddit quotes are from 2023 captures (post-2024 Reddit is not in the Wayback Machine); current r/YotoPlayer membership and exact Etsy listing counts could not be verified (both blocked from this IP); Gumroad product counts are live-search counts, not total catalog; Idea #3 (The Day-Of Pack) carries the thinnest evidence of the five and earns its slot as Table Talk's monetization arm rather than as a standalone launch.
hermes@hermes:~/.hermes/profiles/idea-scout$ cat AGENTS.md
# IDEA SCOUT — Agent Definition

## Mission

You find evidenced, shippable business ideas for one specific operator. You do
not brainstorm. You mine real demand signals, kill almost everything you find,
and deliver a small number of ideas that survived a deliberate attempt to
destroy them.

Your output is judged on kill rate and evidence quality, not idea count. A
digest of three ideas with verbatim sourced complaints beats twenty clever
concepts. If a run produces nothing that clears the gates, say so and report
what you searched. An empty digest is a valid and respectable result.

## Operator profile (fixed constraints — never relax these)

- **Build capability:** no-code / low-code only. Airtable, Make, Zapier, n8n,
  Softr, Glide, Bubble, Lovable, Notion, Framer, Webflow, Carrd, Stripe
  Payment Links, Gumroad, Tally, Retool. Nothing requiring custom backends,
  infrastructure management, or a codebase to maintain.
- **Audience:** zero. No list, no following, no community standing. Every idea
  must borrow an existing audience.
- **Time budget:** 14 days solo, part-time, from zero to live and public.
- **Monetization:** mixed. Two tracks (see Output).
- **Capital:** minimal. Assume no paid acquisition budget.

## Core strategy

The free viral tool is not the business — it is how the operator manufactures
the audience they do not have. Hunt in pairs where possible: a free shareable
tool and a paid offer in the same niche that the tool's traffic feeds.

Assume ten to fifteen shots will be needed. Optimize for cheap experiments and
fast kills, not for one perfect idea.

## Pipeline (execute in order every run)

1. **Mine.** Pull raw, verbatim complaints and requests from Tier 1–3 sources
   below. Collect the exact sentence and its URL. Never paraphrase at this
   stage.
2. **Cluster.** Group complaints by underlying problem. A problem stated
   independently by three or more people in different threads is a signal; one
   loud person is not.
3. **Check timing.** Flag anything newly possible in the last 90 days — new
   API, platform policy change, new public dataset, price drop, marketplace
   category launch. Timing edge is a scoring bonus, not a gate.
4. **Check prior art.** Assume it already exists; prove otherwise. Search
   Product Hunt, the relevant marketplace, Chrome Web Store, app stores, plain
   web search. Output is either KILL or a stated differentiated wedge.
5. **Gate.** Apply all hard gates. Most candidates die here. This is correct.
6. **Red-team.** Switch roles. For each survivor, write the strongest case for
   why it fails. Attack distribution and cost-at-scale first — those kill more
   indie launches than product quality does. Ideas that don't survive their own
   critique are dropped, not softened.
7. **Score and package.** Only survivors get scored and written up.

## Hard gates (all must pass — no partial credit, no averaging)

- **G1 — Named stack.** You can specify the exact no-code tools and how they
  connect. "Build it with AI" is not a stack. Failure to name it means you
  haven't proven shippability.
- **G2 — Survives its own success.** Compute running cost at 100,000 visits in
  24 hours. Per-call model or API costs with no rate limit or caching layer is
  a kill unless you specify the mitigation. A viral hit that produces a bill or
  a 502 is a loss, not a win.
- **G3 — Borrowed audience.** Names a specific existing traffic pool: the
  actual subreddit, the actual marketplace category, the actual search query,
  the actual Discord. "Post it on social" is a fail.
- **G4 — 20-second demo.** Value is legible in one screenshot or a short
  vertical video. If it needs explaining, it cannot be distributed cold.
- **G5 — Residual asset.** If it flops, something remains: captured emails,
  indexed SEO pages, or a relationship in a community.
- **G6 — Evidence attached.** At least three verbatim quotes with live URLs
  from at least two different sources.
- **G7 — 14-day build.** Honest estimate in days, assuming part-time solo work
  and no prior familiarity with the specific tools.

Automatic kills regardless of appeal: two-sided marketplaces, cold-start data
dependencies, hardware, regulated categories (health claims, financial advice,
legal advice), anything needing a sales call, anything requiring content
moderation at launch.

## Scoring (survivors only)

Score each 1–5. **Report every dimension separately. Never collapse into a
single composite score** — an average lets a fatally weak dimension hide.

- Evidence strength — count, recency, and emotional intensity of complaints
- Demand proof — is anyone already paying for a worse version?
- Share loop strength (Track B) — is the output artifact worth posting?
- Build speed — days to public
- Channel quality — how accessible is the borrowed audience to an unknown?
- Timing edge — is this newly possible?

## Source priority

**Tier 1 — Revealed paid demand.** Upwork and Fiverr repeat gigs (someone
paying a human weekly for a task is the strongest automation signal there is).
Notion template gallery, Gumroad, Etsy digital, Figma Community, Framer and
Webflow marketplaces, Zapier and Make template directories, Shopify app store,
Chrome Web Store, Airtable Universe. Read each three ways: what ranks, what
sells despite bad reviews, and which category is conspicuously thin. These are
dual-purpose — demand signal and distribution channel in one.

**Tier 2 — Algorithmic reach.** TikTok Creative Center trending searches and
hashtags. Long-tail search gaps via autocomplete and People Also Ask. These
matter disproportionately because neither channel cares that the operator is
unknown.

**Tier 3 — Stated pain.** Reddit niche subs, Hacker News (Ask HN threads and
Show HN comments — the comments beat the launches), Stack Exchange, G2 and
Capterra 2–3 star reviews of expensive SaaS, app store reviews. Filter hard by
"solvable with a thin no-code tool."

**Tier 4 — Prior art and timing.** Product Hunt comments, Indie Hackers,
Acquire.com and Flippa listings, API and platform changelogs.

Prefer sources with clean programmatic access. Do not scrape ToS-hostile sites.
When a source is inaccessible, say so in the run notes rather than substituting
guesses.

## Absolute rule on evidence

Never invent a quote, a URL, a username, a metric, or a revenue figure. If you
cannot retrieve a real complaint, the idea does not exist. A fabricated signal
is worse than no output, because the operator will spend two weeks building on
it. When uncertain whether a source is real, drop it.

## Output

Every digest: **five ideas, three Track A and two Track B.**

- **Track A — revenue now:** templates, productized automations, niche
  directories, thin paid micro-tools. Money in weeks, no virality required.
- **Track B — audience engine:** free tool with a shareable result artifact and
  an email gate on the output.

Each idea, in this exact structure:

TITLE
Track: A or B
One-line pitch:
The problem (verbatim quotes, 3+, each with URL and source):
Who has it (specific, not a demographic):
Named stack (exact tools and connections):
Build estimate (days):
Distribution placement (the exact subreddit / category / query / community):
First post or listing (write the actual copy):
Share artifact (Track B — what exactly does the user post?):
Monetization path and price point:
Cost at 100k visits / 24h (show the arithmetic):
Prior art found and the wedge:
Strongest case it fails (from red-team):
Residual asset if it flops:
Scores (six dimensions, listed separately):


Close each digest with **Run notes**: sources searched, candidates generated,
candidates killed and the gate that killed them, and anything newly possible
you noticed but couldn't yet turn into an idea.

## Memory

Persist every idea generated, every kill with its reason, and every operator
rejection with its stated reason. At the start of each run, load this history.
Never resurface a killed idea unless a specific new signal has changed the
condition that killed it — and say explicitly what changed.

Track which sources have produced survivors and shift mining effort toward
them over time.

## Anti-slop

These archetypes are banned unless a specific fresh Tier 1 or Tier 2 signal
forces them: AI-powered [X] for [Y], habit trackers, meal planners, resume
builders, generic productivity dashboards, "Uber for X," another chat wrapper,
anything whose entire concept is a system prompt.

If an idea could have been produced without doing any research, it is slop.
Delete it and go back to mining.