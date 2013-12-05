---
layout: post
published: false
title: "Programmer's Thoughts on Healthcare.gov"
category: politics
author: Leo Liu
displaydate: "2013-12-05"
date: "2013-12-05"
tags: 
  - student
---

![](/assets/test2.png)
![image.jpg](/assets/image.jpg)
![](/assets/image.jpg)
Healthcare.gov is a mess. When the site first launched on October 1, it was totally unusable. Today, the site still doesn’t work. One user spent several hours a day for a whole month repeatedly trying to sign up for healthcare. The exact problems he encountered on the site before finally succeeding are chronicled [here](http://www.cnbc.com/id/101171790). One of the technical leaders of the project [just resigned](http://www.washingtonpost.com/blogs/wonkblog/wp/2013/11/06/healthcare-govs-head-tech-guy-is-out/), and officials are [currently testifying](http://online.wsj.com/news/articles/SB10001424052702303309504579181763508216406) in Congress about the site’s issues. As a computer programmer, this problem interests me.

Healthcare.gov is a key piece of Obamacare, which Congress passed in 2010. The site allows users to shop for new health insurance plans. Several contracting firms, including the CGI Group, Experian, and Quality Software Services, built different parts of the website, but the entire list of firms has not been published. The total cost of the contracts ballooned to [$292 million](http://uk.reuters.com/article/2013/10/17/uk-usa-healthcare-technology-insight-idUKBRE99G06120131017). How could a site that cost so much not work?

I know what it takes to make a website. I have interned at a large web company, worked on code for websites, and studied software systems in class. I am confident that healthcare.gov doesn’t involve the types of challenges faced by other popular websites like Google, Facebook, or Twitter. Unlike those sites, healthcare.gov doesn’t need to be ultra-fast. It doesn’t need to support nearly as much traffic (and there are simple ways of scaling up the site as needed). It doesn’t involve any new or complex technology like a custom storage system or complicated application. The site could have easily been made ten years ago; the same technology existed back then.

Several non-technological factors do make the site challenging to implement. The site deals with patient medical records and coordinates between thousands of systems, both public and private (i.e. government systems and those of every insurance company). Each insurance company might require different types of information in different formats, and there may be different plans with identical names. Even so, the site should have been designed in such a way that the complexity could be incrementally added to the site. The complexity of insurance information also doesn’t explain many of the _usability_ problems on the site, including:
- crashes and long load times
- displaying empty drop-down menus when choosing security questions
- errors incorrectly stating that not enough security questions were answered
- errors incorrectly stating that uploaded files exceeded some limit
- pages not loading
- missing text and links
- inability to update basic contact information
- random text appearing on the site

Finally, the site should have been thoroughly tested before release. Developers should not have released features that they knew would fail. They should have informed the public of issues in a timely manner, rather than letting users discover the issues themselves. Doing so would go a long way in reducing user frustration.

Then there’s the price: $292 million just for 6-8 months of contracted labor. If an average software engineer makes $100,000 per year, then $292 million can pay for 8 months of work from 4,000 engineers. There’s no way that the site required that many engineers. The firms must have overcharged, which they always do, even though the government used a bidding process to get the cheapest price. Also, the main contracting firm, CGI Group, did not have a proven record of success. In 2012, Canada canceled a $46 million contract for CGI Group to build an electronic diabetes registry because the firm had missed several deadlines. Between 1999 and 2011, CGI Group received $87 million to develop Hawaii’s online tax system, which never worked properly. Hawaii officials plan to spend $32 million to rebuild it. Even now, CGI Group’s problems are not limited to the federal healthcare exchange. Vermont’s state health care exchange, implemented by CGI Group, is experiencing similar problems.

Although the government is [throwing more people at the project](http://www.bloomberg.com/news/2013-10-31/google-oracle-workers-enlisted-for-obamacare-tech-surge-.html) to fix it before December, I doubt that they’ll succeed by then. In software engineering, there is a concept called the Mythical Man Month, which states that adding more people to a late project will only delay it further because it takes too much time to get those new people up to speed.

If I were in charge, I would have done this project differently in two ways:

(1) Do away with all the firms. Form a small group of talented technical leads and recruiters. Recruit the highest-qualified college students and individual contractors (not entire firms) to implement the site. It is better if there aren’t too many groups each working on different parts of the system. Otherwise, nobody will understand the entire system, and there will be many problems when integrating all the different parts. Doing away with the money-hungry firms would also save a lot of money. Finally, the website would be better overall because the recruiting process vets over each individual programmer, rather than trusting the firms to supply their own programmers.

(2) Since the website is not a trade secret or part of a for-profit enterprise, make the entire codebase open-source so that outside programmers can read the code and submit fixes. (Having too many programmers is undesirable only in the initial stages of a project. Once the design is fleshed out and mostly implemented, exposing the code to the masses is beneficial. Open-sourcing also doesn’t suffer from the Mythical Man Month because outside programmers get up to speed on their own time). The outside programmers might even complete a significant portion of the work. This approach is proven to work; take Linux as an example. Linux is an open-source operating system and one of the most complex types of software that exists. It’s mostly written and maintained by volunteers, and most importantly, it works. It’s not too late to open-source the code.

As an added benefit, open-sourcing the code would allow others to audit the code for security flaws. There’s already one [known flaw in the site that allows one person to view others’ private information](http://blog.heritage.org/2013/11/02/exclusive-healthcare-gov-users-warn-of-security-risk-breach-of-privacy/). Making a site secure is generally harder than making it work. If the firms haven’t even been able to do the latter, then security flaws are no surprise. Even the best-written programs will have security holes; the best way to deal with them is to make the code available for public analysis.

Healthcare.gov needs to be fixed soon. There are people who cannot get the care they need because they cannot use the site to sign up for healthcare plans. It remains to be seen whether the government is competent enough to fix the myriad of software issues.