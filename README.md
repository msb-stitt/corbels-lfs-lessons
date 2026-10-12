# corbels-lfs-lessons

The large files behind *Corbels FTC Programming Lessons in Java*, kept in Git LFS: the videos, the
screenshots and figures, and what each release published. The book's text and code live in
[msb-stitt/ftc31459-26-27-biobuzz](https://github.com/msb-stitt/ftc31459-26-27-biobuzz); its
`gh-pages` branch holds only what is published now, and can be thrown away and rebuilt from here.

## What is where

- **`main`** holds this README and `.gitattributes`, and nothing else.
- **A branch named for a `ftc31459-26-27-biobuzz` branch** holds the sources for the book on that
  branch: each page's current video, in `videos/`, and the figures, in `figures/`.
- **A tag named for a `ftc31459-26-27-biobuzz` release**, such as `v0.1.3-rc.1`, holds that
  release's sources and what it published: the built site, both PDFs and the videos.

Only the current video of each page is kept, not the takes it was cut from.

## Setting up a clone

Install Git LFS, then, inside the clone:

```sh
git lfs install --local
git lfs pull
```

`--local` sets Git LFS up for this clone only, without changing `~/.gitconfig`.

## Checking it

```sh
git lfs fsck --pointers
```

It fails if a video, picture or PDF was committed as an ordinary file instead of through LFS.

## Downloads cost bandwidth

The repository is public, and every download of an LFS file, by anyone or by GitHub Actions,
counts against the owner's monthly LFS bandwidth. Fetch only what you need, with
`git lfs pull --include <folder>`.

GitHub Pages does not serve files from here; the published book is on `ftc31459-26-27-biobuzz`'s
`gh-pages`.
