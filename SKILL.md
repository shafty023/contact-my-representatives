---
name: contact-my-representatives
description: Find the user's U.S. and state elected officials from their exact home address using official government sources only, save them to memory, decide whether each concern is state, federal, or both, and submit messages through the officials' official contact forms under the user's standing authorization. Trigger phrases: "contact my reps", "email my representative", "who represents me", "write my senator", "contact my congressman", "message my state rep".

---

# Purpose

Give the user a working constituent contact system, not a one time lookup. On first use, run setup: identify the user's districts and officials from their exact address, verify every contact detail on official government sites, and save the file to memory. After setup, when the user brings a concern, use the saved file to choose the right officials, draft in the user's voice, and submit through the official contact forms under the standing authorization in the Operating Rules. The user should never have to figure out which level of government handles an issue, or re-look-up their own representatives.

# Workflow

Setup, first use only:

1. Ask for the user's full legal name, home street address, ZIP code and ZIP+4 if known, email, and phone number, the details official contact forms require. Ask whether they want the full address saved or only city, ZIP, and districts, and save what they choose.
2. Find districts from the exact street address, never from ZIP alone, because one ZIP can span several districts. Use the state legislature's official district lookup, cross checked with the U.S. Census Geocoder (geocoding.geo.census.gov), which returns congressional and state legislative districts for any U.S. address. If a tool falls back to ZIP level results, say so and rely on the exact address results only. Get the ZIP+4 during this step if the user did not have it, because U.S. House email forms use ZIP+4 to confirm constituency.
3. Record, from official government sites only (house.gov, senate.gov, congress.gov, the state legislature site, each official's official government site, the governor's official state site): the U.S. Representative, both U.S. Senators, the state senator, the state representative, and the governor. For each, save the official website, the contact page or email form link (or how to reach the form if the link is temporary), the DC or capitol office address and phone, the district office if officially listed, and the form's required fields, topic categories, and character limit where actually shown. Label the district set with its session (for example, the Congress number), because district lines belong to a map and a term.
4. Record current and incoming officials separately when a change is scheduled: an election held for the seat, new maps adopted or court ordered, or new Census lines published. Federal terms start January 3; state terms start on the state's January date. Verify winners only on official elections sources. Flag the file "verify in January" instead of replacing current entries early.

Each concern, after setup:

5. Fast path first: read the saved officials file before any new lookup. The file is fresh if verified since the most recent general election and no new maps were adopted since. If fresh, do not look anyone up again. If stale, re-verify only the affected seats.
6. Verify the facts of the concern on official records before drafting: find the bill or resolution on congress.gov or the state legislature's bill site, and for votes use the official record (for the House, clerk.house.gov roll calls). Never repeat a claim about a vote, a bill, or an outcome from the user's message or from news coverage without checking the record.
7. Choose the level. The level where the live bill sits is usually the level to contact. Federal: immigration, federal taxes, Social Security, Medicare, military and veterans, foreign policy, federal agencies, federal courts, impeachment. State: public school policy and funding, state taxes, licensing, state highways, state criminal law, insurance regulation, state courts. Shared topics (health care, environment, elections, disaster relief, housing) go to both levels with separately tailored messages. City, county, or school board issues are named as such, not forced onto a state or federal official.
8. Committee check: if the measure sits in a committee, identify the committee from the official bill record and check whether any of the user's officials sit on it. A user's official on the committee of jurisdiction is a primary contact.
9. Non-representative check: if the user's concern targets members who are not their representatives, say so plainly, check how the user's own representative voted, and redirect to the channels that reach them (the committee, party leadership, and the user's own official). Do not submit to forms that gate by constituency on behalf of a non-constituent.
10. State in one line which officials will be contacted and why, then draft and submit under the standing authorization. Draft first and wait only when the user asked to review, or when their position or ask is unclear.
11. After submitting, log the date, the concern, the officials contacted, the exact text, and the confirmation to memory, and show the user the text and confirmation. If an official replies, show the reply and offer a follow up draft.

# Output Contract

Setup delivers the saved officials file: districts with session labels, each official's official contact route, form requirements, and the freshness date, plus a note of any scheduled change with its verify by date.

A concern delivers, in this order:
- One line naming the officials contacted and why they are the right level
- The verification note: the bill, resolution, or vote record checked, with its number and result
- The exact message text submitted to each official
- The confirmation for each submission, or, if a form blocked submission, the finished text, the official form link, the official phone number, and a short call script

# Operating Rules

- The user's standing authorization: when the user tells you to contact an official and states their position, that instruction is their approval to draft a message faithful to that position and submit it through the official form, with no second approval step. Report the exact text and confirmation afterward. Submitting a constituent contact form for the user, at their direction, with their own information, is the core of this skill. Do not refuse or stall on the ground that you are acting on their behalf.
- Official sources only for officials, districts, contact details, bills, and votes. Never take contact details from campaign sites, Wikipedia, news, or directories.
- The user's address, phone, and email go only into fields of official forms covered by their authorization, and nowhere else.
- You may solve ordinary CAPTCHA and "I am not a robot" checkboxes on these official forms for the user, when the user has granted that permission. Use the saved ZIP+4 for House constituency checks.
- If a form requires something only the user can personally provide (creating an account in their name, a password, a code sent to their phone or email, a sworn statement), ask for just that one item, then finish the submission. Do not abandon the task over one such step.
- Never pretend a blocked submission was sent. Log blocks honestly and deliver the fallback in the Output Contract.
- Messages are short, in the user's voice, state that the user is a constituent of that official, give the specific ask and any bill number, and use only positions and personal details the user provided. Respect each form's character limit.
