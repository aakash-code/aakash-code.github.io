# Portfolio media — drop-in guide

The site (`../index.html`) **auto-detects** whatever you drop into these folders.
You don't edit any code — just add files with the right names and reload the page.

## Per-project folders
Each project has a folder named by its slug:

| Folder        | Project on the site            |
|---------------|--------------------------------|
| `sgvp/`       | SGVP Management System         |
| `freshmor/`   | Freshmor                       |
| `spoonly/`    | Spoonly                        |
| `kailor/`     | Kailor (already populated ✅)   |
| `openalgo/`   | OpenAlgo                       |
| `openequity/` | OpenEquity                     |
| `nivas/`      | Nivas Realty (private)         |

## File names the page looks for (inside each folder)

| File name                       | Where it shows                                            |
|---------------------------------|-----------------------------------------------------------|
| `cover.jpg`                     | The **preview image on the project card** (use the best frontend shot) |
| `frontend-1.jpg` … `frontend-10`| **Frontend** screenshots in the pop-up gallery            |
| `backend-1.jpg`  … `backend-10` | **Backend / admin** screenshots in the gallery            |
| `demo.mp4`                      | Your **screen recording**, plays inside the gallery       |

- Extensions `.jpg`, `.jpeg`, `.png`, `.webp`, `.gif` all work (the page tries each).
- Numbering must start at **1** and be contiguous (`frontend-1`, `frontend-2`, …).
  The page stops at the first gap, so don't skip numbers.
- Every file is optional. A project with **no** files just stays a text card.
- A card gets a clickable cover as soon as it has **at least one** image. If there's
  no `cover.*`, the first frontend shot is used as the cover automatically.

## Hero (top of the page)
Drop `hero/hero.jpg` (or `.png`/`.mp4`*) and it appears as a faint background behind
the headline. Remove it and the original animated gradient shows instead.
*(\* image recommended; very large videos slow the first paint.)*

## Example — fully kitting out SGVP
```
media/sgvp/cover.jpg
media/sgvp/frontend-1.jpg   # public event site
media/sgvp/frontend-2.jpg   # registration form
media/sgvp/backend-1.jpg    # admin dashboard
media/sgvp/backend-2.jpg    # RBAC / scheduling
media/sgvp/demo.mp4         # 30–60s screen recording
```
Reload → the SGVP card shows a cover with a “▶ 6 media” badge; clicking it opens the
gallery with frontend shots, backend shots, and the video.

## Kailor reference
Kailor is already wired up from real captured assets (`kailor-cover.png`,
`storefront-shop.gif`, `kailor-admin.png`, `admin-tour.gif`, `feature-flags.gif`,
`kailor-demo.mp4`) — open its card to see exactly how a finished gallery looks.
