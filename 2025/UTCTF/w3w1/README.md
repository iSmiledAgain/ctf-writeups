# W3W1

**CTF:** UTCTF 2025  
**Category:** Misc  
**Flag:** `utflag{floating.offices.splash}`

---

## Challenge Description

> The three words I would use to describe this location are...

**Flag format:** `utflag{word1.word2.word3}`

One image attached.

---

## Image

![W3W1](./W3W1.jpg)

---

## Analysis

The image shows a church with a steeple and a cross, and a "Come y'all!" banner visible at street level. There was also a logo next to the banner followed by the word "TEXAS". The logo was the **The University of Texas at Austin** logo. While looking around the area in Google Street View, I noticed that the architectural style was very similar to the one in the image. I was going through the churches in that area, and one of them happened to match the one from the image. It turned out to be the **University Christian Church** on Guadalupe St, directly adjacent to UT Austin's campus in Austin, Texas.

Key identifying features:
- The surrounding buildings - the architectural style of the nearby buildings looked very similar to the ones around the church on Guadalupe St near UT Austin, which helped confirm that I was in the right locality.
- Church architecture - matches University Christian Church's facade.

---

## Solve

1. Identified the church as **University Christian Church, 2256 Guadalupe St, Austin, TX** using visual landmarks
2. Navigated to [what3words.com](https://what3words.com) and pinpointed the exact 3m × 3m square at that location
3. Retrieved the three-word address for that square

---

## Flag

```
utflag{floating.offices.splash}
```
