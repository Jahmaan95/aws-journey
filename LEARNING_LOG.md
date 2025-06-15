# AWS Portfolio Project - Development Log

> **Real-time tracking of my AWS cloud infrastructure project**

## Project Overview

**Goal:** Build a full-stack web application using multiple AWS services  
**Current Phase:** Phase 1 - S3 Static Website  
**Started:** 09-06-2025 
**Status:** S3 deployment complete, moving to EC2 planning

---

## 09-06-2025 - Getting Started with AWS

**What I actually did today:**
- Set up GitHub repository structure for the project
- Created basic HTML/CSS website files (index.html, styles.css)
- Spent time figuring out how to organize the project documentation
- Started learning about AWS S3 and static website hosting

**What I learned:**
- S3 can host static websites directly (didn't know this was possible)
- Bucket names have to be globally unique across ALL AWS users
- There's a difference between S3 object URLs and website endpoints
- AWS Console is pretty overwhelming at first - so many services!

**Struggles:**
- AWS Console navigation is confusing when you're new
- Understanding the difference between public access settings
- GitHub file organization took longer than expected

**Tomorrow's plan:**
- Actually create the AWS account and try S3
- Upload my website files and see if I can get them working

---

## 15-06-2025 - First AWS Deployment Success! 🎉

**What happened:**
Got my website live on S3! Took about 2 hours total with some troubleshooting.

**The process:**
1. Created AWS account (verification took 10 minutes)
2. Found S3 in the console (easier than expected)
3. Created bucket - had to try 3 different names before finding one that wasn't taken
4. Uploaded files... and got a 404 error

**The 404 problem:**
- Error: "NoSuchKey: index.html" 
- Turns out I uploaded files to the wrong location somehow
- Had to delete and re-upload them to the bucket root
- Lesson: File location in S3 matters a lot!

**What finally worked:**
- Bucket policy for public access (copy-pasted the JSON)
- Static website hosting enabled
- Files in the right place
- Website live at: http://pranav-portfolio-2024.s3-website-us-east-1.amazonaws.com

**Honestly surprised by:**
- How fast S3 is - website loads instantly
- How much configuration is needed for something "simple"
- The bucket policy JSON is intimidating but works when you copy it exactly

**Next steps:**
- Add more pages to the site (about, projects)
- Start researching EC2 for Phase 2
- Maybe add some actual content instead of placeholder text

---

## Key Things I've Learned So Far

**About S3:**
- It's not just file storage - it's a web hosting platform
- Public access is scary but necessary for websites
- Bucket policies control who can access what
- Website endpoints are different from regular S3 URLs

**About AWS in general:**
- The console is powerful but intimidating
- Free tier is actually free for basic usage
- Each service has lots of configuration options
- Documentation is detailed but assumes you know the basics

**About project planning:**
- Breaking things into phases helps a lot
- Documentation while you learn is really valuable
- Having a clear structure makes the work feel less overwhelming

**Mistakes I made:**
- Rushed through bucket setup without reading carefully
- Uploaded files to subfolder instead of root
- Forgot to save bucket policy at first
- Didn't test the website URL format properly

**Things that went better than expected:**
- GitHub organization and documentation
- AWS account setup process
- Website actually loading and looking good
- Responsive design working on mobile

---

## What's Actually Challenging

**Technical stuff:**
- Understanding IAM and security policies
- Knowing which AWS region to choose
- Figuring out what settings actually matter vs what's just optional
- Troubleshooting when things don't work (like the 404 error)

**Conceptual stuff:**
- How all the AWS services fit together
- What's considered "best practice" vs just getting it working
- Balancing security with functionality
- Understanding cost implications of different choices

**Personal stuff:**
- Not getting overwhelmed by how much there is to learn
- Staying focused on one thing at a time instead of trying to learn everything
- Documenting without spending more time writing than doing

---

## Actual Hours Spent

**Day 1:** 3 hours
- 1 hour: GitHub setup and documentation
- 1 hour: Creating HTML/CSS files
- 1 hour: Research and planning

**Day 2:** 2.5 hours
- 0.5 hours: AWS account setup
- 1.5 hours: S3 configuration and file upload
- 0.5 hours: Troubleshooting 404 error and getting it working

**Total so far:** 5.5 hours

---

## What I Want to Learn Next

**For Phase 2 (EC2):**
- How to set up a virtual server in the cloud
- What the different instance types mean
- How to connect a frontend (S3) to a backend (EC2)
- Basic server administration and security

**General AWS concepts:**
- How services communicate with each other
- Cost management and optimization
- Security best practices
- Monitoring and logging

**Practical skills:**
- Command line interface for AWS
- Infrastructure as Code (heard this mentioned a lot)
- CI/CD for automated deployments

---

## Resources That Actually Helped

**Official AWS docs:** Good for reference but overwhelming for learning  
**YouTube tutorials:** Hit or miss, some are outdated  
**AWS Console:** Actually pretty good at explaining what each setting does  
**Trial and error:** Honestly the most educational part

**Best approach so far:** Start with something simple, get it working, then understand why it works.

---

## Random Observations

- AWS has a service for everything, but you only need a few to start
- The free tier limits are pretty generous for learning
- Error messages are usually specific enough to figure out what's wrong
- The AWS community seems helpful based on forum posts I've read
- This is definitely more complex than shared hosting, but way more powerful

**Current confidence level:** Cautiously optimistic. Got one service working, ready to try the next one.

---

**Last updated:** [Today's Date]  
**Next session planned:** [Tomorrow's Date] - Adding more content and planning EC2
