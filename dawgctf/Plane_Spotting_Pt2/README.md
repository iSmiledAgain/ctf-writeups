# Plane Spotting Pt. 2

**Category:** OSINT  
**Points:** 225  

## Challenge

![Challenge Description](./assets/plane_spotting_2_desc.png)

## Challenge Image

![Southwest Airlines aircraft on approach](./assets/planespotting2.jpg)

## Solution

**Step 1 - Extract image metadata.**  
Running `exiftool` on the provided image revealed embedded **GPS coordinates** in the EXIF data, giving the exact location where the photo was taken.

```bash
exiftool planespotting2.jpg
```

The coordinates placed the photographer near a major airport approach path.

**Step 2 - Identify the airport.**  
Plotting the GPS coordinates on Google Maps confirmed the photo was taken near an airport. The aircraft is clearly on final approach.

**Step 3 - Track the flight via ADS-B.**  
Using the **timestamp from the EXIF data**, I loaded **ADS-B Exchange** in replay mode, set the date and time to match the image, and filtered for flights in the area of the GPS coordinates. This narrowed down which specific flight was being photographed.

**Step 4 - Determine origin.**  
The ADS-B replay confirmed the inbound flight had departed from **Nashville International Airport**.

- IATA code: **NAS**

## Flag

![Flag](./assets/plane_spotting_2_flag.png)

```
DawgCTF{NAS}
```
