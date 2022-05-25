---
title: Ad Specifications
description: Reference general and publisher-specific ad specifications.
feature: DSP Ads
exl-id: 905dfd9b-e7a3-4eb6-988f-b49d4b282dd2
---
# Specifications for Supported Ad Types

## Video Ads (Pre-Roll and CTV)

### Supported Screens

Ads are delivered by default on desktop, mobile, and connected TV devices. Device targeting is available to adjust delivery.

### Supported Third-Party Ad Servers

You can use tag sheets from [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid], and [!DNL Sizmek]. For a full list of supported vendors, see "[Certified Ad Serving Partners](certified-ad-servers.md)."

### Requirements for High-Definition Video Assets (Required)

**Video Tag Type:** VPAID 2.0 JavaScript or VAST (CTV). All VPAID ad units must adhere to the [VPAID 2.0 specification](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) as defined by the Interactive Advertising Bureau (IAB).

**Video Codec:** MP4/H.264

**Resolution:** 1280x720 for 720p, 1920x1080 for 1080p 

**Bitrate:** 1500-2500 kbps for 720p, 2500-3500 kbps for 1080p

**H.264 Profile/Level:** High profile, level 3.1 for 720p; High profile, level 4.0 for 1080p 

**Video Frame Rate:** 29.970 fps (commonly referred to as 30 fps) for NTSC countries, 25 fps for PAL countries, 23.976 fps (commonly referred to as 24 fps) for film-look content

**Video Color Space:** 4:2:0 YUV Chroma subsampling 

**Video Interlacing:** Progressive scanning, i.e., non-interlaced. No intra-field motion (blending frames) or interlacing.

**Leaders (Slate):** Not permitted

**Audio Codec:** AAC-LC or HE-AACv1 

**Audio Bitrate:** 128-192 kbps for AAC-LC, 64-128 kbps for HE-AACv1

**Audio Channel:** 2-channel stereo mix 

**Audio Sample Rate:** 44.1 kHz or 48 kHz, as per source material 

**Audio Levels:** 24 LKFS (+/- 2.0 dB) in the US as per ATSC A/85; 23 LUFS (+/- 1.0) in the EU as per EBU R128

#### Additional Publisher Requirements for Connected TV Ads

* **Hulu:** See Hulu's [ad specifications](https://advertising.hulu.com/ad-products/video-commercial/).

* **Paramount:** See Paramount's [ad specifications](https://www.paramount.com/digital-ads).

* **Discovery:** See Discovery's [ad specifications](/help/dsp/assets/discovery-networks-ad-specs.pdf).

* **HBO Max:** See HBO Max's [ad specifications](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx).

