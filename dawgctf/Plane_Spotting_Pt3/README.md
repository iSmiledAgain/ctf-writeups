# Plane Spotting Pt. 3

**Category:** OSINT  
**Points:** 250  

## Challenge

![Challenge Description](./assets/plane_spotting_3_desc.png)

## Challenge Image

![Aerial view taken from plane window shortly after takeoff](./assets/planespotting3.jpg)

## Solution

**Step 1 - Extract image metadata.**  
Running `exiftool` on the image returned a precise **timestamp** of when the photo was taken. Unlike Pt. 2, no GPS coordinates were embedded. The challenge required identifying the location visually and cross-referencing with flight data.

```bash
exiftool planespotting3.jpg
```

**Step 2 - Geolocate the aerial view.**  
Reverse image searching the aerial photo pointed to **Seattle, Washington**. The geography is distinctive:

- Large body of water to the left → **Puget Sound**
- Smaller lake visible mid-frame → **Lake Burien**
- Dense urban grid with suburban sprawl
- Port/cargo area visible at lower right

This is consistent with the view shortly after departing **Seattle-Tacoma International Airport (SEA)**, climbing and banking southward.

**Step 3 - ADS-B replay.**  
Using **ADS-B Exchange replay mode**, I set the date and time to match the EXIF timestamp and filtered for departures from **SEA** in that window. The altitude, heading, and aircraft livery visible in the Pt. 2 image (same series) narrowed the candidates significantly.

**Step 4 - Identify the registration.**  
Cross-referencing the flight track and departure time, the aircraft was identified as an **Alaska Airlines Boeing 737** with registration **N609AS**.

## Flag

![Flag](./assets/plane_spotting_3_flag.png)

```
N609AS
```
