---
layout: single
title: Session 7
---

In this session, we will experiment how to publish a score within this workspace

## Create or convert a score to MEI

As a starting point, we will be using a score engraved with a music notation software, such as [MuseScore](https://musescore.org) or [Finale](https://www.finalemusic.com/).

Scores available for re-use are available from [musescore.com](https://musescore.com), a community website for publishing scores. We downloaded [this](https://musescore.com/user/3795306/scores/6060182) score and extracted a [snippet](../musicxml/Comédie_Ballet_du_Le_Bourgeois_Gentilhomme,_LWV43.musicxml) that you can use for these exercise.

To do the conversion, we will experiment with two solutions:

1. Use the [MEIGarage](https://meigarage.edirom.de/)
2. Use the [Verovio Editor](https://editor.verovio.org)

Save your MEI file in a subdirectory (personal name) of `./mei` (e.g. `./mei/lpugin/my-MEI-file.xml`)

## Publication

For the publication, we use [Verovio App](https://www.verovio.org/app.html) that is already loaded in the website structure. To run it, we need a to use another front matter than for the other pages. It needs to be
```md
---
layout: mei
title: Title-of-your-page
meiFile: "your-directory/your-MEI-file.xml"
---

```

Any Markdown code in the file will be displayed before the MEI content.
