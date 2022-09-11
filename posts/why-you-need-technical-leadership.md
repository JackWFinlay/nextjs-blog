---
title: Why you need technical leadership, and what happens when you don’t have it
description: Reflections and observations from a project that went poorly.
date: '2018-12-26'
---

Sometimes projects can go very, very, badly. Most of the time there are multiple reasons. Technical leadership is one of the key things that is often missing. It can make or break a project. This is a reflection on the insights I have gained from observing, and being embedded in, both high and low performing teams.

Through exploring and reflecting on a project that went poorly, I aim to convey the reasons why technical leadership is the key point in a project’s success. Each section presents remedies for discussed issues, each brought forward from my observations garnered when observing high performing teams.

### Experience

Time is the only thing that can teach you some things. Unfortunately, experience was severely lacking on this project team.

#### Technical Leadership

This project had no technical lead or senior developers. That should be enough to tell you the direction this is going.

The team was very inexperienced. To put this in context, the people that started the project were interns, and I was still in university. There was no-one around to guide us, to teach us, to stop us falling into the pitfalls a senior developer would know about and anticipate. There was no leadership from someone who knew what they were doing. This remained throughout my entire time on the project. We simply didn’t know what we were doing was completely wrong.

#### The Intern Invasion

During one particular summer, the number of people on the project increased five-fold. The problem? They were all interns — people at the same level as the permanent staff or lower. We were already under-skilled. During this time the permanent staff were tasked with managing the interns. They were split into teams of three and we were each responsible for one team.

This was probably the hardest part of the project for me. I had experience leading developer teams during my university courses. Nothing prepared me for this though. I was now not only responsible for my own work, but that of the interns as well. They were great, talented people, but for many this was their first experience in a commercial development environment. I was lucky, my team were great. They performed well, but the result was the same; Issues that show through from inexperience, both theirs and mine.

### Tooling

The most important thing to any craftsman is their tools. Without the correct tools and tooling, it’s very difficult to produce quality work. A good team has a leader who knows their tools and can make great decisions for the project’s tooling needs.

#### Databases

In this project, we only had access to a shared database hosted on one of the slowest cloud virtual machine instances you could get. We had multiple people working on the same database, all altering views, dropping tables, and generally messing with the data at the same time. This is not an ideal way to work and certainly slowed us down.

We had no way to reproduce the database either locally or in the cloud without running a backup and restore operation. There was no way to get a clean database in the same state that we would like to deploy to different environments in. The database could only be created as a clone of our development database server. This meant that we had the lifetime of the project’s junk, including test users and data, in all of our environments.

We couldn’t and didn’t recreate the database on our local machines. This meant we had no ability to locally debug, or run in test data without polluting the shared development database. There were a few times we had to rollback to a backup of the database from the night before because someone had trashed it with a bad script. This slowed us down greatly and spread the pain amongst the whole project team.

Database migrations and updates were all manual and this meant that we had to spend time running them all against each database in turn.

The now obvious solution here is to allow developers to have a local instance of the database installed on their machines. Another solution to these kind of issues is to use a tool for migrations that make them automatic. This gives developers freedom to recreate the databases at will and to put in whatever data they want to test with.

#### Performance

Developers need and expect high performance from both their local machines, and the servers that the system is tested on. When developers are given slow tools, they move slower and take longer to produce results.

On this particular project, I was lucky in some ways. I was given one of the fastest machines of the time to develop on. This was certainly not the case for some of the other developers. Others were given the slowest machines I’ve ever seen. These things had been around for probably ten years before those poor souls got to use them. The keyboards were worn down from years of use, and the trackpad buttons had huge marks on them from having worn through the top layer of plastic.

The servers we were testing on were the same slow, bottom-tier, cloud virtual machine instances that the databases were deployed on. This made the system one of the slowest sites I’ve ever seen. Testing was a slow, arduous affair.

Resolving these issues is easy. Give your developers the equipment and resources they need. Don’t hold back on provisioning adequate resources, it’ll only slow your team down.

#### Source Control

