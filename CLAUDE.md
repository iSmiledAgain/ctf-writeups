# ctf-writeups — repo conventions

Writeups for CTFs played with team **SudoWin**. Handle: `ISmiledAgain` (in-CTF: `iSmiled`).

## Layout

```
<year>/<EventName>/
├── README.md                  # event index — table of all challenges
└── <Challenge_Name>/
    ├── README.md              # the writeup
    └── assets/                # every image for this challenge
        ├── <slug>_desc.png    # challenge description screenshot
        ├── <slug>_flag.png    # solved/submissions screenshot
        └── <provided files>   # images the challenge gave us
```

Rules:
- Every challenge folder is self-contained. Images live in that challenge's own `assets/`, never in a shared top-level folder.
- Image links in a README are **relative**: `./assets/foo.png`. Never absolute, never `../`.
- Event folder name matches how the CTF brands itself (`UTCTF`, `DawgCTF`).
- Challenge folder name: `Title_Case_With_Underscores`.
  - Note: `2025/UTCTF/` predates this and uses `lowercase-hyphens` with a bare `image.png`. Leave it alone unless I ask for a migration — don't "fix" it opportunistically.

## Writeup README format

Sections in this order, `##` level:

1. Title (`#`) + metadata block — category, points, solves
2. `## Challenge` — description screenshot, then the prompt text if useful
3. `## Challenge Image` — the file(s) the challenge provided (omit if none)
4. `## Solution` — bolded `**Step N — <what>.**` headers, prose underneath
5. `## Flag` — solved screenshot, then the flag in a fenced block

Metadata block:

```
**Category:** OSINT
**Points:** 400
**Solves:** 43
```

## Event index README

Table with columns: Challenge (linked to its folder README) | Category | Points | Solved. Ordered by points ascending. Header above it gives team and CTF name.

## Writing style

- Technical peer audience. Assume crypto, Linux, and security tooling fundamentals — don't explain what EXIF or ADS-B is.
- Lead with the actual insight that cracked it, not a narrative of everything tried.
- Include real commands (`exiftool foo.jpg`) in fenced blocks.
- No filler, no "in this challenge we will…".
- If I say I don't remember how I solved something, reconstruct a plausible method but **flag clearly in your reply which parts are reconstructed** so I can correct them. Don't present a guess as fact in the writeup.

## Before finishing any change

- Every `![](...)` path in every touched README resolves to a file that exists.
- Event index table includes any newly added challenge.
- Use `git mv` when relocating tracked files.
- Show me the diff. Don't `git push` — I do that myself.

## Commits

- Author is me alone. Do not add `Co-Authored-By:` trailers or "Generated with Claude Code" lines.
- Message style: short imperative, lowercase, e.g. `add DawgCTF 2026 writeups`, `fix image paths in plane spotting`.
