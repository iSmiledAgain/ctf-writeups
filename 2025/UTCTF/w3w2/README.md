# W3W2

**CTF:** UTCTF 2025  
**Category:** Misc  
**Flag:** `utflag{gadgets.syndicate.conditioning}`

---

## Challenge Description

> The three words I would use to describe this location are...

**Flag format:** `utflag{word1.word2.word3}`

One image attached.

---

## Image

![W3W2](./W3W2.jpg)

---

## Analysis

The image shows a double rainbow over a small roadside shop and the shop sign reads **"Merchandice & Gift Shop - Maui Gifts · Logo Items · Snacks"**. The landscape, overcast tropical sky, and overhead power line configuration are consistent with a roadside strip in **Kihei, Maui, Hawaii**.

Key identifying features:
- Shop sign explicitly states "Maui Gifts"
- Power infrastructure style consistent with rural Hawaii

---

## Solve

1. Read the shop sign: "Maui Gifts" immediately pins the island
2. Cross-referenced the shop name **"Merchandice & Gift Shop"** to its location on **South Kihei Road, Kihei, Maui, HI**
3. Navigated to [what3words.com](https://what3words.com) and identified the exact 3m × 3m square at the shop's position
4. Retrieved the three-word address

---

## Flag

```
utflag{gadgets.syndicate.conditioning}
```
