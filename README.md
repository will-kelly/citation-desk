# Citation Desk

A Claude Project that finds every claim in your draft that needs a source, verifies the source for real, and tells you exactly where to place the link. Built for writers who check the source instead of trusting the autocomplete.

Rename it to **Receipts** if you want the bite.

## The problem

AI-assisted drafts have two citation failures, and most tools only catch the easy one. The easy one is a bare statistic with no source. The hard one is a sentence that reproduces a source's framing the author never read, which is plagiarism even when nobody intended it. Worse, plenty of tools will hand you a confident URL that does not actually support the claim you made. Citation Desk is built to catch both failures and to never invent a source.

## What it does

- Finds every claim that needs a citation: statistics, findings, attributed claims, quotes, and distinctive framings borrowed from an identifiable author.
- Verifies that the source supports the specific claim, matching the exact number or finding to the page rather than the topic.
- Flags drift when your figure and the source disagree, and reports both numbers.
- Catches close paraphrase by searching distinctive phrasing against published sources.
- Refuses to invent a URL. When no credible source exists, it tells you to cut or soften the claim instead of propping it up.
- Returns the exact anchor text to hyperlink and a copy-ready sentence with the link in place.
- Optionally returns your draft as a .docx with the verified links already inserted inline.

## How it works

It runs the draft through three passes.

1. **Inventory.** It reads the whole draft and lists every claim that needs a source, grouped by type, so you see the scope before any research happens.
2. **Verify.** It searches for each source, opens the page, and confirms it supports the specific claim. It prefers primary sources: the originating company, the agency, the peer-reviewed paper, the filing, or the analyst firm itself.
3. **Close-paraphrase check.** For findings and distinctive framings, it searches the phrasing to see whether it tracks an existing source, and flags anything too close to either quote and cite or rewrite.

It returns a report with a status on every claim (verified, drift, unverifiable, or paraphrase risk), the verified link, the anchor words, and a placement-ready sentence. When file creation is enabled, it also inserts the verified links into a copy of your .docx with the formatting preserved.

## What's in this repo

```
.
├── README.md
├── citation-desk-instructions.md      paste into the project instructions field
├── citation-desk-voice-standards.md   knowledge upload, keeps rewrites in voice
├── citation-desk-common-knowledge.md  knowledge upload, prevents over-flagging
└── citation-desk-project.md           design spec and reference, do not upload
```

## Setup

1. In Settings > Capabilities, turn on Code execution and file creation so the project can build the .docx, and confirm web search is on, since verification depends on it.
2. Create a new project in Claude and name it Citation Desk.
3. Paste the contents of `citation-desk-instructions.md` into the project instructions.
4. Upload `citation-desk-voice-standards.md` and `citation-desk-common-knowledge.md` as project knowledge. Do not upload the spec.
5. Start a chat in the project, paste a draft or upload a .docx, and say "audit this for citations."

## Usage

Paste a draft or upload a .docx and ask it to audit for citations. You get the gap inventory first, then the full report. Each verified claim comes back with its link, the exact anchor words, and a sentence you can paste whole. With file creation on, you also get the hyperlinked .docx.

Placement reaches the page three ways. The linked .docx arrives done. The rendered markdown line drops into a blog or Substack draft. The anchor words plus the URL work anywhere else, including the LinkedIn workaround of putting the source in a first comment, since LinkedIn does not support inline links in the post body.

## Design principles

- Verification is the product. A citation is only real once the source has been opened and confirmed.
- Never invent a source. Missing evidence is reported as missing, not papered over with a weak link.
- Auto-link only what is verified. Drift, unverifiable, and paraphrase-risk claims stay in the report for a human decision, because auto-linking a wrong figure is the exact failure this tool exists to catch.
- Preserve the author's argument. Voice fixes never water down a deliberate point.

## What it is not

It is not a corpus-based plagiarism scanner running against a private database. It is a reasoning-based auditor that uses live web search to verify sources and catch close paraphrase. Treat its output as a strong first pass, not a guarantee, and confirm the calls that matter.

## Requirements

- A Claude account with Projects.
- Web search enabled, for source verification.
- Code execution and file creation enabled, for the hyperlinked .docx output. Without it, you still get the full report and the copy-ready lines.

## Author

Will Kelly, technical content strategist focused on AI enablement.
Writing at willkelly.substack.com and willkelly.medium.com.

## License

Add your license of choice.
