# missing-internet-specs
Missing Internet Specifications

Here is a list of ideas. Each idea is about a internet standard that I am missing.

> The Internet is not a network of computers. It is a network of people. That is its real strength. 

## Feedback

I love feedback: Don't be shy. Tell me what you think.

 * You are missing an internet standard which is not listed here? Which one? Just create a github issue
 * Your think I am talking nonsense? Just leave a github issue. What needs improvement?
 * You like an idea? Just leave a github issue. 
 * You found a small typo? Just leave a github issue.
 * You like the idea and would like to help? Just leave a github issue.
 
## Preface

What is a "standard" in this context? For me a standard is "rough consensus and working code".

I don't need an official RFC. I just want several products to aggree on a way to exchange data.

## Roadmap

2016:
  * Brainstorming

2017:
 * Concentrating on one or two items. 
 * Talking to experts in this domain.
 
2018: 
 * If enough positive feedback was received: Implement the idea by patching an open source client and server
 * Talk to other client/server vendors.

2019:
  * If enough positive feedback was received: Use the patched client and server.
  * Write a RFC
  * Talk to other client/server vendors (promote RFC).

## Avatar: mail address to image
Use case: Mail user agents like thunderbird or outlook should be able to display the image of a emai sender.

If you get a mail from foo.bar@example.com there should be a way to receive the image and maybe more information.

I asked this at stackoverflow: http://stackoverflow.com/questions/34043435/rfc-for-retrieving-avatar-image-from-email-address

One of several possible solutions: I think DNS could be used. DNS should provide an URL to an image.

> Why not use gravatar.com?

 * Gravatar is a service, not a standard.
 * It is like a single point of failure. 
 * You can't set up an own server

## 43-Folder for IMAP

I like the tickler file system (aka 43-folder) to organize things. I would love to do this for mails, too. I want mails to able to move mails into the future. They should reappear N days later.

More about "tickler file": https://en.wikipedia.org/wiki/Tickler_file

My question in the mail-in-a-box forum: https://discourse.mailinabox.email/t/snooze-feature-like-google-inbox/1790

My question in the k9 (android IMAP client) forum: https://github.com/k9mail/k-9/issues/1842


## Make notes on Mails (IMAP)

Use case: I see a mail from a friend in my inbox. But some information is missing. I call him on the phone. He tells me more details. The next step is that I need to do something. But not today, in about one week. I want to add a note to the mail.

I use thunderbird on PC and K9 on android. Notes should be visible on both devices.

One of several solutions: Extend IMAP Spec

Related: http://softwarerecs.stackexchange.com/questions/27065/create-and-store-notes-on-mails

My question in K9 (Android Mail App) forum: https://groups.google.com/forum/#!topic/k-9-mail/fvu3DRdwDic


## One connection to receive and send mails, not two

There are two protocols to handle email with a mail user agent (thunderbird, K9 on android, ...):

 * IMAP for receiving/storing
 * SMTP for sending
 
Why two protocols? It makes setting up a new mail user agent much more complicated. There is no reason (except "historical reason") for two protocols. 

I guess mail server want "talk" SMTP in the future. OK, I don't want to change that. But sending via IMAP would make a lot of things simpler.



## Edit Mail Filter Rules via IMAP
Sieve is a programming language that can be used for email filtering. See https://en.wikipedia.org/wiki/Sieve_%28mail_filtering_language%29

But AFAIK there is not wide spread use of it, since there is no standard way to update a sieve script.

There is a RFC to manage sieve scripts, but it is a new client/server protocol which needs authentication again. See https://tools.ietf.org/html/rfc5804

Why not handle this via **one** connection?


## HTTP PUT without data transfer, since hash of data is known to server

See http://stackoverflow.com/questions/32794863/http-spec-put-without-data-transfer-since-hash-of-data-is-known-to-server



## Mail Header for online shopping

Use case: If you buy stuff via internet you get several mails. Some users (like me) want to move these mails to sub-folders.


The most common types are these:

  * "We received your order"
  * "This is your invoice"
  * "We are shipping your goods"

It would be very nice if there would be a standard for tagging the mails.
Then users can create mail filters to move mails to sub-folders.

Spec: https://en.wikipedia.org/wiki/Email#Message_header
