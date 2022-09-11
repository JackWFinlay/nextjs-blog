---
title: Mistakes I’ve made as a junior developer — and how you can avoid them
description: Reflections on my first years as a software developer
date: '2018-06-12'
---

When you first start out in the world of software development, things may seem daunting and unknown. Leaving university and venturing into the real world is a big step, and you will stumble many times on the path before finding your feet and confidence.

You may have confidence in your abilities already. But I ask you, “How many mistakes have you made?”

The start of a career in software development is the start of a journey in mastering your craft. As with any field, there will be challenges and chances to be correct, and chances where you can be completely wrong. This piece acts as a reflection on the mistakes I have made early in my career — and a guide to avoiding them.

### Getting the job

Landing your first job out of university isn’t always easy. Make sure it’s the right one for you.

A company has to be a good fit for you, and where you want your career to go.

#### Find out what you are worth

I made this mistake twice. When I got my first software development job during university, in my second year, I was struggling financially. This led me to accept the first salary offer I was given. I felt I needed to just take the offer, as it was great compared to the abysmal pittance I was receiving from student benefits. Little did I know that it was well under the market rate for the location, position, and time.

As I said earlier, I made this mistake twice. Upon graduating, I managed to land a job elsewhere. They were going to pay me 25% more than I was earning at the time!

It was still at the low end of the market rate. I was low-balled, and I was happy to take it. I hadn’t learned yet that not all the power is in the employer’s hands.

