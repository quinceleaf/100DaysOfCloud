## Introduction

I've been busy working every day with the skills I've learned so far with AWS, but I've slipped (again) keeping up with posting my progress (3 weeks since my last post? no way!!!), so time to get back on track on the [#100DaysOfCloud](https://www.100daysofcloud.com/) journey.

Most of my time has been spent on (2) cloud-related projects:

### CloudCalendar

I've been developing an event listing/calendar service for cloud learning events – between the CSPs and the larger ecosystem of vendors, learning sites and learner communities, there is a constant flood of new webcasts, Twitch broadcasts, virtual conferences, podcasts and other valuable resources.

My biggest challenge is finding out about them: sometimes I stumble across announcements in my Twitter or LinkedIn feeds, sometimes others on the [#100DaysOfCloud Discord](https://discord.com/channels/728717915028717670/732081353285304412) server re-post event links, but many I only discover days or months after the fact on YouTube.

So I've built an app using [Next.js](https://nextjs.org/) and the sublime [React Query](https://react-query.tanstack.com/) on the frontend and AWS's [API Gateway](https://aws.amazon.com/api-gateway/), [Lambda](https://aws.amazon.com/lambda/) and [DynamoDB](https://aws.amazon.com/dynamodb/) for the backend. On this app I'm aiming to post upcoming events, and have it available as a resource for other cloud learners to visit to find links to upcoming (and past) events, searchable by keywords and tags.

I'm looking into how I can incorporate what I've already done into the #100DaysOfCloud website. The biggest challenge will be incorporating Cognito and switching away from React Query to SWR. That'll be the hardest – RQ is an amazing library!

### Manufacturing Execution System

Currently starting an exciting project to develop a SaaS **manufacturing execution system** (MES), initially for a foodservice manufacturer that operates on both the wholesale and retail levels in New York and the surrounding New England/mid-Atlantic region.

This is similar to other projects I've done in the past, but a little broader in the overall functionality it will have to cover.

- for previous projects, I've used [Django](https://www.djangoproject.com/) and [MySQL](https://www.mysql.com/) atop [DigitalOcean](https://www.digitalocean.com/). I have nothing but love for all three - they work very well together! For this project, however, I'm looking to expand upon the learning from my AWS certifications and make this a serverless application.

Spent today modeling the data access patterns for DynamoDB for this project (still deciding if DDB will be appropriate in the long run for this), and working up a mock dataset.

### Courses

Also starting (2) new course sequences. I'm a big fan of quality MOOCs (I completed the MITx MicroMaster's in Supply Chain Management back in March), and am looking forward to working through these two before turning to machine learning and data analytics at the turn of the year:

- [**Algorithms** specialization](https://www.coursera.org/specializations/algorithms), with Tim Roughgarden (Stanford) on Coursera

- [**Introduction to Discrete Mathematics for Computer Science** specialization](https://www.coursera.org/specializations/discrete-mathematics), with Alexander Kulikov (UC San Diego) on Coursera

## Next Steps

- working further on the MES project

## Resources

- [React Query](https://react-query.tanstack.com/)
- [Next.js](https://nextjs.org/)
- [Algorithms specialization](https://www.coursera.org/specializations/algorithms), with Tim Roughgarden (Stanford) on Coursera
- [Introduction to Discrete Mathematics for Computer Science specialization](https://www.coursera.org/specializations/discrete-mathematics)

## Social Proof

### Twitter

[Day 19/100](https://twitter.com/quinceleaf/status/1311544835925516290)

### LinkedIn

[Day 19/100](https://www.linkedin.com/feed/update/urn:li:activity:6717322113126166528/)
