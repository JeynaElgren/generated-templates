# Manuscript

Prose lives here, one file per scene: `chNN-sNN.md` (e.g. `ch03-s02.md`), matching
the scene card id in `../scenes/`. Zero-padded numbers keep the files sorted.

To assemble a chapter or the whole book:

```sh
cat manuscript/ch03-s*.md > ch03.md                                # one chapter
ls manuscript/ch*-s*.md | sort | xargs cat > full-manuscript.md    # everything
```

Scene files hold prose only: no front matter or notes. Planning belongs on
the scene card. The one exception is a `<!-- PROPOSED: … -->` marker the assistant
leaves inline for canon awaiting the author's decision.
