# Follow a claim: how the Jensen Huang and Alice Huang claims were stated, by whom, and on what

Open `index.html` (in the repository, the link in the About box opens it as a page). Pick one of the five claims and
see who stated it on which day, how (flatly, with a hedge, disputed or denied), who the statement is put to, what
evidence the sentence offers, which outlets stated it first, and which credit which.

**What is counted.** 12,339 statements in 1,115 of 1,171 documents dated Oct 29 to Nov 14, 2026: 153 pages of the
New York Times, the Wall Street Journal, the Financial Times and the Economist; 995 articles and pages of 334 other
outlets and sites; 23 statements and transcripts of the people and bodies themselves. A statement is one sentence,
headline or caption bearing on one claim: that Alice Huang was a Chinese intelligence asset or spy (7,333); that
Jensen Huang had an affair with her (2,537), with Kimberly Powell (863), with a second Nvidia employee
(13), or an affair with no partner named (1,593). Counts are statements, not sources: one source quoted in ten
sentences is ten statements. `CODEBOOK.md` defines every field.

**How it was coded.** By automated readers working alone from the codebook, which was fixed before coding but for
clarifications after the first audit and one rule added on Nov 16 and applied to everything already coded: a headline
of another article that a page shows (most-read and related lists, reference lists) is not a statement of that page. Two coded
every document independently (6,181 statements stand on their agreement); a third ruled where they differed or only
one had filed (4,986); a fourth checked statements against their documents and re-read documents for missed
statements; a fifth, the referee, ruled on what the fourth contested and proposed (1,172 statements changed or added
that way). A script confirms that every coded sentence is in the saved text of its document. No person has checked the
coding line by line.
- Statements the fourth reader checked: 12689 of 12689; documents it re-read: 1171 of 1171.
- Fields it contested: 2431 on 1637 statements; the referee: for the fourth reader 2231; for the table as it stood 158; for a third value 42.
- Statements the re-reads proposed to add: 500; the referee kept 290.

**What this copy leaves out.** Sentences from news articles are not reproduced. For each of the 12,223 statements taken
from an article the table gives only the words that carry the claim (at most eight), who the sentence says is speaking
(cut to eight words where the article's description runs longer), the headline, and a link where the saved page records
one. A sentence coded under two claims is two statements, each with its own words. Counted per article, the words
shown come to about 3% of the article's text at the median and 20% at most (a page of 796 characters), at about six
characters a word. The 116 statements from documents issued by the speakers themselves (company, government and
officials' texts) are quoted whole.

**Limits.**
- Coverage is not a census of the press. The four papers are covered as far as their pages could be saved (some of
  their pages are read from republished copies); the other outlets are those found mostly through two news
  aggregators and fetched from sites that allow automated access.
- A document's day is the day it was first published, where its page shows one. The text read is the copy saved, which
  may be a later version: a sentence can be newer than that day. Where the saved text itself reports, as having
  happened, a dated event later than that day (the Financial Times's report of Nov 6, Huang's message of Nov 8, the
  President's remarks of Nov 9, the Times's report of a second affair on Nov 11, the resignation of Nov 12), the
  document stands on that event's day: 20 documents here. That can make an outlet look later than it was, never
  earlier. A page changed in other ways is not caught: 61 more documents here say, in their own data, that they
  were modified on a later day than the day they stand on. They are not moved for that alone (most changes are small,
  and a first report would be put behind the pages that cite it); the page marks them. A time of first publication is
  known for only some pages, and a rewritten page can keep an old one.
- A saved page shows headlines of the site's other stories (most read, related, reference lists). Those are not counted
  as the page's statements: 1,251 statements that could be such a line by their form (short or without a full stop, equal to another page's title, or opening with a list number)
  were read one by one in their documents; a reader called 600 another article's headline and the referee removed 600. One that does not look like a headline by its form may remain.
- "Evidence offered" is what the sentence, or the attribution that governs it, names as its basis. It is not a finding
  about what the outlet holds, and a claim put to unnamed people is not thereby false.
- The credited outlet in "who credits whom" is read from the words of the sentence by a fixed list of names.
- Videos and podcasts were not transcribed.
