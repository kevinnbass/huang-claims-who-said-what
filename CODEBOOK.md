# Codebook: every statement on the spy claim and the three affair claims (fixed 2026-11-15 before any coder starts)

One row = one **statement**: one sentence (or one headline, subhead, caption, pull-quote or summary line) in one
document that bears on one claim below. A sentence that bears on two claims gets two rows. A sentence printed twice in
a document is filed once. The passage is copied exactly from the text (one sentence; never joined or trimmed mid-clause).

## `claim`
| value | a statement belongs here when it says, hedges, disputes or reports a denial of this |
|---|---|
| `SPY` | Alice Huang was a Chinese intelligence asset, source, agent or spy; gathered or passed information for Chinese intelligence or the Chinese government; was recruited by it or targeted Jensen Huang for it. Also: what any government concluded, believes, suspects or has not concluded about that; what evidence there is; what she obtained or passed; whether Jensen Huang knew. |
| `AFFAIR_AH` | Jensen Huang and Alice Huang had a romantic, sexual or intimate relationship, or an affair. A sentence that calls it only "close", "a relationship" or "ties" belongs here only if the same sentence or its paragraph makes clear a romantic one is meant; otherwise do not file it. |
| `AFFAIR_KP` | Jensen Huang had a romantic relationship or affair with Kimberly Powell, named or described ("an executive who reports to him", "a subordinate", "an employee") where the document identifies that person as Powell or is relaying the report about her. |
| `AFFAIR_E2` | He had a relationship or affair with another Nvidia employee, distinct from Powell ("a second employee", "another Nvidia employee", a third affair). |
| `AFFAIR_ANY` | He had an affair or was unfaithful, with no partner identified in the sentence and none clear from its paragraph (for example his own "I was unfaithful to my wife"; "his affairs"). If a sentence names or describes the partners, file one row per partner under the claims above instead. |

## `aspect`
For `SPY`: `is_spy` (she was or is one; she passed information) · `recruited` (recruited by, or working for, the
Ministry of State Security or Chinese intelligence; targeted him) · `us_judgment` (what U.S. agencies or officials
concluded, determined, believe, assess, doubt or have not concluded) · `other_govt` (what Singapore, Taiwan or another
government suspected or found) · `what_passed` (what she obtained or passed; whether secrets were compromised) ·
`huang_knew` (whether he knew or was warned) · `evidence` (the sentence describes the evidence itself: surveillance,
intercepts, the memo).
For the affair claims: `existence` (that it happened) · `admission` (that he or Nvidia admitted, acknowledged,
confirmed or denied it) · `detail` (when, where, how long; a video or photograph of it).
Choose the one aspect the sentence is mainly about.

## `stance`
`asserts` (says it is so, with no hedge) · `hedged` (suspected, alleged, believed, reportedly, said to be, accused of,
possible, "may") · `disputes` (says it is not so, or not established or proven) · `denial` (relays a denial by the
person or body concerned) · `declined` (someone declined to comment or did not respond, on this claim) · `question`
(poses it as an open question) · `context` (refers to the claim without saying whether it is so: "the spy allegations").

## Who says it
- `speaker_type`: `outlet_own_voice` (no source is named in the sentence and none clearly governs it in the paragraph) ·
  `unnamed_source` · `named_person` · `organization` (a company, agency, ministry, committee or spokesperson, on the
  record) · `document` (a memo, filing, intelligence report or court paper is described as saying it) · `other_outlet`.
- `speaker`: the name, or the description as the passage words it (at most 12 words): "people familiar with the memo",
  "Todd Blanche", "Nvidia's board", "The New York Times". For `outlet_own_voice` write the outlet's name.
- `speaker_role`: `us_intelligence` · `us_official` · `president_or_white_house` · `lawmaker` · `jensen_huang` ·
  `nvidia_company` · `nvidia_insider` (employees, people who worked there) · `alice_huang_or_megaspeed` ·
  `foreign_government` · `expert_or_former_official` · `investor_or_executive` · `outlet` · `other` · `not_stated`.

