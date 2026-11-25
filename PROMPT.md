# PROMPT — news-image-20261126

Build an entry for make.fun's "Sum up 26 November's world news in one image"
bounty ($100, top 50 share the prize).

Research the world's news of Thursday 26 November 2026 from several sources
and cross-check the date of every story: only events that happened, or were
first reported, on 26 November 2026 in any time zone may appear. Do not use
stories from 24–25 November (Shenzhou-24, the Colombia hostage rescue, the
Huawei verdict) or earlier (ICJ Rohingya ruling 19 Nov, BepiColombo 21 Nov).

Draw the entry as an original newspaper front page, 1024 x 1024, JPEG under
1 MiB: masthead, the date in large type, one lead story and five more stories
across regions and fields, each with a short headline, a one-line summary and
a small drawn emblem. No photos, no borrowed artwork, no text addressed to
the judge beyond the page itself. Every word must be spelled correctly and
nothing may be cut off or overlap.

`main.ts` (Node 22, standard library only) copies the image to
`/output/entry.png` (or `$MAKEFUN_OUTPUT_DIR/entry.png` outside the grader)
and self-checks the copy. Run it twice to two different output directories
and confirm byte-identical output. Verify the image visually by reading it
back before finishing.
