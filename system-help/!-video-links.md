---
title: "! video links"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "! video links"
long_description: "Help documentation for ! video links in the 4GL system."
---

! video links
=============

1. **Log in to Vimeo** (pparsons@4glsol.com/stm4glsol).
2. If not already uploaded, upload the video to the SM3 Help videos folder.
3. In the SM3 Help videos folder, find the video you want to embed into Flare.
4. Click on a video to open it, then click Appearance on the left.
   * **Engagement** and **Details** -- toggle on Hide all.
   * **Play button** -- Bottom.
   * **Controls** -- disable Transcript, Chromecast, Airplay, Picture-in-picture, and the Vimeo logo.
   * Click Save.
5. In the top right corner of the page, click **Share>Copy embed code**.
6. **In Flare**, create a new topic in the Videos folder. For example, for the Remarks video:  
   File Name = vid-remarks  
   1st Heading = Video Remarks How To; Title = Remarks How To  
     
   For Webinars:  
   File Name = vid-webinar-Jan2025  
   1st Heading = Webinar January 2025; Title = January 2025
7. In the topic heading, insert an en dash after “Video”.
8. Insert the VideoRefresh snippet after the heading. Make sure it’s formatted as a Tip.
9. Go into the internal Text Editor view.
10. After the snippet, select the entire line of the placeholder paragraph and paste the Vimeo embed code over it (so the new div is not embedded within a <p>).
11. For webinar topics: after the snippet (and before the video), include a table of the topics and versions (per file prepared by Paul in *Sharepoint: Documents>4GL Solutions>Webinars>2025 Webinar>4GL Solutions Webinar Enhancements.xlsx*; review for typos). Add this in a dropdown (see January 2025 for an example).
12. Copy the H1 text, then go into the Topic Properties and add a meta tag with the same text as the H1 (e.g. Video - Remarks How To; for webinars, include the versions it covers, e.g. “Webinar – January 2025 (3.21, 3.22)”).
13. Save and regenerate output as usual.
14. For webinar topics, in the corresponding Release Notes>Highlights topic(s), add a link to the video (see 3.22 Highlights for an example).

---