* **A+E Network:** See A+E Network's [ad specifications](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **NBCUniversal:**
 
  * [Digital Video](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

  * [Livestream](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

  * [Peacock](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/) 

* **Disney:**

  * ESPN Livestreaming:
  
    **Bit Rate:** > 14000kbps
    **Format:** .mp4
    **Tag Type:** VAST 2.0
    **Creative Size:** 1280x720 or 1920x1080

  * Full-episode programming (FEP): ESPN, ABC, Freeform, Nat Geo, and FX
  
    * **Bit Rate:** > 14000 kbps:
    
      **Format:** .mp4

      **Tag Type:** VAST 2.0
      
      **Creative Size:** 1280x720 or 1920x1080
    
    * **Bit Rate:** > 1000 kbps (low resolution) or 15000 kbps (high resolution):
    
      **Format:** .mp4
      
      **Tag Type:** VAST 2.0 (VPAID 1.0 on desktop only)
      
      **Creative Size:** 1280x720 or 1920x1080

## Display Ads

### Supported Screens

Ads are delivered by default on desktop and mobile devices. Device targeting is available to adjust delivery.

### Supported File Types

**Image:** GIF, JPG/JPEG, PNG

**HTML5:** Image file types: GIF, JPG/JPEG, PNG, SVG

### Requirements for Image Assets (Required)

Universal Display is supported.

**Recommended ad sizes:** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300x600, 320x50, 320x480, 480x60, 640x480, 88x31, 728x90, 970x250, 970x90

**Supported Third-Party Ad Servers:** You can use tag sheets from [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid], and [!DNL Sizmek]. For a full list of supported vendors, see "[Certified Ad Serving Partners](certified-ad-servers.md)."

## Audio Ads

### Supported Screens

Desktop, Mobile, Tablet, Smart Speakers, and Connected TV

### Supported Third-Party Ad Servers

You can use tag sheets from [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid], and [!DNL Sizmek]. For a full list of supported vendors, see "[Certified Ad Serving Partners](certified-ad-servers.md)."

### Requirements for Audio Assets (Required) 

**File type:** MP3, OGG, AAC

**Leaders (slate):**  Not permitted

**Maximum file size:** 2MB

**Bitrate:** 128

**File Length:** 0-60s

#### Additional Publisher Requirements

* **[!DNL Spotify]**
  * Length: Up to 30 seconds
  * File type: OGG
  * Maximum file size: 500MB
  * Volume: RMS normalized to -14; dBFS peak normalized to -0.2 dBFS

* **[!DNL SoundCloud]**
  * Length: 6, 15, or 30 seconds
  * File type: MP3
  * Maximum file size: 5 MB

* **[!DNL Pandora]**
  * Length: 15 or 30 seconds
  * File type: MP4 (in-app), MP3 (desktop)
  * Maximum file size: 2.2 MB 

* **[!DNL TuneIn]**
  * Length: 10, 15, or 30 seconds
  * File type: MP3, OGG
  * Volume: 44.1 kHz 

* **[!DNL iHeartRadio]**
  * Length: 5, 15, 30 or 60 seconds 
  * File type: MP3
  * Maximum file size: 320 kbps
  * Volume: 44.1 kHz 

* **[!DNL TargetSpot]**
  * Length: 15, 30 or 60 seconds
  * File type: MP3

### Requirements for Companion Banner Ads (Optional)

**Supported sizes:** 300x250, 500x500, 640x640, 1024x1024

#### Additional Publisher Requirements

* **[!DNL Spotify]:**
  * File type: Static JPG, PNG
  * Maximum file size: 200 KB
  * Dimensions: 300x250

* **[!DNL SoundCloud]:** 
  * File type: Static JPG, PNG
  * Maximum file size: Under 400 KB
  * Dimensions: 1024x1024

* **[!DNL Pandora]:**
  * File type: JPEG, GIF
  * Maximum file size: Size: 100 KB
  * Dimensions: 300x250 (mobile or desktop), or 500x500 (desktop)

* **[!DNL TuneIn]:**
  * File type: JPEG, JPG, PNG, GIF, HTML
  * Maximum file size: 2 MB
  * Dimensions: 300x250

* **[!DNL iHeartRadio]:**
  * File type: JPEG, JPG, PNG, GIF, SWF, HTML
  * Maximum file size: 2.2 MB
  * Dimensions: 300x250
 
## Native Display Ads

Each ad can include either a still image or a moving GIF (cinemagraph).

### Supported Screens

Ads are delivered by default on desktop and mobile devices. Device targeting is available to adjust delivery.

### Required Assets for All Native In-Feed Formats 

#### Image Asset

**Resolution:** Minimum 600x600px; Recommended minimum of 1200x627px

**File type:** JPEG (image ad or video ad cover image), GIF (cinemograph)

**File Size:** Less than 1 MB (Image should be free of text.)

#### Advertiser Logo

**Resolution:** Minimum 80x80px; Recommended minimum of 300x300px

**File type:** JPEG or PNG.

**Aspect ratio:**  1x1 ratio

>[!NOTE]
>
>Depending on the image over which it will overlayed, choose between light or dark logo assets.

#### Text/Copy

**Headline:** Maximum 200 characters; 25 characters recommended

**Caption:** Maximum 200 characters; 100 characters recommended

**Sponsored By:** Maximum 200 characters; 30 characters recommended

**Call to Action (MoPub Only):** Maximum 15 characters

>[!NOTE]
>
>The final layout is defined by the publisher at runtime. If an ad exceeds the recommended character count, some inventory providers may not to deliver the ad, or the publisher or SSP may truncate the text. 

#### Landing Page URL

The clickthrough URL with optional click trackers.

Requirements for click trackers:

* Third-party impression-tracking pixels: 1x1 image URL format only

* Viewability JavaScript trackers: Supported for IAS only; 1x1 images in JS.append format only

* Third-party click-tracking pixels: Must redirect to the landing page embedded in the URL (HTTP 302 redirect)

* Data management platform (DMP) click trackers with 200 or more responses aren't supported.

>[!MORELIKETHIS]
>
>* [About Ad Management](ad-about.md)
>* [Create a Single Ad](ad-create.md)
>* [Create Multiple Third-party Ads](ad-create-multiple.md)
>* [Edit an Ad](ad-edit.md)
