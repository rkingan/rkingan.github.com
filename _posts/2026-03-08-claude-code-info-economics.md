---
layout: post
title: Claude Code and the economics of personal information
---

Back in the year 2000, at the height of the dot-com boom, I was writing code and doing mathematics for a government agency, and my wife and I had two small kids at home. Back then if you were interested in developments in the tech world from the more nerdy end of the spectrum, the place to go was [slashdot.org](https://slashdot.org/) - reddit was still a few years away. You could find great, spirited discussions about new developments in technology and also fierce debates about open source software and electronic freedom.

One voice that was quoted a lot in the popular press was Michael Saylor, founder of a company called MicroStrategy. He was a tremendous proponent of the internet, and even mused at times about developing neural implants that would allow people to access the web mentally (and presumably allow the web to access people, too).

Also at that time, if you went into any bookstore or watched financial news, you couldn’t miss seeing books by, and interviews with, an author and financial advisor named Suze Orman. She expressed advice in a way that showed the link between peoples’ feelings about money and hard financial reality, and encouraged people to make more rational decisions.

Caught up in the excitement, and with some half-baked pseudo-libertarian ideas about ownership of information, I put together a pitch deck and headed off to present it at a pitch competition in the suburbs of Northern Virginia, which at the time was second only to Silicon Valley as a hub for startups. My idea was to build a personal agent. It would run on your own PC and have connectors to resources like your email, your bank and investment accounts and some health information. In the same way you might buy one of Suze Orman’s books to help you make financial decisions, or an Atkins Diet book to help you lose weight, you could buy modules that would “plug in” to your agent to provide recommendations based on your specific situation. Most importantly, all your information would stay with you. Nothing had to be shared or stored on remote servers. Think globally, compute locally.

I got to the second round in the competition and gave my pitch to some genuine VCs. They were generous and polite in their feedback, and recommended some existing startups to look at as comparators. In so many words, they told me that the idea was already being pursued. It was fun, but the idea really didn’t go further than that competition.

The thing that really surprised me, though, was what I saw when I checked out the other startups they regarded as pursuing the same idea. Every single one of them expected users to share all their personal information with the company! The very thing that I thought was the most important part of my idea, was to the VCs an incidental detail. I was confused. Did I just not get it?

Over time, I realized two things. One is that I wasn’t alone in being concerned about the way our personal data is managed. I think the most prominent voice in this area has been Tim Berners-Lee, who has been talking for years about the need for people to take back control of their information. The other, sadly, is that economics is not typically on my side. Keeping control of your information enables companies to use that information as a business asset - “if the service is free, you are the product”. It also helps companies build a “moat” that keeps you locked in because switching to a different platform is so difficult.

Now let’s talk about Claude Code and Cowork. Claude Code is, of course, an AI assistant designed to help with software development. This is an activity that even now is largely done locally on the developer’s PC, enabled by version control systems that allow each developer to maintain a separate copy of the system’s code, and to merge their changes with the main repository when done. Claude Code can be extended with plugins and skills, described in English so that they can be used by the assistant. These extensions allow the assistant to access the developer’s email, chats, project management software and other resources to gain a better understanding of the project, and also to help automate tedious reporting and documentation tasks.

Claude Cowork extends this model to tasks other than software development. It also works locally, though of course when the Claude LLM is called it involves talking to the “mothership”. Cowark also has a growing marketplace of plugins that enhance its capabilities and allow for connections to other systems.

One important thing about both of these systems: they are not, at any practical level, free. The user is the customer, not, at least as of this writing, the product.

There is a growing feeling among thought leaders that systems should be written more for agents to use, and not as much with only human interfaces in mind. I wonder, though, what will happen when this feeling comes up against the business models of the services themselves. If I have a free email account and see ads whenever I check my inbox, what happens when Claude is checking my email for me? If Claude can access details of my investments, what happens when it becomes easy for it to automate the process of moving my money to a different broker? And what will happen when Anthropic themselves feel the pressure to mine users’ data? Or to lock it up in a way that makes it hard to switch to another AI assistant?

My own opinion? I think the makers of these assistants can do the right thing and be successful if they adopt some of the information protection ideas that Berners-Lee has been talking about, and implementing. It may well be the case that some information has to be shared in order for an AI assistant to access certain services. But make that contract explicit and get the user’s approval before proceeding. This model even allows for ad-supported services. I can imagine an assistant telling the user, “I can use this free service but they would like you to see a 15-second ad before proceeding. Do you approve?” Make the user aware of exactly what is being exchanged. Make the assistant an explicit advocate for and protector of the user. After all, the user is paying the bill.

I’m just as excited about the possibility of giving people more control over their information as I was when I drove down to that pitch competition over 25 years ago. I hope we get it right this time.

**Notes**
* slashdot.org is still at it today!
<img src="/images/slashdot.jpg">
* So is [Suze Orman](https://www.suzeorman.com/)!
* So is [Michael Saylor](https://www.strategy.com/investor-relations/executive-team/michael-saylor) - now very, very, (very) much into Bitcoin.
* So is [Tim Berners-Lee](https://www.ccc.mit.edu/person/sir-tim-berners-lee/), at [inrupt.com](https://www.inrupt.com/)!