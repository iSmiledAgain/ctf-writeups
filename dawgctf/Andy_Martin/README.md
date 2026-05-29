# Andy Martin

**Category:** OSINT  
**Points:** 400  

## Challenge

![Challenge Description](./assets/andy_martin_desc.png)

## Solution

**Step 1 - Find the right Andy Martin.**  
The challenge description gives enough to identify the target: a Londoner who has traveled to Mauritius and Portugal, leaving an "unorthodox trail." Searching for Andy Martin on Google Maps surfaced a reviewer profile with travel reviews spanning multiple countries matching the description.

**Step 2 - The date problem.**  
Google Maps does **not** display exact review dates - only relative timestamps like "3 years ago" or "7 years ago". This makes pinpointing a specific date like July 12, 2018 impossible directly from the UI.

**Step 3 - EXIF data in review photos.**  
Key insight: when users attach photos to Google Maps reviews, those images often retain their original **EXIF metadata**, including the exact date and time the photo was taken.

Filtering Andy Martin's reviews to food/restaurant entries that appeared ~7–8 years old (i.e., around 2018), I downloaded the photos attached to those reviews and ran `exiftool` on each:

```bash
exiftool <image_file>
```

This returned the `DateTimeOriginal` field embedded in each photo.

**Step 4 - Match to the target date.**  
One photo's EXIF timestamp matched **Thursday, July 12, 2018**. The associated Google Maps review was for a restaurant in London:

**Poppies Fish & Chips**

## Flag

![Flag](./assets/andy_martin_flag.png)

```
Poppies Fish & Chips
```
