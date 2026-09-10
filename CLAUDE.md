# english-teens

Homework pages for a small online English group: three teenage girls, level A2/A2+. The site is published with GitHub Pages from the `main` branch root, so every `*.html` file here is live at
https://zhvictoria998-web.github.io/english-teens/<file>.html as soon as it is pushed.

## Files

- `index.html` - Homework 1 (present simple vs past simple, back-to-school words). Use it as the template for every new homework.
- `homework2.html`, `homework3.html`, ... - later homeworks. One self-contained file each, no external scripts.

## How to make a new homework

1. Copy the structure of `index.html`: same CSS, same word bank block, same exercise sections, same summary block with "Copy my results for the teacher" and save/load progress. Change only the title, the subtitle line, the word bank and the exercises.
2. Keep the page self-contained: inline CSS and JS, inline SVG icons, no CDN scripts. Google Fonts are optional and must have fallbacks. The students are in Russia and open the page on phones, so it must work offline after loading and on a narrow screen.
3. Exercise types already supported by the script: picture -> phrase inputs (`.piccard`), gap-fill inputs (`.ans.gap` with `data-key` as a JSON array of accepted answers), word-order chips (`.order` with `data-answer`), free writing with automatic checks (`#blog` + `#checks`). Reuse them instead of inventing new ones.
4. Answers are checked client-side with `norm()`: lowercase, trailing punctuation stripped, contractions expanded/normalised. Put every reasonable spelling into `data-key`.
5. Change the localStorage prefix (`hw1.` in index.html) to `hw2.`, `hw3.`, ... so homeworks do not overwrite each other's saved progress. Update the `EX_TITLES` map and the "N of 7 exercises" counter to match the new exercise count.
6. Language: British English, simple instructions a 13-15-year-old A2 learner can follow without a dictionary.
7. Commit with a message like `Add Homework 2 (homework2.html)` and push to `main`. Then report the live URL.
