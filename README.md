**Astro Migration Playbook**

0 of 83 checked

EnactOn playbook

# Astro Migration Checklist

A Plain-Language Playbook for New Builds and Migrations

Moving a website to Astro is not hard because of Astro. It is hard because a website has hundreds of small things that work today and nobody remembers they exist: a button, a redirect, a table, a tracking tag, a link from another site. Teams launch, then find these things broken.

This checklist runs from day one to the first 90 days after launch.

**Check**what to do**Why**why it matters**If skipped**what you will face

## Who this is for

### Building a new site or a new design

**Biggest risk:** pages nobody finds, and pages that compete with each other in search.

**Focus on:** keyword research and the competition checks.

### Moving your site to Astro, same design and content

**Biggest risk:** things quietly going missing: links, structured data, buttons, forms.

**Focus on:** the link checks and the page-by-page content comparison.

### Moving to Astro and redesigning at the same time

**Biggest risk:** not knowing what caused a traffic drop.

**Focus on:** both sets of checks, and a written list of every change.

**83**checks to complete

**79**"if you skip it" warnings, each explained

**14**real problems from our own migration

**12**phases, from day one to day 90

[Phase 1Copy your old site, then save the key data](#phase-1-copy-your-old-site-then-save-the)[Phase 2Decide your URLs](#phase-2-decide-your-urls)[Phase 3ANew design path (content, keywords, competition between pages)](#phase-3a-new-design-path-content-keyword)[Phase 3BOld design path (links, structured data, URL checks)](#phase-3b-old-design-path-links-structure)[Phase 4Content parity (nothing missing on the new pages)](#phase-4-content-parity-nothing-missing-o)[Phase 5Staging and the safety net](#phase-5-staging-and-the-safety-net)[Phase 6Audit staging, by hand and with AI agents](#phase-6-audit-staging-by-hand-and-with-a)[Phase 7Mobile checks](#phase-7-mobile-checks)[Phase 8Forms, tracking and integrations](#phase-8-forms-tracking-and-integrations)[Phase 9Launch day](#phase-9-launch-day)[Phase 10After launch: new sitemap, Google Search Console, Bing Webmaster Tools](#phase-10-after-launch-new-sitemap-google)[Phase 11Monitoring after launch](#phase-11-monitoring-after-launch)[Part 12Real problems from EnactOn's own WordPress to Astro migration](#part-12-real-problems-from-enacton-s-own)[Part 13Frequently asked questions](#part-13-frequently-asked-questions)[Last noteAbout this playbook](#last-note-about-this-playbook)

Jump to a phase

[Phase 1Copy your old site, then save the key data](#phase-1-copy-your-old-site-then-save-the)[Phase 2Decide your URLs](#phase-2-decide-your-urls)[Phase 3ANew design path (content, keywords, competition between pages)](#phase-3a-new-design-path-content-keyword)[Phase 3BOld design path (links, structured data, URL checks)](#phase-3b-old-design-path-links-structure)[Phase 4Content parity (nothing missing on the new pages)](#phase-4-content-parity-nothing-missing-o)[Phase 5Staging and the safety net](#phase-5-staging-and-the-safety-net)[Phase 6Audit staging, by hand and with AI agents](#phase-6-audit-staging-by-hand-and-with-a)[Phase 7Mobile checks](#phase-7-mobile-checks)[Phase 8Forms, tracking and integrations](#phase-8-forms-tracking-and-integrations)[Phase 9Launch day](#phase-9-launch-day)[Phase 10After launch: new sitemap, Google Search Console, Bing Webmaster Tools](#phase-10-after-launch-new-sitemap-google)[Phase 11Monitoring after launch](#phase-11-monitoring-after-launch)[Part 12Real problems from EnactOn's own WordPress to Astro migration](#part-12-real-problems-from-enacton-s-own)[Part 13Frequently asked questions](#part-13-frequently-asked-questions)[Last noteAbout this playbook](#last-note-about-this-playbook)

Phase 1

## Copy your old site, then save the key data

**Applies to:** anyone who already has a live site.

**Quick rule:** before you change anything, keep a full working copy of the old site.

## Step 1: Copy the old site to an "old" address

Make a full working copy of your current site at its own address, for example `old.yoursite.com`. This is a copy, not a move: your real site stays live at the normal address until launch day. The copy is only for your team.

| Why | If you skip it |
| --- | --- |
| **It is your "before" picture.** Open any old page next to the new one whenever you like. You do not need screenshots | You rely on screenshots and memory, and argue later about what a page used to look like |
| **It is your way back.** If something breaks after launch, the old site is still there | A broken launch stays broken until someone rebuilds the old site |
| **You can recover what you missed:** text, images and files that did not move | Missing content has to be rebuilt from scratch |
| **You can test redirects against real old pages** | Redirects are tested only against a spreadsheet |

**Protect the copy.** Put noindex and a password on it, the same as staging (see Phase 5, Step 2). Otherwise two full copies of your website compete in Google. Also check that forms on the copy do not send leads to your real inbox, and that its links do not all point back to the live site.

**How long to keep it:** until your post-launch checks are clean and traffic and leads are stable. Many teams keep it for 30 to 90 days. This is a safe habit, not a fixed rule.

## Step 2: Save the key data

The copy shows you how pages look. It does not tell you what matters most or where your traffic comes from. Save this before building anything:

| What to save | Why it matters | If you skip it |
| --- | --- | --- |
| **A full list of every page address.** Combine a crawl of your site, your sitemap, pages shown in Search Console, and pages shown in your analytics | Pages that are not on the list do not get moved, and nobody notices until visitors do | Old pages quietly disappear. Visitors and search engines land on error pages |
| **For every page: title, meta description, main heading (H1), canonical tag, and whether it is set to noindex** | These control how your page shows in Google and what it is understood to be about | Search results show different titles and descriptions than before, and clicks drop |
| **Which pages get the most traffic, clicks and leads** (last 3 to 6 months) | Tells you which pages you must protect first | You treat a page earning 5 leads a week the same as a forgotten one, and break the wrong thing |
| **Which pages have links from other websites pointing to them** | Those links carry trust. If the page moves without a redirect, the trust is lost | You lose the benefit of links you worked hard to earn |
| **Every form, chat tool, tracking tag, and connected tool** (CRM, email, analytics, ad pixels) | These are the invisible parts that make the site work for your business | Leads stop arriving, or ad and analytics numbers go blank and nobody knows why |
| **Existing redirects** (from your old platform, plugins, or server rules) | Old redirects protect old links. If you do not carry them over, they break | Links that worked for years suddenly return errors |
| **Speed and Core Web Vitals scores** (Lighthouse or PageSpeed Insights) | Your baseline. You can show the improvement, or catch a drop | You cannot prove if the new site is faster or slower |

Checklist for this phase

- [ ] Old site copied to its own address, with noindex and a password
- [ ] Copy checked: forms do not reach the real inbox
- [ ] Full URL list created and saved
- [ ] Page-level details (title, description, H1, canonical, robots) exported
- [ ] Top pages by traffic and leads marked as "protect first"
- [ ] Pages with outside links marked
- [ ] List of forms, tools, and tracking tags written
- [ ] Existing redirects exported
- [ ] Speed baseline saved

Phase 2

## Decide your URLs

**Applies to:** anyone who already has a live site.

**Quick rule:** keep the same URL unless you have a strong reason to change it.

Every page has an address. Search engines, other websites, and your visitors' bookmarks all point to those addresses. You have two choices.

## Option 1: Keep the same URLs (best choice when possible)

If your old page is at `/services/web-development/`, the new Astro page should live at exactly `/services/web-development/`.

- **Why:** nothing needs to be redirected, so nothing can break in the redirect.
- **If you skip it:** every changed address is a chance to lose ranking and links.

**One detail people forget:** `/page` and `/page/` (with and without the last slash) are treated as two different addresses. Pick one style, set Astro and your hosting to use it, and use it everywhere: links, sitemap, canonical tags. If you do not, you can end up with two copies of every page.

## Option 2: Use new URLs

Sometimes new URLs are needed: a new site structure, merged pages, a cleaner naming system. If so, you must build a **redirect map**.

**What it is:** think of the form you fill in at the post office when you move house. Anyone who still writes to your old address gets their mail forwarded to the new one. On a website, the "people writing to the old address" are Google, other websites that link to you, and visitors with a bookmark. The redirect map is the list that says, for every old page, where to forward it.

**How to build it:**

1. Open the full page list you saved in Phase 1.
2. Mark every page whose address will change on the new site.
3. For each one, write down the address of the closest matching new page.
4. Give the list to your developer to set up as permanent (301) redirects, and test them on staging.

**Example:**

| Old address | New address | What it means |
| --- | --- | --- |
| `/services/web-development/` | `/web-development-company/` | The page moved. Anyone opening the old address lands on the new page, and Google learns the page has moved and passes its ranking strength across |
| `/blog/2019/astro-tips/` | `/blog/astro-tips/` | The date was dropped from the address. Old links from other websites still work |

**Pages that do not go on the list:**

- A page that keeps the same address needs no redirect.
- A page you are removing for good has no new home. Let it show "page not found" (404 or 410) instead of forwarding it somewhere unrelated.

**The rules for a good redirect map**

| Rule | Why | If you break it |
| --- | --- | --- |
| **Use a permanent redirect (301)** | Tells search engines the move is for good, so they pass the old page's strength to the new one | Search engines may keep the old address and treat the new one as a new, unproven page |
| **One hop only.** Old address goes straight to the final address | Chains (old, then middle, then final) slow things down and can lose signals | Pages load slower. Google follows up to 10 hops, then stops, so a long chain can leave the final page undiscovered |
| **Send each old page to the closest matching new page** | Visitors and search engines expect the same topic | Sending everything to the homepage looks like an error to Google and confuses visitors |
| **Pages with no replacement should return "not found" (404) or "gone" (410)** | It is honest, and Google drops pages that return either code from its index (it treats 404 and 410 very similarly) | Redirecting dead pages to the homepage hides the problem and creates a poor experience |
| **Keep redirects live for at least a year** (longer is better) | Google needs time to process the move, and old links keep existing for years | Redirects removed too early bring back old errors and lost traffic |

## Decide what happens to every page

Go through your URL list from Phase 1 and give every page one decision:

| Decision | Use it when |
| --- | --- |
| **Keep** | The page ranks, converts, earns links, or supports sales. Keep the URL and the meaning of the content |
| **Improve** | The page is useful but weak. Keep the URL and topic, upgrade the content, and write down what changed |
| **Merge** | Several pages compete for the same search. Build one stronger page and redirect the others to it |
| **Redirect** | The page is going away but has traffic or links, and there is a close replacement |
| **Noindex** | Useful for visitors, but should not show in search (for example, thank-you pages) |
| **Remove** | No traffic, no links, no replacement |
| **Investigate** | Nobody is sure. Do not launch until someone decides |

Checklist for this phase

- [ ] Decided: same URLs or new URLs
- [ ] Trailing slash style chosen and set
- [ ] Every old page has a decision
- [ ] Redirect map built (if URLs change)
- [ ] Redirect rules reviewed: 301, one hop, closest match

Phase 3A

## New design path (content, keywords, competition between pages)

**Applies to:** new builds, and moves with a redesign.

**Quick rule:** every page should have one clear job in search, and no two pages should have the same job.

A new design usually means new content. That is a chance to do search work properly, and also a chance to hurt yourself if you skip it.

## Step 1: Plan your pages

Write down every page the new site will have, and for each one, decide: new, rewritten, or carried over.

- **Why:** this stops pages being built "because the design had room for one".
- **If you skip it:** you end up with thin pages, duplicates, and gaps where visitors expected an answer.

## Step 2: Do keyword research for every page

For each page, find the words people actually type into search when they want what that page offers. Choose one **main keyword** and a few **supporting keywords**. Also write down the **search intent**: what is the person really looking for? A how-to guide? A price? A list of options? A company to hire?

Put it all in a **keyword map**:

| Page URL | Main keyword | Supporting keywords | What the searcher wants | Status |
| --- | --- | --- | --- | --- |
| `/astro-migration-services/` | astro migration services | hire astro developer, website to astro | Find a company to do the work | New |
| `/blog/astro-migration-checklist/` | astro migration checklist | astro migration steps | A step-by-step guide to follow | New |

- **Why:** search engines match pages to what people want. A page written without a keyword and intent in mind often matches nothing.
- **If you skip it:** pages look good but nobody finds them. Traffic after launch is lower than before.

## Step 3: Optimize every page for its keyword

For every page, check these items against its main keyword:

| Item | What to check | Why |
| --- | --- | --- |
| **Main heading (H1)** | Contains the main keyword, written for a human | The H1 is the strongest signal of what the page is about |
| **Page title** (the title tag, shown in search results) | Contains the keyword, makes people want to click | It is the headline people see in Google |
| **Meta description** | Describes the page honestly and invites the click | It is the short text under the title in search results |
| **URL** | Short, readable, contains the keyword | Easier for people and search engines to understand |
| **Subheadings** | Cover related questions people ask | Helps the page answer more searches |
| **First paragraph** | Answers the main question quickly | Visitors and search engines both look here first |
| **Images** | Descriptive file names and alt text | Helps accessibility and image search |
| **Internal links** | Link to related pages with clear link text | Spreads strength across your site and helps visitors move around |
| **Structured data (schema)** | Added where it fits: article, FAQ, organization, breadcrumb, product | Helps search engines understand the page |

**If you skip it:** the new pages are well designed but carry weaker signals than the old ones. Rankings slip.

## Step 4: Check for competition between your own pages (cannibalization)

**What it is:** two or more of your pages target the same search. Google has to guess which one to show. It may pick the weaker page, or swap between them, so neither ranks well.

**How to check, in order:**

1. **Look at your keyword map.** If the same main keyword appears on two rows, you have a problem before you start.
2. **Search Google for your keyword with your site name,** for example `site:yoursite.com "astro migration checklist"`. If several pages appear that could each answer the question, they may be competing.
3. **In Search Console,** open Performance, click a keyword, then open the Pages tab. If many of your pages show for that one keyword, they are competing.
4. **Check the whole site, not only the new pages.** Old pages that you carried over can compete with the new ones.

**How to fix it:**

| Situation | Fix |
| --- | --- |
| Two pages say nearly the same thing | **Merge** them into one stronger page and 301 redirect the weaker one |
| Two pages cover different needs but share a keyword | **Change the focus** of each: different main keyword, different title, different H1 |
| A page exists only as a duplicate (for example a print version) | Use a **canonical tag** to point to the main page |
| A page is useful to visitors but should not rank | Set it to **noindex** |

- **Why:** one strong page beats two weak ones.
- **If you skip it:** rankings go up and down, the "wrong" page shows in search, and you cannot tell why traffic dropped after launch.

## Step 5: Write content that is worth reading

- Answer the real question on the page, not around it.
- Keep proof, tables, FAQs, and examples that helped the old pages.
- Do not change the meaning of a page that already ranks. If it ranks for "astro migration checklist", the new version must still be clearly about that.
- **If you skip it:** thin or vague content ranks poorly, and AI answer tools have no reason to quote you.

Checklist for this phase

- [ ] Page list written (new, rewritten, carried over)
- [ ] Keyword map built (one main keyword per page)
- [ ] Search intent written for each page
- [ ] Titles, H1s, descriptions, and URLs match the keyword map
- [ ] Cannibalization checked across the whole site
- [ ] Duplicate topics merged, separated, or noindexed
- [ ] Content for ranking pages keeps the same meaning
- [ ] Schema planned for each page type

Phase 3B

## Old design path (links, structured data, URL checks)

**Applies to:** moves that keep the design, and moves with a redesign.

**Quick rule:** if the design stays, the site must behave exactly the same.

When you keep the old design, visitors expect nothing to change. Your job is to rebuild the same site on a new foundation, with nothing lost.

| Check | How | Why | If you skip it |
| --- | --- | --- | --- |
| **Broken internal links** (links from one of your pages to another) | Crawl the old site and the staging site. List every link that returns an error | Broken links frustrate visitors and waste the attention of search engines | Visitors hit error pages. Search engines stop trusting the site's structure |
| **Broken external links** (links from your pages to other websites) | Same crawl, filter for outside links that fail | Dead outside links make pages look neglected | Pages look outdated and visitors leave |
| **Internal links match the old site** (menu, footer, breadcrumbs, related posts, links inside text) | Compare link counts for important pages, old versus new | Internal links tell search engines which pages matter most | Important pages lose strength because fewer pages point to them |
| **Links point to final addresses, not redirected ones** | In the staging crawl, filter for links that return a 301 | Redirects are a safety net, not the plan | Slower pages and weaker signals |
| **Structured data (schema) is the same** | List schema types per page type (article, FAQ, breadcrumb, organization, product). Test on staging with Google's Rich Results Test or the Schema Markup Validator | Schema helps search engines and AI tools understand your pages | Schema disappears silently. The page still looks fine, so nobody notices |
| **Titles, descriptions, H1, canonical, and robots tag match the Phase 1 export** | Crawl staging and compare against the Phase 1 export | These are what search results are built from | Titles in Google change overnight, and clicks drop |
| **Social sharing tags** (the preview image, title and text when someone shares a link) | Check each page type in a share preview | First impression in social posts and chat apps | Shared links look broken or empty |
| **Images and downloads load from working addresses** | Check that every image and PDF loads. Watch for old address patterns from your previous platform | Image paths often change when the platform changes | Empty boxes where images used to be, and broken PDF links |

Checklist for this phase

- [ ] Broken internal links fixed
- [ ] Broken outside links fixed or removed
- [ ] Menu, footer, breadcrumb, and in-text links match the old site
- [ ] Internal links point to final addresses
- [ ] Schema compared page type by page type and tested
- [ ] Titles, descriptions, H1s, canonicals match the Phase 1 export
- [ ] Social sharing tags checked
- [ ] Images and downloads load

Phase 4

## Content parity (nothing missing on the new pages)

**Applies to:** moves that keep the design, and moves with a redesign.

**Quick rule:** a page has not migrated just because the new page exists. It has migrated when it contains everything the old page did.

This is the phase most teams underestimate. A page can load, look fine, and still be missing a button, a section of cards, a table, or half the FAQs. It is especially common when pages are rebuilt by scripts, scrapers, or AI tools that read the old site and generate the new one. Section 12 of this playbook lists the real problems found on EnactOn's own migration.

## The page-by-page parity check

Open the old page and the new page side by side. Go from top to bottom. Tick every item:

| Item | What to compare | Why it matters |
| --- | --- | --- |
| **Title and meta description** | Same text, or an approved improvement | Controls what shows in search results |
| **Headings, in order** | Same headings, same order, same levels | Search engines read the heading order to understand the page |
| **Body text** | Every paragraph is present, nothing duplicated | Missing text means missing keywords and missing answers |
| **Cards** | Title, description, icon, and image on each card | Scripts often copy the title and skip the rest |
| **Buttons and links** | Every button is visible, has the right text, and goes to the right place | A button can exist in the data and still not appear on screen |
| **Lists** | Same items, same order | Lists often hold the most useful details |
| **Tables, including pricing and comparison tables** | Headers, descriptions, all rows, and any button inside the table | Tables are often partly copied |
| **FAQs** | Every question and answer | FAQs answer real searches and are often quoted by AI answer tools |
| **Testimonials and proof** | Names, quotes, logos, ratings | Trust content drives leads |
| **Images** | The right image in the right place, with alt text. No empty placeholders | Wrong or missing images are very visible |
| **Videos and embeds** | Play correctly | Often break on platform change |
| **Forms** | Show up, submit, and deliver | See Phase 8 |
| **Whole sections** | Process steps, timelines, comparison matrices, calls to action | Entire sections can be missed by automated tools |
| **Grouping** | Things that were together on the old page are still together | A benefit under a pricing plan can end up in a different section |

## How to make this check faster and safer

1. **Group pages by type** (service page, industry page, case study, blog post, landing page). Fix the template for each type, then check every page of that type.
2. **Expect variations.** Pages of the same type are often built a little differently. A fix that works for 9 pages may break the 10th.
3. **After any change to a template, check all pages of that type again.** Fixing one problem can cause another.
4. **Compare your page list with your live sitemap.** Pages that exist on the old site but not in the new project are easy to miss.
5. **Never trust automated output without a visual check.** Scripts are fast, but they miss things.

Checklist for this phase

- [ ] Page types listed
- [ ] Parity check completed for every page, or for every page type plus the top pages
- [ ] Page list compared against the live sitemap
- [ ] Missing pages found and moved
- [ ] After each template fix, all pages of that type rechecked

Phase 5

## Staging and the safety net

**Applies to:** everyone.

**Quick rule:** nothing goes live until you are 100% sure. Build and review everything on staging first.

## Step 1: Build on a staging site

A staging site is a private copy of the new website at a separate address (for example `staging.yoursite.com`, or a preview address from your hosting). It looks and works like the real site, but only your team should be able to see it.

Build the new site there, including every new or rewritten page. Do not publish any of it to the live site while you work. The live site keeps running as it is until the audit in Phase 6 is clean and you are sure.

- **Why:** it is the only safe place to find problems.
- **If you skip it:** you find problems when real visitors and Google do, and you fix them in public.

## Step 2: Keep staging out of search results (noindex, and a password)

Add the **noindex** setting to every page on staging, **and** protect the staging site with a password or by limiting access to your team.

| Why you do this | If you do not |
| --- | --- |
| **Search engines can find staging by accident.** They follow links, and a link in an email or a shared document is enough | Your unfinished site appears in Google |
| **A staging copy is a duplicate of your real site.** Two near-identical sites compete with each other | The staging address can outrank your real pages, or Google picks the wrong version as "main" |
| **Unfinished or test content is visible to everyone** | Placeholder text, draft prices, and test pages are public |
| **Staging pages may carry the wrong canonical tags** | Google treats the staging address as the main address |

**Do not rely on robots.txt alone.** A robots.txt "block" asks search engines not to visit a page. But search engines can still list the address if they find a link to it, and because they are not allowed to visit, they cannot see the noindex note on the page. Use noindex plus a password. Use robots.txt as an extra, not as the only protection.

## Step 3: Write your rollback plan before launch

A rollback plan answers three questions in advance:

1. **What counts as "bad enough" to go back?** For example: the homepage is down, forms do not deliver, or noindex is live on production.
2. **Who decides?** One named person, available on launch day.
3. **What are the steps?** Written down, with the person who does each step.

Also, if your domain's DNS settings have a "time to live" (TTL) value, lower it a day or two before launch. This makes switching back faster. (This is common practice, not a Google requirement. Ask your hosting provider how it works for your setup.)

- **Why:** deciding under pressure leads to bad choices.
- **If you skip it:** teams argue for hours while the site is broken.

Checklist for this phase

- [ ] Staging site built
- [ ] Staging has noindex and a password
- [ ] Rollback plan written, with an owner

Phase 6

## Audit staging, by hand and with AI agents

**Applies to:** everyone.

**Quick rule:** use machines to check everything, and humans to check what matters most.

Once you have finished the cannibalization check, the redirect check, the internal and external link check, and the keyword check, do not launch yet. Audit the whole staging site first.

## Step 1: Crawl the staging site with a tool

Use a crawler (for example Screaming Frog, Sitebulb, or similar) and look for:

| What to look for | Why | If you skip it |
| --- | --- | --- |
| Pages returning errors (404, 500) | Broken pages | Visitors hit dead ends |
| Redirect chains and loops | Slow pages, pages that never load | Pages never get indexed |
| Missing or duplicate titles and descriptions | Weak search results | Pages blend together in Google |
| Missing or multiple H1 headings | Unclear page topic | Search engines misread the page |
| Wrong canonical addresses | Tells Google the wrong "main" version | The wrong page ranks, or none |
| Noindex tags where they should not be (and the reverse) | On staging they should be on. On the real site, they should be off | Pages vanish from search |
| Images with no alt text or broken paths | Accessibility and image search | Empty boxes and lost image traffic |
| Pages with very few words | Possible missing content | Thin pages that rank poorly |

## Step 2: Test every redirect

Take the full list of old addresses and request each one. Confirm:

- [ ] It lands on the correct new page
- [ ] It uses a 301
- [ ] It takes one hop
- [ ] There is no loop
- [ ] The http to https and www to non-www (or the reverse) versions also land on the right page
- [ ] Capital letters and trailing slashes behave as planned

## Step 3: Re-run the cannibalization check on the final set of pages

Plans change while building. Check again with the real pages and real titles.

## Step 4: Manual review by a person

Tools do not see what a human sees. Have a person read:

- **Every page that earns traffic or leads**, top to bottom, on desktop and on phone.
- **A sample of every other page type.**

Look for: missing sections, text that cuts off, wrong images, buttons that do nothing, odd spacing, pages that feel unfinished.

## Step 5: Use AI agents as a second pair of eyes

AI agents are good at checking many pages quickly. Give them clear, narrow jobs. Examples of tasks that work well:

| Task for an AI agent | What it catches |
| --- | --- |
| "Compare this old page and this new page. List everything on the old page that is missing from the new page: headings, paragraphs, buttons, images, tables, FAQs, links" | Missing content |
| "List every link on this page that returns an error or a redirect" | Broken and redirected links |
| "Check that every page has one H1, a title under 60 characters, and a meta description" | Basic on-page problems |
| "Read these two pages and tell me if they target the same search. Explain why" | Cannibalization suspects |
| "Check these pages for text that appears twice" | Duplicate content |
| "Compare the schema on the old and new version of this page" | Lost structured data |

**What AI agents are not good at:** judging whether the page *feels* right, noticing a button hidden by a layout problem, and knowing which pages matter most to your business. They can also report that "everything matches" when it does not. So always have a person verify the pages that matter, and spot-check the agent's own claims.

Checklist for this phase

- [ ] Staging crawled and issues fixed
- [ ] Every redirect tested
- [ ] Cannibalization rechecked on the final pages
- [ ] Top pages read by a person
- [ ] AI agent checks run, with spot checks on their results

Phase 7

## Mobile checks

**Applies to:** everyone.

**Quick rule:** a site that works on a laptop can still be broken on a phone.

Google mostly uses the **mobile version** of your pages to decide how to rank them. Many of your visitors are on phones. Mobile problems are some of the most common ones found after launch.

Test on **real phones** (at least one iPhone and one Android), and also in your browser's device mode. Check:

| Check | Why | If you skip it |
| --- | --- | --- |
| **The page scrolls smoothly, up and down** | Layout bugs can lock scrolling or cause jumps | Visitors cannot reach the content or the button |
| **There is no sideways scrolling** | A wide image, table or element pushes the page wider than the screen | The page feels broken and visitors leave |
| **The menu opens, closes, and every link works** | Menus often break on a new build | Visitors cannot get around the site |
| **Nothing overlaps** (sticky headers, banners, chat widgets, cookie notices) | Layers can cover buttons or text | Buttons cannot be tapped |
| **Tables are readable** | Wide tables often run off the screen | Pricing and comparison data become unreadable |
| **Buttons and links are big enough to tap** | Small targets cause mis-taps | Forms and calls to action get fewer clicks |
| **Forms can be filled in and submitted** | The keyboard can cover fields | Leads are lost |
| **Images are not cut off or stretched** | Image sizing often changes on mobile | The page looks unprofessional |
| **Text is readable without zooming** | Fonts and spacing can change | Visitors leave |
| **Pop-ups can be closed** | A pop-up with no visible close button traps the visitor | The site is unusable |
| **Page does not jump around while loading** | Images and fonts that load late push content down | Visitors tap the wrong thing, and your speed scores suffer |
| **Speed is acceptable on mobile** (run Lighthouse or PageSpeed Insights in mobile mode) | Phones are slower than laptops | Slow pages lose visitors and search visibility |

Checklist for this phase

- [ ] Tested on at least one iPhone and one Android phone
- [ ] Tested in browser device mode at several widths
- [ ] Scrolling, menu, tables, forms, buttons, and pop-ups checked
- [ ] Mobile speed scores checked
- [ ] Every issue logged and fixed

Phase 8

## Forms, tracking and integrations

**Applies to:** everyone.

**Quick rule:** a site can look perfect and still lose every lead.

Forms and tracking are the quiet parts of a website. They are rebuilt differently in Astro, and they break without an error message.

| Check | How | Why | If you skip it |
| --- | --- | --- | --- |
| **Every form submits and arrives** | Fill in each form on staging as a real visitor. Confirm the message reaches the right inbox or CRM with all fields | A form that shows "thank you" may still deliver nothing | Leads vanish, and you find out weeks later |
| **Thank-you pages and confirmation messages work** | Check what appears after submitting | Visitors need to know it worked | Visitors submit twice or leave unsure |
| **Spam protection still works** | Check captcha or other protection | Old plugins used to handle this | Spam floods the inbox |
| **Analytics records page views** | Visit pages and check the live reports | Your history and reports depend on it | You lose a stretch of data you cannot get back |
| **Conversion events fire** | Complete a test conversion and check it records | Reports and ad bidding use these | Reports show zero leads, and ad platforms stop learning |
| **Ad pixels and tags load** | Check tag manager and each pixel | Ads depend on them | Ad performance drops, and spending is wasted |
| **Cookie and consent notice works** | Check that tags respect the choices | Required in many countries | Legal risk, or tracking that does not fire |
| **Booking, chat, and CRM connections work** | Test each connection | These bring in business | A booking link that fails costs real deals |
| **Tracking tags load in a sensible order** | Check after a tag is added or moved | Order can change what is tracked | Numbers differ from before, and nobody knows why |

Checklist for this phase

- [ ] Every form tested end to end
- [ ] Thank-you pages checked
- [ ] Spam protection tested
- [ ] Analytics page views and events confirmed
- [ ] Ad pixels and tag manager confirmed
- [ ] Cookie notice tested
- [ ] CRM, booking, chat, and email connections tested

Phase 9

## Launch day

**Applies to:** everyone.

**Quick rule:** launch day should be boring. Everything has been decided and tested already.

Pick a quiet time. Avoid big campaigns, product announcements, and peak traffic. Freeze unrelated edits for the day. Have your rollback owner available.

| Launch item | What to confirm | Why | If you skip it |
| --- | --- | --- | --- |
| **Remove noindex from the live site** | View the page source of the homepage and several key pages. Search for `noindex`. None should be there | Staging used noindex. Carrying it across tells Google to ignore the site | The site disappears from search, sometimes for weeks |
| **Remove the staging password** from the live site | Open the site in a private window | Search engines cannot visit a password page | Nobody can see the site |
| **Canonical tags point to the real address** | Check a sample of pages | Staging canonicals tell Google the wrong "main" version | Google treats the staging address as the real one |
| **robots.txt is correct for production** | Open `yoursite.com/robots.txt`. Check it does not block pages you want found, and that old platform rules (for example, WordPress admin folders) are removed or still make sense | Staging often blocks everything | Nothing gets crawled |
| **The site address in Astro is set to the real domain** | Check the generated sitemap and canonical tags | Astro builds addresses from this setting | Sitemap and canonicals use the wrong domain |
| **Domain, hosting, and secure connection (https) are working** | Open the site with and without `www`, with `http` and `https` | Visitors should always land on one secure version | Warnings, duplicate versions, or errors |
| **Redirects are live** | Test a sample of old addresses, including the highest-traffic ones | Redirects tested on staging need to work on production hosting too | Old links break on day one |
| **Cache is cleared** (on your hosting and any content network) | Check you see the new version | Old versions can linger | Visitors see a mix of old and new |
| **Forms deliver to the real inbox or CRM** | Submit a real test | Staging forms point to test inboxes | Leads go to a test inbox |
| **Analytics and tags use live IDs** | Check live reports | Staging IDs can pollute your data | Data is lost or mixed with test traffic |

Checklist for this phase

- [ ] noindex removed (checked in page source)
- [ ] Password removed
- [ ] Canonicals correct
- [ ] robots.txt correct
- [ ] Site address setting correct
- [ ] https and www behavior correct
- [ ] Redirects live and sampled
- [ ] Cache cleared
- [ ] Forms and analytics tested on the live site

Phase 10

## After launch: new sitemap, Google Search Console, Bing Webmaster Tools

**Applies to:** everyone.

**Quick rule:** tell the search engines the new site exists, and tell them clearly.

Once the site is live, do these steps the same day.

## Step 1: Create a clean new sitemap

Astro can generate a sitemap with its official sitemap add-on (`@astrojs/sitemap`). Check that it only lists addresses that are:

- the **final** address of the page (not redirected)
- **indexable** (not set to noindex)
- **working** (not an error page)
- on the **real domain** (not staging)

| Why | If you do not |
| --- | --- |
| A sitemap is a map you hand to search engines. A clean map helps them find the right pages | A messy map sends search engines to redirects, errors, and test pages, and wastes their attention on pages you do not want |

## Step 2: Check that robots.txt points to the sitemap

Your robots.txt file should include the full address of your sitemap. This helps search engines that find the site by other routes.

## Step 3: Add and verify your site in Google Search Console

If you already have a property, check that it still verifies on the new site. If you use a different way of verifying, such as a file or a tag on the old site, it may need setting up again.

- **Why:** you cannot submit a sitemap, inspect pages, or see errors without it.
- **If you skip it:** you are blind. Problems go unseen for weeks.

## Step 4: Submit the sitemap in Google Search Console

Open Search Console, go to Sitemaps, and submit the sitemap address.

- **Why:** it tells Google where your pages are and speeds up discovery of the new site.
- **If you skip it:** Google still finds your pages, but more slowly, and you do not get a clear report on which pages it could not read.

## Step 5: Add and verify your site in Bing Webmaster Tools, and submit the sitemap there

Bing Webmaster Tools lets you import your site from Google Search Console, which saves time. Then submit the sitemap in the same way.

- **Why:** Bing's index also feeds other search products, such as Microsoft Copilot, Yahoo and DuckDuckGo. It is a smaller share than Google, but it costs very little to cover.
- **If you skip it:** your new pages are discovered more slowly on Bing and the products that rely on it. Bing's sitemap and crawl reports also show problems you would not see elsewhere.
- **Optional extra:** Bing supports IndexNow, a simple way to tell it right away when pages change. Many website tools support it.

## Step 6: Inspect your most important pages

In Google Search Console, use **URL Inspection** on your homepage and top pages. Confirm Google can reach them, that they are allowed to be indexed, and that the canonical address is the one you expect. You can request indexing for the most important ones. (There is a daily limit, so choose carefully.)

## Step 7: If you changed your domain name, use the domain-move process

If your site moved to a different domain or subdomain (for example `example.com` to `example.net`, or `a.example.com` to `b.example.com`), Google Search Console has a specific "Change of Address" tool. Use it. It is not needed for platform changes, URL path changes, or an http to https or www switch on the same domain.

Checklist for this phase

- [ ] Clean sitemap generated (final, indexable, working, real domain only)
- [ ] robots.txt references the sitemap
- [ ] Google Search Console verified
- [ ] Sitemap submitted in Google Search Console
- [ ] Bing Webmaster Tools verified
- [ ] Sitemap submitted in Bing Webmaster Tools
- [ ] Top pages inspected in URL Inspection
- [ ] Change of Address used, only if the domain or subdomain changed

Phase 11

## Monitoring after launch

**Applies to:** everyone.

**Quick rule:** launching is the start of the check, not the end.

Search engines need time to visit and understand the new site. Some movement in rankings and traffic is normal while this happens. What you are looking for is not "did anything move", but "are there errors we can fix".

**Before launch, agree on your warning line.** Decide what size of drop in clicks, over what time, makes the team stop and investigate. Write it down. Use your normal ups and downs, seasons and campaigns to set it. That way, nobody argues about it under stress, and normal ups and downs do not trigger panic.

| When | What to check | Why |
| --- | --- | --- |
| **First hour and first 24 hours** | Top pages load. Forms deliver. Old addresses redirect. Sitemap opens. robots.txt is right. No noindex on live pages. Search Console starts showing data | Critical problems are cheapest to fix right now |
| **First week** | Run a full crawl of the live site and compare it to your Phase 1 data. Look for new 404s, pages missing from the sitemap, sitemap addresses that redirect or are noindex, missing schema, missing images, mobile problems, and conversion gaps. Check Search Console for errors daily | Small mistakes show up here before they become ranking problems |
| **First month** | Compare clicks, impressions, ranking pages, leads, and form conversion rate against your baseline. Fix the biggest-impact issues first: a broken redirect on a page with outside links matters more than a missing alt tag on a minor page | Separates real problems from normal ups and downs |
| **Months 2 and 3** | Look for pages that lost rankings and also changed meaning. Look for pages not indexed, old addresses still getting visits, and sections with fewer internal links than before | Slow-moving problems appear here |

**Do not roll back just because rankings moved one day.** Rolling back is for broken pages, wrong noindex, failed forms and site errors. Reversing a healthy launch adds more changes and slows recovery.

Checklist for this phase

- [ ] Warning line agreed before launch
- [ ] 24-hour check done
- [ ] First-week crawl and comparison done
- [ ] First-month comparison against baseline done
- [ ] Months 2 to 3 review done

Part 12

## Real problems from EnactOn's own WordPress to Astro migration

EnactOn migrated its own WordPress website to Astro. The pages were rebuilt using migration scripts that read the live website and generated Astro pages. The result had many problems that were only found by comparing every page against the live site. These are the real ones, in plain language, with how to catch each one.

| # | What went wrong | What it looked like | How to catch it before launch |
| --- | --- | --- | --- |
| 1 | **Wrong section type.** Some sections were turned into the wrong kind of block: card sections became call-to-action sections, call-to-action sections became plain text, and some comparison tables or industry sections were mislabeled | The layout did not match the live site, even though the words were there | Compare the layout of every section, not just the text |
| 2 | **Content missing from the scrape.** Pages arrived without titles, descriptions, cards, buttons, lists, tables, FAQs, or testimonials that were on the live page | Thin, unfinished-looking pages | Do the parity check in Phase 4 on every page |
| 3 | **Half-copied cards.** Only the card titles were copied. Descriptions, icons, and images were missing | Cards with a heading and nothing else | Check every card for title, description, icon, and image |
| 4 | **Buttons that existed but were invisible.** Some buttons were never copied. Others were copied but missing the "enabled" setting, so they did not show on the page | Pages with no call to action, even though the data had one | Click every button on the new page. Never assume that "it is in the files" means "it is on screen" |
| 5 | **Broken comparison and pricing tables.** Missing headers, missing descriptions, missing buttons, or missing rows | Tables that looked complete but were not | Compare every table cell by cell against the live page |
| 6 | **Wrong or missing images.** Some sections showed the wrong picture, no picture, or an empty box | Visible, embarrassing gaps | Check every image is in the right section and has alt text |
| 7 | **Whole sections not detected.** Comparison matrices, process steps, timelines, and call-to-action blocks were missed by the scripts | Whole sections absent from the new page | Count the sections on the old page and the new page. The numbers must match |
| 8 | **Content grouped wrongly.** Content that belonged together, such as the benefits under a pricing or hiring model, was split into different sections | Page layout differed from the live site | Check that grouped content stays grouped |
| 9 | **Duplicate content.** Some sections were extracted more than once, or reused in different blocks | The same text appeared twice on one page | Search the page for repeated paragraphs. Ask an AI agent to flag repeated text |
| 10 | **Templates did not cover all page types.** The first version did not handle every HTML variation across Solutions, Services, Team Extension, Industries, and Case Studies pages | Pages of some types came out wrong | Group pages by type and test the template on several pages of each type |
| 11 | **Missing pages.** Some pages on the live site were not in the Astro project at all | A live page returned an error after launch | Compare your project's page list against the live sitemap |
| 12 | **Pages of the same type were built differently.** Slight differences in structure meant the scraper had to be updated to handle many layouts without being hard-coded for each one | A fix for one page broke another | Test each fix on pages of the same type, not only the one you fixed |
| 13 | **Repeated checking was needed.** After each template update, every generated page was reviewed against the live site to make sure nothing had slipped backwards | Time spent re-reviewing, but no regressions went live | Plan time for rechecking after every template change |
| 14 | **The goal: complete content parity.** No title, description, button, card, image, table, call to action, or FAQ left behind, while keeping the content compatible with the existing Astro components | A clear target everyone could check against | Write "parity" as the definition of done |

Part 13

## Frequently asked questions

**Will my rankings drop after moving to Astro?** Some movement is normal while search engines revisit your pages. Keeping the same URLs, content, titles, and links removes most avoidable risk. Nobody can promise unchanged rankings. If you see errors (404s, wrong canonicals, noindex), fix those first.

**Should I redesign and migrate at the same time?** If you can, no. Moving platforms first and changing the design later makes any problem easier to trace. If you must do both, keep a written list of every change.

Last note

## About this playbook

This playbook was written by EnactOn Technologies, a custom software development company founded in 2013. EnactOn migrated its own website from WordPress to Astro, and the problems in section 12 come from that project.

Your ticks are saved in this browser only. They are not shared with anyone else.