## What evidence the statement itself offers
- `evidence_kind` (the basis named in the sentence or in the attribution that governs it; if several, the strongest):
  `none_stated` · `intelligence_reporting` (intelligence, intelligence reports or assessments are said to show or
  conclude it) · `memo` · `intercepts` · `surveillance` · `investigation` (an FBI, Justice, Commerce or foreign inquiry
  is said to have found or suspected it) · `own_admission` (Jensen Huang's own words or acknowledgment) ·
  `company_statement` (Nvidia, its board, a spokesperson, a filing) · `official_on_record` (a named official's public
  statement) · `witness_accounts` (people said to have seen or known first-hand) · `video_or_photo` ·
  `documents_records` (corporate, court, travel or other records) · `other_outlet_report` · `circumstantial` (inferred
  from career, wealth, nationality, access or timing) · `other`.
- `evidence_seen`: `outlet_saw` (the outlet says it saw or holds the evidence) · `outlet_did_not_see` (it says it did
  not) · `described_by_source` (a source describes it) · `not_applicable`.

## How it is worded
- `key_words`: the verb or hedge that carries the claim, copied from the passage (at most 8 words): "was found to be",
  "determined", "believe", "suspected", "alleged", "acknowledged".
- `identifies_her` (for `SPY` and `AFFAIR_AH`; otherwise `not_applicable`): `named` (Alice Huang or Ms. Huang is in the
  sentence) · `described` ("a Chinese businesswoman", "the Megaspeed executive") · `not_in_sentence`.
- `note`: optional, at most 20 words (for example: "partner clause is the reporter's, beside Trump's quote").

The place of the passage in the document (headline, subhead, caption, first paragraph, body) is added by a script.

## Clarifications after the first audit (2026-11-15, 08:45 UTC; the values above are unchanged)
- **An agency said to conclude, with nobody quoted.** A sentence that says U.S. intelligence, an agency, "officials" or
  "the U.S." determined, concluded, found, believe or suspect something is not `outlet_own_voice`, even when no person
  is quoted: `speaker_type` is `unnamed_source`, `speaker` is the body as worded, `speaker_role` is `us_intelligence` or
  `us_official`, and `evidence_kind` is `intelligence_reporting` (or the basis named). `outlet_own_voice` is for a
  sentence that asserts the claim itself with no such attribution ("a Chinese spy" as a bare description).
- **Whose words.** A statement is credited to Jensen Huang or Nvidia (`speaker_role`) only where the document presents
  it as what he or the company said, admitted, confirmed or denied. Where a named person's words are about something
  else and the affair or the spying sits in the reporter's own clause beside them, the speaker is the outlet.
- **`AFFAIR_ANY`** is judged on the sentence and its own paragraph only; a partner named in another paragraph does not
  make it `AFFAIR_AH`.

## One rule added after coding (2026-11-16)
- **Another article's headline is not a statement of this document.** A saved page shows more than its article: lists
  of the site's related, recommended, trending or most-read stories, a line such as "RELATED:", "Also read" or "Read
  more" followed by a headline, a teaser or promo for another piece, the entries of a reference list. A headline of, or
  a link or teaser to, a different article is not filed for the page that shows it. A headline, deck, subheading,
  caption, pull quote, bullet or list item of the article itself is filed as before. Why: such lists are filled in
  after publication, so a page of Oct 29 can show a headline of Nov 8, and the table would date that claim to Oct 29.
  The rule was applied to the statements already filed: a reader looked at every statement picked by form (short and
  without a full stop, or equal to another saved page's title, or opening with a list number), and the referee ruled
  on each one that reader called another article's headline.
  The same holds for readers' comments printed under an article: they are not statements of the document (added the
  same day, after a reading of every first-day statement found four of them filed).
