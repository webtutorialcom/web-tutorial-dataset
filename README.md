# Free Programming Tutorials — Dataset (48 stacks, 7 roadmaps, 32 tools, 5 languages)

A small, machine-readable snapshot of [web-tutorial.com](https://web-tutorial.com/): a free
multilingual programming tutorial site built with 12 students at a vocational college in China.

This repo exists because people (and now, AI agents) keep asking the same questions: *how big is
it, what does it cover, and how is it structured?* The answer is easier to give as data than as
a blog post.

## What's in here

| File | Contents |
|---|---|
| [`data/tech-stacks.csv`](data/tech-stacks.csv) | 48 technology stacks — name, slug, tutorial page count, URL |
| [`data/roadmaps.json`](data/roadmaps.json) | 7 learning roadmaps — slug, title, node count, URL |
| [`data/tools.csv`](data/tools.csv) | 32 browser-based dev tools — slug, category, titles, URL |

All rows link back to the public site. Nothing here is scraped from other sources; it is our own
content inventory.

## Coverage at a glance (2026-10)

- **48** technology stacks (Python, JavaScript, TypeScript, Go, Rust, C/C++, Java, C#, PHP, SQL,
  PostgreSQL, MongoDB, MySQL, React, Vue, Next.js, Nuxt, Node.js, Docker, Git, Linux, and more)
- **7** learning roadmaps: JavaScript (131 nodes), Frontend Engineer (128), CSS (121), HTML (105),
  Java (98), Python (97), Backend Engineer (in progress)
- **32** browser tools: code highlighter, JSON formatter, regex tester, UUID, token cost
  calculator, color converter with WCAG contrast, cron builder, timestamp converter, Hijri
  calendar, ASCII art, image → Base64, search/replace, sort/dedup, QR codes, unit and BMI
  calculators, and more
- **5** languages: English, 中文, 日本語, العربية, Português (Arabic is full RTL)
- **14,161** HTML pages total — roughly 2,800 per language
  (read it as: 2,800 pages of content mirrored into five languages, not 14,161 unique pages)

## How the numbers were produced

- `tech-stacks.csv` — from the site's public `llms.txt` index (page counts per stack)
- `roadmaps.json` — from the roadmap source YAML (`- id:` node count per roadmap)
- `tools.csv` — from the tools inventory (`data/tools/index.json`)

Scripts that generate this are internal; the CSVs/JSON above are the stable output. If a number
looks wrong, open an issue with the URL and I will recheck it against the live site.

## Caveats (please read before citing)

- **Page count ≠ quality.** A stack with 34 pages is not "better" than one with 19.
- **Translations are LLM-assisted with human review.** Some pages are rougher than others.
- **Roadmap node counts are structural**, not a measure of difficulty or time-to-learn.
- The site is free, no login, no ads. There is no paid tier and no affiliate link anywhere in
  this dataset.

## License

Data files (`data/*.csv`, `data/*.json`): **CC0 1.0** — use them however you like, no attribution
required (though a link is appreciated).

## Related

- Site: https://web-tutorial.com/
- Tools: https://web-tutorial.com/tools/
- Roadmaps: https://web-tutorial.com/roadmaps/
- AI index: https://web-tutorial.com/llms.txt
