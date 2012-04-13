---
layout: post
title: "Completed move to static page hosting with Git/Jekyll/S3"
description: "AWS free tier ran out, needed a new cheap platform for my unimportant blog."
category: 
tags: [hosting, blog, ramblings, git, jekyll, s3]
---
{% include JB/setup %}
So I was running my blog on a micro EC2 instance for the last year, of course I had not added much content (a mode I now boldly proclaim will change for the better) and my AWS “free micro tier for 1 year” plan was set to run out at month's end. So I had to weigh my options:

1. Acceptance.  Pay $14 a month to Amazon, continuing comparatively massive consumption of machine resources, serving a Drupal instance whose sole purpose is to serve a few pages of my random thoughts to... eh... no one but myself.

2. Punt.  This is likely what Don Shula would do.  Just scrap it.  No one is going to read my blog anyway (save myself, skeptical that actually counts).

3. Rebel.  Find an alternative which shocks the system, something free (or near enough to free).  If this alternative should happen to in some round-about way cause me to actually learn something then great.

I went with #3 of course.  Did not take long to find some great posts about static blog hosting leveraging services such as S3 or Git.  Well, Jekyll it turns our leverages either/both so it made good sense.  I did spend a day or so puttering around with Git from my Windows 7 workstation, only to find that mostly Git for Windows 7 is provided only for hazing purposed for the newly initiated to Git.  Once I wised up and fired up a VHD running Ubuntu I was on my way... to a 2nd day of puttering.  At least day 2 of puttering involved something vaguely resembling progress so I kept fighting the good fight.  Eventually I found I could install Git/Ruby locally, stage Jekyll in a new Git repository and by leveraging Jekyll-S3 do a pretty seamless staging of my site from development to production environments.  Some outstanding tasks remaining like actually adding blog posts (this one is the re-launch if you have not yet figured that out) and finding a way to have AWS Route 53 point roge.me to the S3 bucket hosting this content (so far best I can do is a CNAME record pointing ftl.roge.me to the S3 bucket.  Anyway, it works and as noted earlier I am likely the only one who will ever read any of this.
