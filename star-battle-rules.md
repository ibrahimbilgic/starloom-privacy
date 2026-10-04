---
title: "Star Battle puzzle rules and solving techniques"
description: "How to play Star Battle: one star per row, column and region, and no two stars touching. Six solving techniques, with a 5x5 puzzle solved step by step."
---
<style>
.sb{border-collapse:collapse;margin:.5rem 0 1rem}
.sb td{width:2.6rem;height:2.6rem;text-align:center;font-size:1.15rem;border:1px solid #fff;color:#222}
.sb .r0{background:#cfd8ff}.sb .r1{background:#ffd6a5}.sb .r2{background:#c6f0c2}.sb .r3{background:#f7c6e8}.sb .r4{background:#fff3a6}
.techs dt{font-weight:700;margin-top:1rem}.techs dd{margin:.2rem 0 0 0}
.box{border-left:4px solid #6a5acd;padding:.1rem 1rem;margin:1rem 0;background:#f4f2ff}
</style>
<script type="application/ld+json">
{"@context":"https://schema.org","@type":"FAQPage","mainEntity":[
{"@type":"Question","name":"What are the rules of Star Battle?","acceptedAnswer":{"@type":"Answer","text":"Place stars on a square grid that is divided into coloured regions. Every row, every column and every region must contain exactly one star (two in the harder two-star variant), and no two stars may touch, not even diagonally."}},
{"@type":"Question","name":"Can Star Battle be solved without guessing?","acceptedAnswer":{"@type":"Answer","text":"Yes. A well-made puzzle has one solution that logic can reach: single-candidate cells, regions confined to one row or column, and counting rows against regions."}},
{"@type":"Question","name":"Where do I start a Star Battle puzzle?","acceptedAnswer":{"@type":"Answer","text":"Look for the smallest region. A region of one cell is a star immediately, and a region that fits inside one row or column tells you the rest of that line is empty."}}
]}
</script>

# Star Battle: the rules and how to solve it

Star Battle is a logic puzzle played on a square grid cut into coloured regions. You never need to guess. Here is what the rules are, the techniques that solve it, and one puzzle worked through from the first star to the last.

## The rules

1. Put stars in the grid so that **every row** has exactly one.
2. **Every column** has exactly one.
3. **Every coloured region** has exactly one.
4. **No two stars touch**, including diagonally. The eight cells around a star are always empty.

Harder variants use two stars per row, column and region; the idea is the same. A grid with N rows has N regions and N stars.

## Six techniques, easiest first

<dl class="techs">
<dt>1. A star clears its surroundings</dt>
<dd>Once a star is placed, mark every cell around it, and the rest of its row, column and region, as empty. Every other technique feeds on these crosses.</dd>
<dt>2. The last open cell</dt>
<dd>If a row, column or region has only one open cell left, the star goes there. A region that was drawn as a single cell is the first example: it is a star from the start.</dd>
<dt>3. Confinement</dt>
<dd>If every open cell of a region sits in one row, that region's star is in that row, so the other cells of the row, outside the region, are empty. It works the other way round too: if every open cell of a row belongs to one region, the rest of the region is empty. The same goes for columns.</dd>
<dt>4. Pigeonhole</dt>
<dd>If two regions fit entirely inside the same two rows, those two rows' stars are spoken for, and every other cell in those rows is empty. Three regions in three rows, and so on. The reverse works for rows that reach only a few regions, and for columns.</dd>
<dt>5. "What if I put a star here?"</dt>
<dd>If a star in a cell would leave some row, column or region with nowhere to put its own star, the cell is empty. You do not follow a long chain; you check one step and see whether something is left with no room.</dd>
<dt>6. The 2&times;2 block</dt>
<dd>Any 2&times;2 square can hold at most one star, because two would touch. When an area needs its last star and all its candidates sit in one 2&times;2 square, you know that square holds the star, and everything outside it is empty.</dd>
</dl>

<div class="box" markdown="1">
**Where to start:** scan for the smallest regions first, then for any region that lies entirely in one or two rows or columns. Large regions are the last to give up their star.
</div>

## A 5&times;5 puzzle, solved

Five regions, one star each. Coloured areas are regions; there are no numbers or other clues.

<table class="sb" aria-label="5 by 5 Star Battle grid"><tr><td class="r0"></td><td class="r0"></td><td class="r0"></td><td class="r0"></td><td class="r0"></td></tr><tr><td class="r0"></td><td class="r0"></td><td class="r0"></td><td class="r0"></td><td class="r1"></td></tr><tr><td class="r2"></td><td class="r3"></td><td class="r0"></td><td class="r4"></td><td class="r4"></td></tr><tr><td class="r2"></td><td class="r2"></td><td class="r4"></td><td class="r4"></td><td class="r4"></td></tr><tr><td class="r2"></td><td class="r2"></td><td class="r2"></td><td class="r2"></td><td class="r2"></td></tr></table>

**Step 1: single-cell regions.** The pink cell in the third row and the orange cell at the end of the second row are regions by themselves, so both are stars. Their rows, columns and eight neighbours are crossed out.

<table class="sb" aria-label="5 by 5 Star Battle grid"><tr><td class="r0"></td><td class="r0">&times;</td><td class="r0"></td><td class="r0">&times;</td><td class="r0">&times;</td></tr><tr><td class="r0">&times;</td><td class="r0">&times;</td><td class="r0">&times;</td><td class="r0">&times;</td><td class="r1">&#9733;</td></tr><tr><td class="r2">&times;</td><td class="r3">&#9733;</td><td class="r0">&times;</td><td class="r4">&times;</td><td class="r4">&times;</td></tr><tr><td class="r2">&times;</td><td class="r2">&times;</td><td class="r4">&times;</td><td class="r4"></td><td class="r4">&times;</td></tr><tr><td class="r2"></td><td class="r2">&times;</td><td class="r2"></td><td class="r2"></td><td class="r2">&times;</td></tr></table>

**Step 2: the yellow region.** Of its five cells, the crosses have removed four. The one left, in row 4, column 4, must be its star.

**Step 3: the green region.** Rows, columns and neighbours now leave only the bottom-left cell open. It is the star.

<table class="sb" aria-label="5 by 5 Star Battle grid"><tr><td class="r0"></td><td class="r0">&times;</td><td class="r0"></td><td class="r0">&times;</td><td class="r0">&times;</td></tr><tr><td class="r0">&times;</td><td class="r0">&times;</td><td class="r0">&times;</td><td class="r0">&times;</td><td class="r1">&#9733;</td></tr><tr><td class="r2">&times;</td><td class="r3">&#9733;</td><td class="r0">&times;</td><td class="r4">&times;</td><td class="r4">&times;</td></tr><tr><td class="r2">&times;</td><td class="r2">&times;</td><td class="r4">&times;</td><td class="r4">&#9733;</td><td class="r4">&times;</td></tr><tr><td class="r2"></td><td class="r2">&times;</td><td class="r2">&times;</td><td class="r2">&times;</td><td class="r2">&times;</td></tr></table>

**Step 4: the blue region.** The only open cell is at the top of the third column. Five stars, one in each row, column and region, none touching:

<table class="sb" aria-label="5 by 5 Star Battle grid"><tr><td class="r0"></td><td class="r0"></td><td class="r0">&#9733;</td><td class="r0"></td><td class="r0"></td></tr><tr><td class="r0"></td><td class="r0"></td><td class="r0"></td><td class="r0"></td><td class="r1">&#9733;</td></tr><tr><td class="r2"></td><td class="r3">&#9733;</td><td class="r0"></td><td class="r4"></td><td class="r4"></td></tr><tr><td class="r2"></td><td class="r2"></td><td class="r4"></td><td class="r4">&#9733;</td><td class="r4"></td></tr><tr><td class="r2">&#9733;</td><td class="r2"></td><td class="r2"></td><td class="r2"></td><td class="r2"></td></tr></table>

Every move above followed from the rules; none needed a guess.

## When you get stuck

- Re-check the crosses. A missing cross around a star is the most common reason for a "stuck" grid.
- Count regions against rows: if two regions are squeezed into two rows, use technique 4.
- Pick an empty cell and test it in your head with technique 5. Disproving a star in a cell is as good as placing one.

## Starloom

Starloom is a Star Battle game for phones with 300 levels on grids from 5&times;5 to 10&times;10, plus a daily puzzle. Its hint button explains which of the techniques above applies instead of just showing a cell. The app is free with ads on Android and iOS; this puzzle is level 1.
[Get it on Google Play](https://play.google.com/store/apps/details?id=com.appfellas.starloom&referrer=utm_source%3Dweb%26utm_medium%3Drules_page%26utm_campaign%3Dorganic).

[Privacy policy](./) | [Gizlilik politikası](tr/)
