### Who’s behind this website? A Checklist. 
​
Strong recommendation: while running through this checklist, create a data diary — it can be a TextEdit doc, a Google Doc, just the Notes app, whatever. 
​
#### Site Content
​
##### Text
- Are there any authors listed? 
- Are there any e-mail addresses or contact information? 
  - If there are e-mail addresses, do those share the domain with the website?
- Has the website been archived?
  - use archive.org 
- What’s the server’s local time?
  - use TKTKTK
- Does the website have a privacy policy or terms and conditions that mentions an LLC?
- Does the website have an RSS feed?
  - Does the RSS feed give any additional information about authors / stories that aren't visible on the site? 
​
##### Features and functionality 
- Does the website have a newsletter? 
  - Check for the physical postal address — required by the CAN-SPAM Act in the US
- Does the website collect donations? 
- Does the website have an e-commerce store? Or, does it sell products? 
​
##### Links
- What domains does the website link to most? (Requires scraping)
- Who links to the domain most often? 
  - Check backlinks on ahrefs.com
- Do the links have UTM codes? 
​
##### Photos, images and documents
- Are there author photos? 
  - Use reverse image search to see if the same images appear elsewhere
  - Check sensity.ai to see if the image is GAN-generated 
  - Read more about spotting GAN-generated images [here](https://www.theguardian.com/technology/2020/jan/13/what-are-deepfakes-and-how-can-you-spot-them).  
- Do the images have EXIF data?
- Do the images have any other identifying information? 
  - Run through the list [here](https://themarkup.org/ask-the-markup/2020/03/12/photos-privacy)
- Where are the images hosted?
  - If on AWS S3, the bucket name can be revealing — or you might find the bucket isn’t secure. 
- Are there PDFs hosted on the site? 
  - On a search engine, filetype:pdf site:<your\_domain.com>
​
#### Social Media
​
If there are any social media profiles mentioned on the site, they are worth investigating. 
​
- Are there any social media accounts in the <meta> section of the HTML? 
- When were the individual accounts created? Does it line up with the site history?
- What platform has the biggest reach?
- Is the messaging different across platforms? 
- Do they have completely distinct account names across social media platforms or are they more-or-less the same? 
  - Note: just because you find the same account name across platforms doesn’t necessarily mean they belong to the same person! 
​
##### Facebook
On the Facebook profile, go to Page Transparency:
- Is there an address and phone number for the page?
- Does the page history reveal a different name? 
  - Has the page shifted topics? 
- When was the Facebook page created?
- Is the page running any groups? 
- Has the page run any ads? Has the page run political ads? 
​
- Does Facebook flag any ‘related pages’ for the given page? Rely on Facebook’s algorithms to find connections! 
​
##### Twitter
On Twitter, the account might be part of a pod or network that boosts each other. Using whotwi.com, it’s worth checking:
- Who the account is engaging with?
- What are the account’s tweeting patterns? 
- What hashtags are associated with the account? 
​
#### Infrastructure 
​
- Have you saved down the website? 
  - you can do this on archive.org
  - you can grab the whole website on Terminal with `wget`: `wget -mpEk <yourwebsite.com>`
​
- What is the website using? 
  - Is it using Wordpress, Squarespace, something else?
​
- Where is it hosted? 
  - Is it on Google Cloud, AWS, Cloudflare, something else? 
​
- Are there any trackers present? 
  - You can check [Blacklight](https://themarkup.org/blacklight) to begin with. 
​
- How is the site monetised? 
  - Are there any affiliate links? 
​
- What are the various tracking identifiers, and are those shared with other domains?
  - Check Google Analytics, Facebook Pixel, Quantcast, NewRelic, etc. 
  - Use tools like builtwith, RiskIQ, or Dnslytics to see if other domains share the same ID. 
​
- Are there any relevant subdomains? 
  - Use Farsight Security DNSDBScout Flexible.
​
- Are there historic WHOIS records? 
  - Look at Whoxy or RiskIQ. 
​
- Has the site changed over time?
  - Look at archive.org to see whether the domain's shifted tremendously — and if so when. 
​
- Did the earlier version of the site have more information? 
  - People can remove info when a site's been up for a while. 