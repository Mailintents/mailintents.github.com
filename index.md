# Mail Intents
Enabling push-based API for the universal interface with humans as endpoints - email.

* or making transaction mail suck less.
* or because even bacn becomes trite.
* or netizens for a meaningful inbox.
* or your own personal webhooks.

## Why?

You hear the cries of "email is broken" repeating every few years, but at its core, email is pretty great. It's the largest social network, humans are the nodes, and it supports push-messaging. But ask any Internet user - most hate the cognitive load of a never-empty inbox.

Email should be smarter. Computers should do more things for us without so much micromanagement.

## How?
This proposal is in a very early stage, and it's mostly about identifying a pain point. But at a high level, Mail Intents implements a small amount of metadata on email messages to give mail agents hints about the meaning of the email so that they can perform rich, useful actions based on the messages.

## Stories

I book a flight and receive a confirmation in my email. My mail client sees that it includes the receipt intent, and adds the transaction to my banking software so that I can reconcile it later. It also sees the travel intent and adds my travel time to my calendar - private, of course, but I can go in later and share it with others if I choose.

I go to my doctor's office with a sore throat and end up getting some bloodwork done. When I leave the office, I can get a discharge summary, listing the examinations and the labs that were ordered, along with anything else that was added to my patient chart. If my email address supports S/MIME secure communications, I can receive the results directly in my email with a Continuity of Care Document and maybe an Invoice intent attached. Otherwise, for privacy, I can receive a Notification intent forwarding me to a secure message website where I can access and download this information. If I have a sophisticated enough mail agent, this process can be done automatically, preserving my privayc thorugh secure encryption while still providing me convenient access to the data I Care about. Next, a few days later, I receive another email, this time with the results of the lab. As a result of all of this, my medical details automatically appear in my Personal Health Record (which is acting as another mail agent, after all) and the financial details end up in my checking account summary.

So, I buy a lot on Amazon. I end up with a lot of transactional email. Once when I first order it. Another when my package is sent. Maybe another when there's a shipping exception - like it can't be delivered because there's a hurricaine or something. Lastly, there's the email when it's delivered. My mail agent can manage this better than I can. The receipt can go into my ledger, the and the package tracking ID can be sent to my phone so I can compulsively keep tabs on my inbound goodies. The thing is, I do care about this information - I just don't want it in my inbox. I'm glad my mail agent is smart enough to know what to do with these emails so I don't have to think about it.

The other day I signed up for an account on a website. I shouldn't have to do this anymore, but there it was: A signup form with fields for email, a confirmation of my email, and a password. Dutifully, I filled it out and hit the signup up button. "Great! Your account has been created. Check your email to confirm your address." Wait, what? I already confirmed it in the field labeled "confirm your email." Thankfully, the confirmation email was sent with a Confirmation intent, and my mail client - expecting this email after having received a Confirmation Web Intent - was able to intercept it before reaching my eyes and complete the confirmation process on my behalf, saving me at least that much hassle.

Once I had the bright idea of watching a GitHub repository for a popular open source project. This was great! I could follow along with the day-to-day development of a project I used heavily. Unfortunately, this also generated a large volume of notification email. Frustrated, I turned off email notifications, instead opting for on-site notifications only. If an inbox was going to be cluttered with this torrent of notifications, it would at least be scoped just to one service, rather than my email, my universal inbox. Entitled millennial that I am, I immediately turned to Twitter to lament the lack of a daily digest version of these notifications. However, since the notifications were being sent with Notification intents, with the resource specified as the repository URI, I realized I could create this functionality myself. I added a rule to hide these email form my inbox and hacked a quick map-reduce script for my mail agent to generate the digest - and set it to run daily.

## Get Involved

Star the [repository](https://github.com/Mailintents/mailintents.github.com) on github. Follow [@mailintents](https://twitter.com/mailintents) on Twitter. Propose implemntations, elaborate on use cases, pitch the idea to mail agent manufacturers and transational email processors.