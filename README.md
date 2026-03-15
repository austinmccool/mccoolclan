# McCool Clan — Family Tree Site

## Files

```
index.html     ← The site. Don't touch unless you're changing design.
family.js      ← YOUR FILE. Add every new person here.
photos/        ← Drop all photos in here.
README.md      ← This file.
```

---

## How to Add a Person

Open `family.js`. Copy this template and fill it in:

```js
{
  id: "firstname-lastname",       // unique, lowercase, hyphens only
  name: "Full Name",
  nickname: null,                  // or "Bob", "Grandma", etc.
  birth: "1945",                   // year, or "Jan 12, 1945"
  birthplace: "Evansville, IN",
  death: null,                     // null = still living
  deathplace: null,
  bio: "One or two sentences about this person.",
  photos: ["photos/name1.jpg"],    // list as many as you have
  parents: ["dad-id", "mom-id"],   // use their ids
  spouses: ["spouse-id"],
  children: ["child-id"],
  generation: 3,                   // match the generation level
},
```

Then:
1. Add their `id` to their parents' `children` array
2. Add their parents' `ids` to their `parents` array
3. Save. The tree updates.

---

## Generations

| # | Who |
|---|-----|
| 1 | Oldest known ancestors (Cornelius & Bridget) |
| 2 | Their children |
| 3 | Grandchildren of Gen 1 |
| 4 | etc. |

---

## Photos

- Create a folder called `photos/` next to `index.html`
- Drop photos in there: `photos/austin-mccool-1.jpg`
- Reference in family.js: `photos: ["photos/austin-mccool-1.jpg"]`
- Multiple photos = gallery strip in the profile panel

---

## Hosting (Vercel)

Same workflow as CredneXus:
1. Push to GitHub
2. Vercel auto-deploys
3. Point `mccoolclan.com` DNS to Vercel

---

## Tips

- Leave unknown fields as `null` — the site handles it gracefully
- IDs must be unique — if two people share a name, add a middle name or birth year: `robert-mccool-1908`
- `generation` just controls what row they appear on — use your judgment for in-laws and step-relations
- The tree grows automatically as you add people — no layout adjustments needed
