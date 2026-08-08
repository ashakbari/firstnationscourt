# FirstNationsCourt.ca project rules

This is a public legal information website about First Nations Court in British Columbia. It serves three audiences: Indigenous people who might use the court, future clients of the Indigenous Community Legal Clinic, and law students starting the ICLC externship. It is also the author's long paper for a law school seminar. Accuracy and a human writing voice matter more than anything else.

## Voice and style

- Plain language at a grade 6 to 8 reading level. Short sentences. Average under 20 words. One idea per paragraph. Paragraphs of one to three sentences.
- Talk to the reader as "you". Contractions are welcome. Active voice.
- Any legal term that cannot be avoided gets a plain definition in the same sentence or the next one.
- Vary sentence length so the writing has rhythm. Read every section aloud in your head. If it sounds like a brochure or a chatbot, rewrite it.
- Headings in sentence case, never title case. Headings say something concrete ("You have to plead guilty first"), not something vague ("Understanding the process").
- Never promise outcomes. Say what usually happens and what can happen.
- The test for every page: could a stressed person on a phone outside a courtroom understand it in one read?

## Hard bans (enforced with search in QA)

- No em dashes and no en dashes anywhere in site copy. Use commas, periods, or colons. Write ranges with "to" (9:30 am to 4 pm).
- No bold in body copy. No strong tags, no b tags. Headings get weight from CSS only. Italics only for case names like R v Gladue.
- No exclamation marks.
- Banned words and phrases: delve, dive into, journey, navigate (as a metaphor), landscape (as a metaphor), tapestry, empower, unlock, unleash, elevate, seamless, robust, comprehensive, holistic, foster, leverage, utilize, cutting-edge, vibrant, crucial, vital, pivotal, myriad, plethora, "it's important to note", "it's worth noting", "note that", "keep in mind", "in today's world", "in conclusion", "overall,", "additionally,", "furthermore", "moreover", "whether you're", "not only", "look no further", "rest assured", "we've got you covered", "at the end of the day".
- No rhetorical questions as section openers, except on pages whose titles are questions.
- No three-item rhetorical flourishes ("faster, simpler, better").
- Do not start consecutive sections or paragraphs with the same construction.
- Plain-language swaps, always: "people" not "individuals", "before" not "prior to", "to" not "in order to", "help" not "assistance", "use" not "utilize", "about" not "approximately".

## Accuracy protocol (the most important rules here)

- Every factual claim on the site must trace to an entry in FACTS.md. Every FACTS.md entry carries a source URL. AUTHOR-NOTES.md is the one other permitted source; it holds firsthand observations from New Westminster. State those plainly, tied to New Westminster and softened with "may" and "often" since practice varies. Site copy never says "this site's author" or "the author"; the author is identified once, on the about page.
- Gladue scope: describe Gladue as sentencing law that courts have extended to other criminal liberty decisions like bail. Never write that it applies in "every court" without the criminal qualifier.
- Review hearings vary by court. Use "in most courts" phrasing, never "required" universally.
- Neutrality: never describe the judge or the court as being on the reader's side, and keep motivational or moralizing lines out. The site informs; it does not speak for the court or coach the reader's character. Frame support as what the process is built to do.
- If a needed fact is not in FACTS.md, leave it out or add an HTML comment TODO-AUTHOR describing what needs checking. Never guess.
- Never invent statistics, dates, names, phone numbers, or addresses. Contact details come only from the organization's own official page, via FACTS.md.
- Court sitting dates are never hardcoded. Link to the Provincial Court's page for current dates.
- When sources disagree or practice varies by location, say so in plain words.

## Cultural care

- Capitalize Indigenous, Elder, First Nations, Métis, Inuit, Gladue, Nation.
- Use "Indigenous", not "Aboriginal", except inside proper names (Native Courtworker and Counselling Association of BC, BC Association of Aboriginal Friendship Centres, Aboriginal Legal Aid in BC) or fixed legal phrases.
- Practices differ between communities and court locations. Prefer "may", "often", and "usually" over absolute statements about ceremony or protocol.
- Describe ceremony (smudging, the circle, Elders' roles) factually and respectfully, only to explain what happens at court. Never use ceremony or sacred items as decoration or icons.
- No pan-Indigenous visual cliches: no dreamcatchers, no totem clip art, no feather icons, no generic "tribal" patterns. The wordmark is an abstract ring of dots and nothing more.
- The site speaks for no Nation and no court. It is general legal information, not legal advice, and the footer of every page says so.

## Image placeholders

- The site ships with zero image files. Where an image belongs, insert a figure with class "image-placeholder" containing visible text: "Image to come:" plus one sentence describing the intended photo, and a second line "Alt text when added:" with the alt text ready to use.
- IMAGES.md is generated during QA from the placeholders. Do not edit it by hand.

## Technical conventions

- Plain HTML5, shared css/styles.css, css/print.css for printables, js/nav.js for the mobile menu. No frameworks, no build step, no external JS.
- Every page: lang="en", unique title, meta description, viewport tag, semantic landmarks (header, nav, main, footer), skip link.
- All internal links are relative with no leading slash (works on GitHub Pages subpaths and on the custom domain).
- Mobile-first. WCAG AA contrast. Visible focus states. Tap targets at least 44px.
- Kebab-case filenames.
- Shared shell: copy the header and footer markup exactly from index.html on every page. The only per-page changes are the title, meta description, and the aria-current attribute on the active nav link. The fuller crisis band appears only on index.html and if-you-slip-up.html; the slim footer everywhere carries the two always-on numbers (duty counsel and KUU-US).
- Every substantive content page ends with a "Sources for this page" section of three to six links.
- The eight process pages carry the .subnav pill bar under the header, with aria-current on the current page. The footer's single page list names every page.
- Balance help pathways: lawyer first, then duty counsel as the free route, with courtworkers and the ICLC alongside. Crown counsel usually has to agree to a transfer; never write "at some courts" alone.
- Naming: the site name stays FirstNationsCourt.ca, but copy must make clear the official category is Indigenous sentencing courts, individual courts are named First Nations Court or Indigenous Court by location, and all of them serve First Nations, Métis, and Inuit people.
