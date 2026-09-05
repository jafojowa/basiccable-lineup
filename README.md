# basiccable-lineup

**Machine-published data. Not a project.**

This repository holds the curated channel lists for **Basic Cable** — JSON files
of TMDB/TVDB ids, one per catalogue entry, plus a `manifest.json` naming every
file and its versions. The app downloads them to decide which titles belong to
its concept channels.

- **No source code lives here.** The application is elsewhere and private.
- **Not open to contributions.** Every file is written by an automated weekly
  job; a pull request here would be overwritten by the next run.
- **Public so that the app can fetch it** without credentials. That is the only
  reason.

## Layout

```
manifest.json      every list, its content version and the list-format version
006.json           one file per catalogue entry, named by its catalogue NUMBER
```

Files are named by catalogue number and carry no channel names: the names live
in the app, so renaming a channel is a release-free change and never touches
this repo.

## Versions

Each file carries two, and they mean different things:

- **`formatVersion`** — the shape of the file. Changes **additively only**, so an
  older build can always read a newer file: it ignores fields it does not know
  and every field it needs is still there.
- **`version`** — the contents. Changes whenever the list does.

## Attribution

Lists are derived from data supplied by [TMDB](https://www.themoviedb.org/).
This product uses the TMDB API but is not endorsed or certified by TMDB.
