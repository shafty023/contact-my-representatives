# Contact My Representatives

A skill for Muse (Meta's personal AI assistant) that finds your U.S. and state elected officials from your exact home address, saves them, and then contacts the right ones for you whenever you raise a concern, deciding on its own whether the issue is state, federal, or both.

Works in any U.S. state. By Daniel Ochoa. Apache License 2.0.

## Install

Tell your Muse:

> Install the skill at https://raw.githubusercontent.com/shafty023/contact-my-representatives/main/SKILL.md as a custom skill named contact-my-representatives, save it so it triggers whenever I ask to contact my representatives, and then run its setup.

Or paste the contents of [SKILL.md](SKILL.md) into a Muse chat and ask Muse to save it as a skill and run the setup.

No Muse? [PROMPT.md](PROMPT.md) is the same workflow as a single paste-in prompt that works with any AI assistant.

## What it does

Setup, once:

- Finds your congressional and state legislative districts from your exact street address, using your state legislature's official lookup cross checked with the U.S. Census Geocoder. Never ZIP alone: one ZIP can span several districts, and ZIP level guessing picks the wrong representative.
- Records your U.S. Representative, both U.S. Senators, your state senator, your state representative, and your governor from official government sites only, with each official's contact form, required fields, and character limits.
- Captures your ZIP+4, because U.S. House email forms use it to confirm you are a constituent.
- Handles redistricting and elections properly: current and incoming officials are kept separate with the dates each applies, winners are verified only on official elections sources, and a stale file triggers re-verification of only the affected seats.

Every concern after that:

- Fast path: if your saved file is fresh, no new lookup happens. Muse goes straight to contacting.
- Verifies the facts first on the official record: the bill on congress.gov or your state legislature's site, the roll call at clerk.house.gov. It never drafts from a headline.
- Decides state, federal, or both from where the live bill actually sits, and checks whether one of your officials sits on the committee holding the measure.
- Submits a short message in your voice through the official form under a standing authorization you set at setup: telling Muse to contact an official and stating your position is the approval. You get the exact text and the confirmation back, and every contact is logged.
- If your concern targets members who are not your representatives, it says so, checks how your own representative voted, and redirects to the committee and leadership channels instead of sending submissions that constituency gates will reject.

## A worked example

[examples/hegseth-vote.md](examples/hegseth-vote.md) walks a real case end to end: a user upset that 11 Democrats missed the November 10, 2026 House vote on the Hegseth impeachment articles. The workflow corrected the premise (it was a referral vote, not an impeachment vote), ruled out the senators and every state official, refused the wasted submissions to non-representatives, and landed on exactly one contact: the user's own representative, who had voted to refer the articles and sits on the committee that now holds them.

## What it touches, in plain terms

- Reads official government sites only: house.gov, senate.gov, congress.gov, clerk.house.gov, the Census Geocoder, state legislature and state elections sites.
- Writes one officials file and a contact log to your Muse's memory, on your own account.
- Submits constituent contact forms only under your explicit standing authorization, using your own information and positions you stated. Your address, phone, and email go into official form fields and nowhere else.
- It never asks for a password or any credential. If a form needs something only you can provide, it asks for that one item and finishes.
- It never pretends a blocked form was sent. A blocked form returns the finished text, the official link, the official phone number, and a short call script.

## Files

- [SKILL.md](SKILL.md): the skill itself, the exact text Muse installs.
- [PROMPT.md](PROMPT.md): the same workflow as a portable prompt for any assistant.
- [examples/hegseth-vote.md](examples/hegseth-vote.md): a worked example on a real vote.
- [LICENSE](LICENSE): Apache License 2.0.

## Also listed

Submitted to the community directory at museskills.dev (submission issue: https://github.com/jongouveia/muse-skills/issues/50).

## Contributing

State lookup tools and legislature sites vary a lot. Issues and pull requests with per state notes, edge cases, and form quirks are welcome. Keep the rule: official government sources only, and nothing about a real person's address or contact details ever goes in this repo.
