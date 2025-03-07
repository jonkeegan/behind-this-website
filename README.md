### Who’s behind this website? A Checklist. 

By Prianjana Bengani ([@acookiecrumbles](https://twitter.com/acookiecrumbles)) and Jon Keegan ([@jonkeegan](https://twitter.com/jonkeegan))

By Priyanjana Bengani
Data Reporter
Bloomberg
Bluesky: @acookiecrumbles.bsky.social
Mastodon: @acookiecrumbles@indieweb.social

Jon Keegan
Tech reporter / Data journalist
Sherwood News
Bluesky: @jonkeegan.com


Oringinally presented at IRE NICAR Conference - March 4, 2022 - Updated March 2025
Slides: [English](https://bit.ly/nicar25-behind-this-website) | [Russian ](https://docs.google.com/presentation/d/1TxynZrKKrYMvPFk3oxYMNRkx8fp0Gs_AhQufuVkKOOo/edit?usp=sharing) (earlier version)

*Thank you to Svetlana Borodina at Harriman Institute for the Russian translation!*


#### What is this?

This checklist is meant to be used as a reporting tool to help journalists and researchers when trying to find out who published a website. This is meant to be used in conjunction with offline reporting techniques. 

Following this checklist does not guarantee that you can unmask the owner of a website that does not want to be found, but it can help surface crucial clues and connections that can act as leads for further reporting. 

🌟 Strong recommendation: while running through this checklist, create a data diary — it can be a TextEdit doc, a Google Doc, just the Notes app, whatever. It is important to be able to retrace your steps. 

# Who’s Behind This Website?

**Priyanjana Bengani**  
Data Reporter, Bloomberg  
[@acookiecrumbles.bsky.social](https://bsky.social)  
[@acookiecrumbles@indieweb.social](https://indieweb.social)

**Jon Keegan**  
Tech Reporter / Data Journalist, Sherwood News  
Bluesky: [@jonkeegan.com](https://jonkeegan.com)

**Updated March 2025**

- [GitHub Repository](https://github.com/jonkeegan/behind-this-website)
- [Slides](https://bit.ly/nicar25-behind-this-website)


## The New Normal: More Opacity, Less Transparency

### Existing Tools Are Breaking  
- Google Cache no longer exists (but Bing Cache still does).  
- Microsoft shut down RiskIQ.  
- Google dorks / search operators are inconsistent.

### World of Platforms and Walled Gardens  
- Google Analytics 4 disallows finding relationships between websites based on ID.  
- Platforms are restricting transparency tools, retreating from content moderation.  
- CrowdTangle no longer exists; journalists can’t get access to the Meta Content Library.  
- The X (formerly Twitter) API is prohibitively expensive.  
- More platforms to monitor: Mastodon, Bluesky, Threads, Discord, Telegram.

### Concealing Identities Is Easier  
- WHOIS is less useful for new domains due to GDPR.  
- Squarespace, WordPress, GoDaddy static websites share IP addresses with thousands of sites.  
- CDNs make IP address matching harder.  
- Easy to incorporate a company with false identities.

---

## Somebody Set This Website Up!  
**Who? Why? When? How?**

### Who?  
- Who’s featured on the website?  
- Are there authors, email addresses, profile pictures?  
- Are there payment options (crypto, PayPal, donations, subscriptions)? Who’s receiving the money?  
- Are authors common across multiple sites or exclusive to this one?  
- Is the owner trying to stay hidden?

### Why?  
- Was the site set up to make money (scams, ads, content farms)?  
- Is it part of influence operations?  
- Promoting political candidates or social advocacy?  
- Deceiving audiences by impersonating another website?  
- Poisoning LLMs?

### When?  
- When was the domain first registered?  
- How long has the site existed in its current form?  
- Was it offline for any significant time?  
- Did the ownership change? (Check historical WHOIS)  
- Did the site’s design or content change drastically?

### How?  
- What is the tech stack? Where is it hosted?  
- Is it a WordPress site? (Check authors, templates, plugins)  
- How is it monetized? Affiliate links, advertising?  
- Is the content generated by AI?  
- Where does it link to, and who links to it?

---

## Documenting, Archiving, Monitoring

### 📝 Documenting  
- Maintain a data diary with detailed notes.  
- Create a timeline of the website’s evolution.  
- Use [Hunchly](https://www.hunch.ly) or screen recordings.

### 📚 Archiving  
- Archive sites consistently using [archive.org](https://archive.org) and [archive.is](https://archive.is).  
- Screenshots are essential for non-archivable content.  
- Download videos before they are taken down ([yt-dlp](https://github.com/yt-dlp/yt-dlp)).  
- Capture full browser windows with timestamps ([GoFullPage](https://gofullpage.com), [ArchiveWeb](https://archiveweb.page)).

### 🔍 Monitoring  
- Set up alerts with [Klaxon Cloud](https://www.muckrock.com/news/archives/2023/dec/04/klaxon-cloud-free-simple-alerts-when-a-webpage-updates/) or [VisualPing](https://visualping.io).  
- Automate screenshots over time with [GitHub Actions](https://github.com) and [ShotScraper](https://github.com/simonw/shot-scraper).

---

## So Many Tools  
- Investigative techniques > tools.  
- Most investigations require multiple tools.  
- Tools can be expensive, overpromise, underdeliver, and collect data unethically.  
- Platforms rise and fall, APIs disappear.  
- Don’t get too dependent on one tool.

[List of OSINT tools](https://start.me/p/7kxyy2/osint-tools-curated-by-lorand-bodo)

---

## Protecting Yourself Online  

### 🛡️ IP Address Protection  
- Use a VPN or Tor (note: some VPNs track activity).  
- Use a separate browser in incognito/private mode.

### 📧 Email Protection  
- Use a different email address for newsletter signups.  
- Block remote content loading to prevent tracking.  
- Use the `+` trick (e.g., `johnsmith+newsletter@gmail.com`).

### 💻 Virtual Machine  
- Use [UTM](https://getutm.app) or [VMware](https://www.vmware.com) for sandboxing.

---

## Ethics & Legality  

### Ethics  
- Some tools collect data from shady sources (data brokers).  
- Investigations should avoid doxxing individuals.

### Legality  
- Scraping publicly available content is generally fine but be aware of the [Computer Fraud and Abuse Act](https://www.cjr.org/tow_center_reports/data-journalism-and-the-law.php).  
- Accessing unauthorized credentials is a legal risk.  
- The Missouri SSN exposure case shows that even “viewing source” can be misinterpreted as hacking.

[Read More](https://www.cjr.org/tow_center_reports/data-journalism-and-the-law.php)

---

## Investigating Site Content  

### 📝 Text  
- Check for duplicate text using exact string searches.  
- Look for names, emails, phone numbers, social media handles, company names.

### 🖼️ Media  
- Use reverse image search (Google, Bing, Yandex).  
- Check for stock images or repeated profile pictures.  
- Use facial recognition ([PimEyes](https://pimeyes.com), [Search4Faces](https://search4faces.com/en/)).  
- Extract metadata from images ([EXIF Data](http://exifdata.com)).  
- Use forensic tools to detect AI-generated content ([WeVerify](https://weverify.eu), [Forensically](https://29a.ch/photo-forensics/)).

### 📄 Documents  
- Use Google dorking (`filetype:pdf site:<domain>.com`).  
- Check PDF metadata. Use [Dangerzone](https://dangerzone.rocks) for safe viewing.

---

## Investigating Domains & Infrastructure  

### 🏠 Ownership  
- Lookup WHOIS data ([Whoxy](https://www.whoxy.com), [DomainTools](https://www.domaintools.com)).  
- Find related domains ([DNSTwist](https://dnstwist.it)).  

### 🔗 Shared Infrastructure  
- Find domains sharing the same IP ([SecurityTrails](https://securitytrails.com), [BuiltWith](https://builtwith.com)).  
- Identify shared analytics identifiers ([BuiltWith](https://builtwith.com), [DomainTools’ Iris Investigate](https://iris.domaintools.com/investigate/)).

### 📡 Network Requests  
- Use [FouAnalytics X-Ray](https://pagexray.fouanalytics.com/) to analyze network requests.

---

## Investigating Social & Platform Connections  

### 📱 Social Media Presence  
- Find accounts with [WhatsMyName](http://whatsmyname.app), [Sherlock](https://github.com/sherlock-project/sherlock), [Blackbird](https://github.com/p1ngul1n0/blackbird).  
- Check Facebook Page Transparency.

### 📢 Ads & Influence  
- Check ad spending on platforms.  
- Monitor engagement levels.

---

## Case Study: Kremlin-Aligned Influence Networks in Europe  

Link: [https://www.thebureauinvestigates.com/stories/2024-07-06/russian-disinformation-networks-ramp-up-attacks-on-european-elections
](https://www.thebureauinvestigates.com/stories/2024-07-06/russian-disinformation-networks-ramp-up-attacks-on-european-elections
)
- Russian-aligned websites targeting Ukraine and Europe.  
- Hundreds of domains registered post-2022 invasion.  
- Tracked using WHOIS, analytics, and infrastructure tools.

---

## Resources  

### 📰 Newsletters  
- [Craig Silverman’s Digital Investigations](https://digitalinvestigations.substack.com)  
- [Digital Digging](https://www.digitaldigging.org)  
- [The OSINT Newsletter](https://osintnewsletter.com)

### 📚 Books  
- *Verification Handbook* ([Craig Silverman](https://datajournalism.com/read/handbook/verification-3))  
- *Open Source Intelligence Techniques* ([Michael Bazzell](https://inteltechniques.com/book1.html))  
- *Hacks, Leaks, and Revelations* ([Micah Lee](https://hacksandleaks.com/))