You too can make an offer. If I had taken the time to do some proper research, I would have seen what I was really worth. I recommend sites like [PayScale](https://www.payscale.com/) to give you an indication. You can even use sites like this as a source when negotiating.

#### Read the reviews

[Glassdoor](https://www.glassdoor.com/) is a great resource. Real employees of the companies listed have taken the effort to rate the companies they work for. Generally the reviews can be quite polarized as to whether employees have had good or bad experiences.

Search out some of each and you’ll find the middle-ground for yourself. Had I read some of these reviews earlier, I would have avoided some terrible experiences when interviewing and beyond.

#### Know what you’ll really be working with

Earlier in my career, I was so keen to work for a particular company (a friend was working there and was enjoying it) that I forgot to stop and ask what I would actually be working on. It turned out that I would not be in the same department as my friend, and that I would be on the other side of the building, and later even on different floors. And I didn’t take the time to make sure the job would really fit me.

Another side of this mistake was not asking enough about the environments, tools, and languages I would be using.

When going for the next step in my career, I made sure to ask about the following:

1.  Version control strategy and tooling
    Is it industry standard? [Git](https://git-scm.com/), [TFS](https://docs.microsoft.com/en-us/visualstudio/releasenotes/tfs2018-update2), [SVN](https://subversion.apache.org/) or [Mercurial](https://www.mercurial-scm.org/)? If you’ve heard of it, it should be okay.
2.  Is there [CI/CD](https://en.wikipedia.org/wiki/CI/CD) tooling and environments in place?
    Deployments should be as automated as possible. It’ll make your life so much easier.
3.  How often are deployments?
4.  What frameworks/languages will I be working in?
5.  What tooling do you use? Which IDE?
    [Visual Studio](https://visualstudio.microsoft.com/), Rider or [IntelliJ](https://www.jetbrains.com/idea/) are some good options.
6.  What kind of projects will I be working on?
7.  What kinds of technologies will the company be looking to use next? Also, what kind of horizon are these changes at?
    How far off are they from becoming day-to-day in use at the company?

### In the job

The challenges don’t stop once you are in the job. Every day will present some new way to challenge you.

#### Code is never self documenting

“My code is self-documenting, I don’t need comments”. 😒 I thought this when I first started programming professionally. I don’t make this mistake anymore.

Comments are the most powerful feature of any language. They can convey where your thoughts were at the time. You need to capture that in comments.

I’ve read countless sections of code where a single, simple comment would have made that complex code and the algorithms much easier to understand and update.

Commented out code is worse than no comments at all. When you are deep in investigation mode, trying to discover how something works, all that commented out code will do is make your job harder. As soon as you comment out a line, the next person to read it will have no idea why you did that.

Be judicious with your comments. Good comments will not only lighten the cognitive load, they will help you spot errors.

If something doesn’t look like it matches up to the comment, it’s probably wrong. Or it’ll give you a good chance to put the following section into practice.

#### Ask questions early

Don’t wait until you are down the wrong rabbit-hole before asking for help.

Waiting to ask for help may just lead you to the wrong conclusions, or worse, you’ll break something. Ask questions early, even if it’s just a quick Google search. Part of not asking questions when you really need to, through fear of appearing like an idiot, is how you end up building the wrong thing.

Asking questions is one of the most important things you can do to accelerate your learning, and to help get involved in projects right away. If you don’t ask questions when you need to, you may make some wrong assumptions.

#### Assume nothing

Assumptions are an important part of defining what you need to be building when you are working on a project. There will often be assumptions recorded against the tickets you’ll be working on (if your company uses a ticketing or task system).

Not every case has to be catered to when you’re designing a solution. A correct set of assumptions will help guide you towards the correct solution.

I have spent hours building things incorrectly and even building the wrong thing because I made incorrect assumptions. Usually, tasks will be quite fleshed out when they arrive from the Business Analysts, but often there will be gaps.

Don’t make any assumptions unless they have been stated for you, or you’ve asked about them.

#### Working from home

Don’t be afraid to ask to work from home every once in a while. Sometimes it’s a great way to get away from the stresses and distractions of the office and really focus. There are whole companies built on a [remote workforce](https://github.com/yanirs/established-remote). It certainly works.

There will also be some companies that are fully against it. I worked for over a year with a team in Australia, from our office in New Zealand. Collaboration and cooperation still happened online. Through email, chat, and old fashioned phone calls, distance doesn’t stop you working with your peers. There was no practical difference whether I was in the office or at home, but I was forced to be at the office anyway.

Look out for the opportunity to spend the day working from home or somewhere different wherever possible.

#### Time actually programming

Unfortunately, you will not be programming 100% of your week. As much as this may pain you, it’s not all bad. Programming isn’t 100% code anyway.

Much of your time will be spent in meetings, usually to the point of reducing the amount of time you need to spend programming. This comes through making sure that you are writing the minimum amount of code possible to engineer the best possible solution.

### Outside the job

Some say that it doesn’t really matter, but others say that what you do outside the job is just as important as what you do in the job.

#### Programming on your own time

Once I realized the crushing reality of how terrible proprietary tooling and languages really are, I started to work on skills that I knew would be transferable to another company.

If you find yourself stuck in the same type of environment, knowing a few things about more mainstream technologies will help you in finding your way out. It’s a polarizing opinion, but I believe that time spent on career development in your own time has a great effect on the opportunities you will become open to.

#### Read

Now I have made my way through a few, I wish I had picked up some more books earlier. There are countless things to learn from books. Grab a few and read them on your downtime, at the office, or on your way there. Most people I know have some kind of commute, and it’s a great way to pass the time.

#### Write

Writing can be a great way to further your career. That’s what I’m attempting here. This isn’t just an advice piece, it’s a reflection. A good blog can also help you when you face a particular issue you may have faced before. If you keep a log of what has challenged you, it may just come to your rescue.

It may seem strange at first, but writing things down is a great way to decompress and exhale after stress. I make (most of) my writings public, but you don’t have to. Half of my posts are still sitting in the drafts folder.

#### Exercise

For the first few years of my career I didn’t regularly exercise and it certainly caught up to me. As a programmer, most of your day will be spent sitting, generally inactive, staring at a screen. You will not get to program all day, sure, but between meetings and time at your desk, you won’t be moving much. Try to exercise as much as you are capable of.

#### Taking some time off

As important as it is to be available all the time for work, it’s also important to take some time off every now and then. If you are not saving up for a big holiday, it’s sometimes nice to just make long weekends extra long, or take a few days off here and there. Many countries provide a varying number of guaranteed weeks of leave. Make sure to take advantage of this wherever possible.

I made the mistake of saving up as many leave days as possible and getting burned out in the process. It was a good decision financially, but not for my mental and physical well-being.

___

### Thanks for reading!

I hope this reflection of my first years of programming professionally provides some insight into where you may head in your career. This has been an interesting reflection for me, and I hope you can take something from it.