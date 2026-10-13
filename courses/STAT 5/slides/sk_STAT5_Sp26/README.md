# STAT 5 discussion slides — Spring 2026

These are nine discussion-section decks developed by Sho Kawano for STAT 5 at the University of California, Santa Cruz in Spring 2026. Yunan Wang was the course instructor.

The decks cover data collection and summaries, probability, normal distributions, sampling distributions, confidence intervals, and hypothesis testing. They are intended as adaptable teaching materials, not as a fixed course sequence: revise examples, schedule, logistics, assessment prompts, and worksheet directions for your own offering.

## Contents

- `slides/section1.qmd` through `slides/section9.qmd`: editable Quarto RevealJS sources
- `slides/custom.scss`: shared dark-theme styling
- `slides/section2_img/`, `slides/heights.png`, and `slides/slide6.png`: instructional figures required by the sources

The package deliberately excludes rendered PDFs and HTML dependencies, lecture files, attendance QR codes, and student/course links. The included photographs were taken by Sho Kawano on his iPhone. TAs are encouraged to choose their own images when adapting the decks. The introductory, bio, cover, and graduate-school photographs are excluded.

## Requirements and rendering

Install [Quarto](https://quarto.org/) and R with `ggplot2`. Render a deck from within `slides/` with:

```sh
quarto render section5.qmd
```

This produces RevealJS HTML. To make a PDF, run a local Quarto preview and export the deck with [DeckTape](https://github.com/astefanutti/decktape), for example:

```sh
quarto preview section5.qmd --port 4321
decktape reveal http://localhost:4321 section5.pdf
```

Review the generated deck before use, especially any slides marked for local adaptation.

## Attribution

Created by Sho Kawano. Please retain attribution when reusing or adapting these materials.
