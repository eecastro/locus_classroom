# Locus of Control: An In-Class Activity for Intro Psych

A single-page web activity that lets students take a college-adapted version of Rotter's Internal–External Locus of Control Scale. Students then see their score next to national benchmarks for US college students, along with discussion of what the construct means across cultures and decades.

It was built for in-class use in an introductory psychology course and runs entirely in the browser. No data is collected, stored, or sent anywhere.

## About the instrument

Locus of control is a generalized expectancy about whether outcomes in one's life depend on one's own behavior (internal) or on luck, fate, timing, or powerful others (external). Julian Rotter introduced the construct within social learning theory. He published the Internal–External (I-E) Scale in 1966. That scale has 29 forced-choice pairs: 23 are scored and 6 are fillers that disguise the scale's purpose. Scores run from 0 (most internal) to 23 (most external).

**This page does not reproduce Rotter's original items.** The statements are new wording written for current college students, about exams, group projects, internships, roommates, and campus politics. The adaptation keeps the original's structure and scoring logic:

- 23 scored pairs and 6 fillers, with the fillers placed in roughly the original positions
- the external option sometimes listed first and sometimes second
- one point for each external choice

The adapted wording has not been validated. Use the page for classroom demonstration and discussion, not for research or clinical assessment.

## What students see

After completing the 29 items, students get:

- **Their score.** It's shown on a 0–23 line alongside the US college student averages for 1960 (8.70) and 2002 (11.96).
- **Estimated percentiles.** These are relative to both cohorts. They assume a normal distribution with SD ≈ 4.1, derived from the reported 0.80 SD shift.
- **A breakdown by life area.** Areas are school, work, relationships, luck and life direction, and politics and society. It's descriptive only and not a validated subscale.
- **Interpretation.** It explains research correlates, the costs of both extremes, historical change, and cross-cultural cautions.
- **Extras.** An item-by-item review of their answers, six discussion questions, and a print/save-as-PDF option.

## Attribution

Instrument structure and construct:

> Rotter, J. B. (1966). Generalized expectancies for internal versus external control of reinforcement. *Psychological Monographs: General and Applied, 80*(1), 1–28. https://doi.org/10.1037/h0092976

National comparison data:

> Twenge, J. M., Zhang, L., & Im, C. (2004). It's beyond my control: A cross-temporal meta-analysis of increasing externality in locus of control, 1960–2002. *Personality and Social Psychology Review, 8*(3), 308–319. https://doi.org/10.1207/s15327957pspr0803_5

Other sources cited on the results page:

- Benassi, V. A., Sweeney, P. D., & Dufour, C. L. (1988). *Journal of Abnormal Psychology, 97*, 357–367.
- Findley, M. J., & Cooper, H. M. (1983). *Journal of Personality and Social Psychology, 44*, 419–427.
- Ng, T. W. H., Sorensen, K. L., & Eby, L. T. (2006). *Journal of Organizational Behavior, 27*, 1057–1087.
- Smith, P. B., Trompenaars, F., & Dugan, S. (1995). *International Journal of Psychology, 30*(3), 377–400.
- Wang, X., & Xin, Z. (2023). *Journal of Pacific Rim Psychology, 17*.

The adapted item wording, page design, and code are original to this project. If you reuse them, please credit this repository and keep the citations above.

## Using this page in your own course

### Host your own copy

1. Fork this repository, or download `index.html` and add it to a new public repository.
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save.
4. After a minute or two, your page will be live at `https://<your-username>.github.io/<repository-name>/`.

The page is a single self-contained file. Apart from Google Fonts, which have system fallbacks, it doesn't load any external libraries, and it needs no build step.

### Customize it

Everything you're likely to change is in `index.html`:

| To change | Look for |
|---|---|
| Course name in the header | `<div class="course">` |
| Item wording | the `ITEMS` array in the script. Each item has `a`, `b`, `ext` (`"a"`, `"b"`, or `null` for fillers), and `d` (life area) |
| Benchmark means and SD | the `NORMS` object |
| Score band descriptions | the `bandFor()` function |
| Discussion questions | `<ol class="discuss">` |

If you have licensed access to Rotter's original items and want to use them instead, replace the text in `ITEMS` and set each `ext` value to match Rotter's scoring key. Keep the six filler items marked `ext: null`.

### Running it in class

- Students can complete it on phones in about 5–7 minutes.
- Because nothing is collected, gather class data by having students report their score anonymously, for example through a poll or a show of hands by score band. Comparing the class mean with the 1960 and 2002 averages makes a strong opening for discussion.
- The page pairs well with lessons on social learning theory, attribution, learned helplessness, cross-cultural psychology, and the limits of self-report and forced-choice formats.

## Limitations

- The adapted items have not been validated against the original scale, so the comparisons to national norms are approximate.
- The percentile estimates rely on a normal approximation and an estimated SD.
- The benchmark data covers US college students only, and the most recent year is 2002.
- The life-area breakdown uses 4–5 items per area and is not a reliable subscale.

## License

Add the license of your choice here (for example, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) for the content and [MIT](https://opensource.org/licenses/MIT) for the code). Without a license file, others can view the page but have no clear permission to reuse it.
