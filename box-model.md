Links
---
- [box model](http://learnlayout.com/box-model.html)
- [block-formatting](https://www.w3.org/TR/CSS21/visuren.html#block-formatting)
- [CSS 2.1 Specification](https://www.w3.org/TR/2011/REC-CSS2-20110607/#minitoc)

Normal Flow
---
*Boxes in the normal flow belong to a formatting context, which may be `block` or `inline`, but not both simultaneously. `Block-level` boxes participate in a block formatting context. `Inline-level` boxes participate in an inline formatting context.*

Collapsing margins
---
*In CSS, the adjoining margins of two or more boxes (which might or might not be siblings) can combine to form a single margin. Margins that combine this way are said to collapse, and the resulting combined margin is called a collapsed margin.*

line box
---
*In an inline formatting context, boxes are laid out horizontally, one after the other, beginning at the top of a containing block. Horizontal margins, borders, and padding are respected between these boxes. The boxes may be aligned vertically in different ways: their bottoms or tops may be aligned, or the baselines of text within them may be aligned. The rectangular area that contains the boxes that form a line is called a `line box`.*

inline box splitting & overflow
---
When an inline box is split, margins, borders, and padding have no visual effect where the split occurs.

When an inline box exceeds the width of a line box, it is split into several boxes and these boxes are distributed across several line boxes. If an inline box cannot be split (e.g., if the inline box contains a single character, or language specific word breaking rules disallow a break within the inline box, or if the inline box is affected by a white-space value of nowrap or pre), then the inline box overflows the line box.
