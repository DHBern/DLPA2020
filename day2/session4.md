---
layout: single
title: Session 4
---

In this session, we will experiment with MEI encoding

## MEI Tutorials

As a starting point, try to fulfil some of the MEI tutorials available on the MEI website:

* [A 5-minute Quickstart tutorial for MEI](https://music-encoding.org/tutorials/101-quickstart.html)
* [Learn how to encode rests](https://music-encoding.org/tutorials/104-rests.html)
* [A short tutorial about chords](https://music-encoding.org/tutorials/103-chords.html)

## Use the Verovio Editor for direct interactive encoding

Encode the first bar of the first staff from the following excerpt (KV 425 in [NMA](https://dme.mozarteum.at/DME/nma/)):

![image](https://user-images.githubusercontent.com/689412/57692051-4e450080-7635-11e9-9e9b-0dfa44d88803.png)

Start with [this file](https://editor.verovio.org/?file=https://dhbern.github.io/DLPA2020/mei/single-note.mei) (you can right-click and open in a new tab)

### First staff

1. Add a system bracket with `staffGrp@symbol="bracket"`

2. Add the instrument label with:

```xml
<staffDef>
  <label>Oboe I, II</label>
</staffDef>
```

3. Add the time signature with `scoreDef@meter.count="3"` and `scoreDef@meter.unit="4"`

4. Add the tempo with, in `<measure>`:

```xml
<tempo>Adagio</tempo>
```

5. Place the tempo indication `tempo@tstamp="1"` and `staff="1"` (not necessary with a staff)

See [time stamps in guidelines](https://music-encoding.org/guidelines/v4/content/cmn.html#cmnTstamp)

6. Add forte with `<dynam>`

See [dynam in guidelines](https://music-encoding.org/guidelines/v4/content/shared.html#sharedExpressionMarks)

7. Add beam and notes with:

```xml
<beam>
  <note/>
  <rest/>
  <note/>
</beam>
```

8. Enter second voice with `<layer>` and `layer@n="2"`.

### Second staff

1. Add the second staff (definition) with `<staffDef>` and `staffDef@n="2"`.

2. Add the second staff (content) with `<staff>` and `staff@n="2"`.

3. "a 2" indication with `<dir>`

4. Italic Text witn `<rend>` and `rend@?`

See [Text rendition in guidelines](https://music-encoding.org/guidelines/v4/content/lyricsperfdir.html#sharedTextRendition)

5. Add forte by modifying `<dynam>` as `dynam@n="1 2"`

**Is this solution representative in terms of content?**

See [Guidelines](https://music-encoding.org/guidelines/v4/content/analysisharm.html#analysisDescribingRelationships)


### Third staff

1. Add the third staff with `<staffDef>`/`<staff>` and `@n="3"`

2. Add the notes with:

```xml
<beam>
  <chord>
    <note/>
    <note/>
  </chord>
  <rest/>
  <chord>
    <note/>
    <note/>
  </chord>
</beam>
```

**Is this solution representative in terms of content?**

See [MEI GitHub repository](https://github.com/music-encoding/music-encoding/search?q=stem.sameas&type=Issues)