Source control was an utter mess on this project. We used a large source control system popular in enterprises, but the software wasn’t the issue. There was no strategy in place for how we were to use it: Branches were taken off of branches ad nauseam; teams had issues merging because they all decided to work off the same branch; there just were conflicts everywhere. All of this lead to hours of gruelling merge conflict resolutions. Often we would break someone else’s work inadvertently because of bad merges, and sometimes even lose work.

For source control to be effective, you have to have a strategy and to educate your team on how to actually use it.

#### Integration and Deployment

I must warn you, the following is very disturbing.

This project had absolutely no sense of [CI/CD](https://en.wikipedia.org/wiki/CI/CD) principles or solutions anywhere near it. Deployments involved  copying the resources out of the build folder and pasting them on to the server via Remote Desktop.

If you’ve ever done this before, you know my pain. I can hear you screaming right now.

For the uninitiated: this method relies on your computer’s clipboard. If you copy anything else to your clipboard while this is in process, it will kill the upload. Anyone else on the team could connect onto the server too, killing the upload. Sometimes things also just end up getting corrupted when you transfer them in this manner 🤷‍.

The solution to these problematic deployments is using a proper CI/CD solution. This allows you to integrate code quickly, and to deploy automatically, as often as required.

### Quality Assurance

QA is one of the most important things when it comes to software development. A good QA team can spot things before the stakeholders do. They are also much more forgiving.

#### Peer reviews

Peer reviews consisted of team members sitting together, going through the work they had done. This often didn’t involve looking at code, so much was missed in the way of performance and duplication of code. The second issue was that we were all juniors or interns. We didn’t know yet what makes good code or have the ability to spot anti-patterns and common mistakes.

Senior developers know many of the issues that can arise in code and would have spotted a large number of the mistakes we were making. They are a valuable resource, especially in peer reviews.

#### Testing in showcase

We had no QA team. Testing was often not done properly by developers. The result? Testing was often completed for the first time in the showcases. This resulted in showcases that dragged on for hours as we sat there and logged every single bug our stakeholders would find.

You need a testing team to properly catch problems and validate your tasks are done properly. Developers are notorious for not testing properly.

### Code Quality

The quality of the code you put out is one of the biggest factors in a project’s success.

#### Copy-paste Culture

We had a copy-paste culture. Whenever we didn’t know how to do things, we would simply search it up on Stack Overflow. This lead to a lot of code that was mostly composed of things we could copy off the internet. This copy-paste culture lead us to producing often poor code, code that was taken out of context, not fully readable, or even properly understood by the person who copied it.

There are many different things you could say about this. This is common in a lot of projects and environments, but really shouldn’t be. Developers need to understand the code that they are copying and make it their own. Plagiarising things doesn’t pay in academia, and it doesn’t pay in software either.

#### Spaghetti Code

Our poor understanding of software architecture lead us to producing some code that was a total mess. Spaghetti code is a kind description.

Much of the code that was written was passed around many developers who each added their own flair to it. There was a mix of ideas and no cohesive style or sense of conventions. It was like a dirty pair of glasses, covered in fingerprints. Every time someone would touch it, it left a mark that made it harder to get a clear picture. Now, it’s fair to say that code will definitely be touched by many different people over the years, but this is where care needs to be taken to make sure that everything is still coherent.

We had no dependency injection framework in place and did not use any common design patterns. This lead to a lot of bad code that just began to rot as soon as it was cut. SOLID principles were something we had heard of, but never put into practice.

Code clarity is as important as getting things working correctly and the two often go hand-in-hand. Clear, consistently styled, and coherent code make for a better, more maintainable solution.

### Conclusion

A lot of the issues we faced came down to a lack of experience. We didn’t know how to set up a project properly. We didn’t know how to set up our environments correctly. We didn’t have the tools we required. There was no technical oversight. We didn’t have the knowledge we required... There was simply unchecked naïveté running abundant.

Having experience in the field of software engineering, a good technical leader would have never gotten the project into this kind of a mess. They would have foreseen the issues we faced, and headed them off before they arrived.

Projects need that knowledge that a senior developer can bring to the table. I can see the direction of the project having gone completely different, had someone set us on the right path.

This project wasn’t all bad news. I met many great people with whom I formed great bonds, sealed by these trials and tribulations. Many of these people I still regularly talk to. There were many talented people on this project, but a lack of technical leadership held back their true, real potential.