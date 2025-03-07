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


#### Documenting and monitoring

- Maintain a data diary with detailed notes about what you’ve looked at and how you got there
- Try to create a timeline of the website and how it’s evolving over the course of your investigation
- Use [Hunchly](https://www.hunch.ly/) or screen recordings to keep track of everything you’re doing
 - Set up [Klaxon Cloud](https://www.muckrock.com/news/archives/2023/dec/04/klaxon-cloud-free-simple-alerts-when-a-webpage-updates/) or [VisualPing](https://visualping.io/) to be notified of any changes to a site 
 - Use [GitHub Actions](https://docs.github.com/en/actions) and [ShotScraper](https://github.com/simonw/shot-scraper) for automated screenshots over time

 - Archive sites consistently, and in some cases, use multiple archival services (archive.org, archive.is)
- For public records or social media posts, take screenshots — some of them might not be archivable
- Download videos lest they get taken down. Youtube videos: [yt-dlp](https://github.com/yt-dlp/yt-dlp)
- Take screenshots with timestamps so you can monitor changes and gather receipts ([GoFullPage](https://gofullpage.com)). 
- Capturing the full browser window with the URL field helps strengthen your evidence



#### Site Content

##### Text
- Check text fragments from articles, about-us pages, and privacy policies to see if they are unique to the site or duplicated [Use exact string matching on multiple search engines]

- Run article text through numerous tools to see if the text is AI-generated, but note lots of false positives in these tools [[GPTZero](https://gptzero.me), [OpenAI’s Text Classifier](https://platform.openai.com/ai-text-classifier), [ContentScale’s AI Detector](https://contentatscale.ai/ai-content-detector/), [CopyLeaks](https://copyleaks.com/ai-content-detector)]
- Browse site for any names (including bylines), email addresses, phone numbers, addresses, social media handles, and company names

- [ ] ✍️ Are there any authors listed? 
    - If the site is Wordpress, try this wildcard search on Google to reveal the author list: 
    "https://yourwebsite.com/author/*/"
    - If the site is Wordpress, active(!) and you are allowed to access it(!!), you can try getting the list of users accessing https://yourwebsite.com/wp-json/wp/v2/users . The list shows names, slugs and gravatar hashes (md5 of email address) for the authors of the site.
    - If the site is Wordpress, use [wpscan](https://wpscan.com/) to see the theme a Wordpress site uses as well as the authors, or use [built.with](built.with) for a technology profile. 
    - Use Bellingcat’s [Name Variant Tool](https://bellingcat.github.io/name-variant-search/#gsc.tab=0) to find possible variations on any names.
      
- [ ] 📫 Are there any e-mail addresses, phone numbers or contact information? 
  - If there are e-mail addresses, do those share the domain with the website?
  - Use tools like [Epieos](https://epieos.com) and [haveibeenpwned.com](https://haveibeenpwned.com/) to reverse lookup emails and phone numbers: both will show you other services and platforms on which the email address or phone number might exist. [TrueCaller](https://www.truecaller.com) also serves as a reverse yellow pages. 
  - Check to see if there is a Gravatar associated with that address: 
    - https://en.gravatar.com/site/check/XXXXX@gmail.com
- [ ] 🏢 Are there any companies listed?
  - If you find company names, use [OpenCorporates](https://opencorporates.com) or [LinkedIn](https://www.linkedin.com) to see whether any personnel information is available. [OpenCorporates](https://opencorporates.com) also lets you search by addresses — so you can find who else shares the same office location! 
- [ ] 🕑 What’s the server’s local time?
  - Look at the `datetime` attribute in links on Wordpress sites. GMT timestamp can reveal time zone based on GMT offset: 
    `<time class="updated" datetime="2022-03-04T10:21:40+06:00">March 4, 2022</time>`
- [ ] 🕶 Does the website have a privacy policy or terms and conditions that mentions an LLC, or what regional laws apply?
- [ ] 📡 Does the website have an RSS feed?
  - Does the RSS feed give any additional information about authors / stories that aren't visible on the site? 
  - You can pull RSS article links into Google sheets using [IMPORTFEED](https://infoinspired.com/google-docs/spreadsheet/how-to-use-importfeed-function-in-google-sheets/)
    

​
##### Features and functionality 
- [ ] 🗞 Does the website have a newsletter? 
  - Check for the physical postal address — required by the CAN-SPAM Act in the US
  - If you are allowed to access the site(!) you can try registering to the newsletter and examining the headers of the email you received. Those headers can reveal the IP address of the server
- [ ] 💸 Does the website collect donations? 
- [ ] 🛒 Does the website have an e-commerce store? Or, does it sell products?
    - Try walking through the checkout process (without paying). Sometimes the real payee name is revealed just before you confirm the payment.  
​
##### Links
- [ ] 🔗 What domains does the website link to most?
- Use [photon](https://github.com/s0md3v/Photon/wiki/Usage) or [urlscan.io](https://urlscan.io) to gather the outbound urls, (urls a site links to), as well as some high-level “intel” — who’s the site linking to the most? 
- Analyze outbound links, especially those to merch stores, for affiliate links — who’s the affiliate? (Especially useful for health and wellness scams) 
- [ ] ❤️ Who links to the domain most often? 
    - Google search operator: "link:yourwebsite.com"
    - Find who’s linking to the website of interest consistently by using a backlink checker ([ahrefs.com](https://ahrefs.com/backlink-checker), [Moz](https://moz.com/link-explorer)) — what’s the relationship between the sites? 
    
- [ ]  Do the links have UTM codes? 

​



##### Photos, images and documents
- [ ] 📸 Are there author photos? 
  - Use reverse image search to see if the same images appear elsewhere
  - Check [sensity.ai](https://sensity.ai) to see if the image is GAN-generated 
  - Read more about spotting GAN-generated images [here](https://www.theguardian.com/technology/2020/jan/13/what-are-deepfakes-and-how-can-you-spot-them).  
- [ ] 🔎 Do the images have EXIF data? 
    - Instructions [here](https://www.howtogeek.com/289712/how-to-see-an-images-exif-data-in-windows-and-macos/#:~:text=Viewing%20EXIF%20data%20in%20Windows,the%20photo%20was%20taken%20with.).
- [ ] 👀 Do the images have any other identifying information? 
  - Run through the list [here](https://themarkup.org/ask-the-markup/2020/03/12/photos-privacy)
- [ ] 🪣 Where are the images hosted?
  - If on AWS S3, the bucket name can be revealing — or you might find the bucket isn’t secure. 
- [ ] 📄 Are there PDFs hosted on the site? 
  - On a search engine, "filetype:pdf site:<yourwebsite.com>"
  - If you find some, check the metadata with "Get Info" in your PDF viewer.
- [ ] 🕛 Are there old archived images on [Wayback Machine](https://web.archive.org)?
  - Using the "URLs" page may find deleted images, filter on "image/" to narrow the search.
​
#### Social Media

If there are any social media profiles mentioned on the site, they are worth investigating. 

- [ ] 👤 Are there any social media accounts in the \<meta\> section of the HTML? 
- [ ] 📅 When were the individual accounts created? Does it line up with the site history?
- [ ] 📊 What platform has the biggest reach?
- [ ] 📣 Is the messaging different across platforms? 
- [ ] 📇 Do they have completely distinct account names across social media platforms or are they more-or-less the same? 
  - Note: just because you find the same account name across platforms doesn’t necessarily mean they belong to the same person! 
- [ ] 🔎 Use tools like [sherlock](https://github.com/sherlock-project/sherlock) and [Blackbird](https://github.com/p1ngul1n0/blackbird) that will scan multiple platforms to see if the same handle appears elsewhere — you’ll still have to confirm that it’s the same user and not just the same handle.



##### Facebook
On the Facebook profile, go to Page Transparency:
- [ ] ☎️ Is there an address and phone number for the page?
- [ ] ⏪ Does the page history reveal a different name? 
  - Has the page shifted topics? 
- [ ] 🐣 When was the Facebook page created?
- [ ]  Is the page running any groups? 
- [ ] 🗳 Has the page run any ads? Has the page run political ads? 
- [ ] 🤖 Does Facebook flag any ‘related pages’ for the given page? Rely on Facebook’s algorithms to find connections! 

​
##### Other platforms
Don't forget to check to see if the site has accounts on Youtube, Instagram, Reddit, Github, 

#### Infrastructure 
- [ ] 🗄 Have you archived the website? (You always should!)
  - you can do this on archive.org or use their [browser extension](chrome-extension://fpnmgdkabkmnadcjpehmlllkndpkmiak/about.html).

- [ ] 🖥 What is the website using? 
  - Is it using Wordpress, Squarespace, something else?

- [ ] ☁️ Where is it hosted? 
  - Is it on Google Cloud, AWS, Cloudflare, something else?
- [ ] What is the IP address of the website?
  - Which other websites are hosted on the same IP address? (won't work if it is behind Coudflare, or on shared hosting with thousands of other sites)
  - can check on [SecurityTrails](https://securitytrails.com)
- [ ] 🪳 Are there any trackers present? 
  - You can check [Blacklight](https://themarkup.org/blacklight) to begin with. 
- [ ] 🛍 How is the site monetised? 
  - Are there any affiliate links (Amazon, etc.)? 
- [ ] 🧬 What are the various tracking identifiers, and are those shared with other domains?
  - Check Google Analytics, Facebook Pixel, Quantcast, NewRelic, etc. 
  - Bellingcat’s [Wayback Analytics](https://github.com/bellingcat/wayback-google-analytics) tool looks at Internet Archive to extract old analytics IDs, which might be helpful in the present and can be used to aid the investigation.
  - Use tools like [builtwith](https://builtwith.com), [RiskIQ](https://www.riskiq.com/), or [Dnslytics](https://dnslytics.com/) to see if other domains share the same ID. 
- [ ] Look at the network requests
  - Use [FouAnalytics X-Ray](https://pagexray.fouanalytics.com/) to see all the network requests a site makes. 
- [ ] Are there any relevant subdomains? 
  - Use Farsight Security [DNSDBScout](https://www.farsightsecurity.com/tools/dnsdb-scout/) Flexible.
  - Use [Virustotal](https://www.virustotal.com/gui/url/) to verify site relations like subodmains, given files and favicons
  - Use [Alienvault OTX](https://otx.alienvault.com/) to verfiey any related subdomain to a given domain 
- [ ] 📜 Are there historic WHOIS records? 
  - Look at [Whoxy](https://www.whoxy.com/) or [RiskIQ](https://www.riskiq.com/). 
- [ ] ⌛️ Has the site changed over time?
  - Look at [archive.org](https://archive.org/) to see whether the domain shifted tremendously — and if so when. 
- [ ] 🗑 Did the earlier version of the site have more information? 
  - People can remove info when a site's been up for a while.
  - The "Sitemap" page is particularly useful in finding deleted pages under a domain.
- [ ] 📋 Analysis on SSL certificates
  - Find site certificate metadata including CNs and matching identities using [crt.sh](https://crt.sh/)
  - Use Censys for analyze the JARM fingerprint to detect any possible related server which exposes the site as well as find SSL metadata for IP addresses / servers [Censys](https://search.censys.io/search/language?resource=hosts&q=services.jarm.fingerprint%3A&sort=RELEVANCE&per_page=25&virtual_hosts=INCLUDE)

#### Resources & Tools

##### Books
Open Source Intelligence Techniques - Michael Bazzell
https://inteltechniques.com/book1.html

Verification Handbook - edited by Craig Silverman
https://datajournalism.com/read/handbook/verification-3

##### Website Infrastructure 
- [Blacklight](https://themarkup.org/blacklight): The Markup's real-time website privacy inspector.
- [builtwith.com](https://builtwith.com): gives you the infrastructure of the site, including IP addresses, analytics codes, tech stack, etc. Freemium model. 
- [DNSDBScout]((https://www.farsightsecurity.com/tools/dnsdb-scout/)): allows you to search and ‘flexible search’ for passive dns lookups including IP <-> domain mapping. 
- [Dnslytics](https://dnslytics.com/): offers a range of tools including [reverse Analytics](https://dnslytics.com/reverse-analytics) and [reverse DNS lookups](https://dnslytics.com/reverse-ip), as well as [WHOIS data](https://dnslytics.com/whois-lookup). Freemium. 
- [RiskIQ](https://www.riskiq.com/): a ‘threat intelligence’ tool that allows you to get reverse IP, reverse analytics, WHOIS, SSL, subdomains, etc. 
- [Whoxy](https://www.whoxy.com/): a tool that lets you see historical WHOIS registrations. Free. 
- The Internet Archive [browser extension](chrome-extension://fpnmgdkabkmnadcjpehmlllkndpkmiak/about.html).


###### Social Media Accounts 
- [Sensity AI](https://sensity.ai/deepfakes-detection/): check if an image is GAN-generated or not. Freemium. 
- [whotwi.com](https://en.whotwi.com/): create a profile-at-a-glance for any account on Twitter. Free. 
