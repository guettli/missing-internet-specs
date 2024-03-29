# Missing Internet Specifications


Here is a list of ideas. Each idea is about a internet standard that I am missing.

For things which would require an agreement/specification see Missing Internet Specs.

> The Internet is not a network of computers. It is a network of people. That is its real strength. 

For a list of things which could be solved in a particular application see [Not Solved Yet](https://github.com/guettli/not-solved-yet)

***

## Feedback

I love feedback: Don't be shy. Tell me what you think.

 * You are missing an internet standard which is not listed here? Which one? Just create a github issue
 * Your think I am talking nonsense? Just leave a github issue. What needs improvement?
 * You like an idea? Just leave a github issue. 
 * You found a small typo? Just leave a github issue.
 * You like the idea and would like to help? Just leave a github issue.
 
***
## Preface

What is a "standard" in this context? For me a standard is "rough consensus and working code".

I don't need an official RFC. I just want several products to aggree on a way to exchange data.


## HTML: Copy+Paste (including images)

You can copy+paste html (including images) from a public page.

But you images will be missing if the page requires you to login.

I can't believe that this is not fixed in the year 2022.

Related: https://webapps.stackexchange.com/questions/163964/how-to-copy-and-paste-html-including-images-to-google-docs

There is a work-around: First save the page locally (select "whole page" or something like this). Then open the local html file. There you can select and copy+paste the images. I hope this work-around will be not needed in some years.

## From mail address to profile (image, homepage, ...)

Use case: Mail user agents like thunderbird or outlook should be able to display the image of a emai sender.

If you get a mail from foo.bar@example.com there should be a way to receive the image and maybe more information.

I asked this at stackoverflow: http://stackoverflow.com/questions/34043435/rfc-for-retrieving-avatar-image-from-email-address

One of several possible solutions: I think DNS could be used. DNS should provide an URL to an image.

A simple solution could look like this: If a user has the address `foo@example.com`, then his profile URL is `https://example.com/~foo`. This can be a html page created from user "foo". Other URLs should get defined. For example `https://example.com/~foo/profile.jpg` with a profile picture of the user.

"tilde strikes back": I you have used the internet in the years 1996-2000, then you have seen this URL pattern before :-)

... or use [RFC8615 /.well-known/ URLs](https://en.wikipedia.org/wiki/List_of_/.well-known/_services_offered_by_webservers)

## Mail: Creating groups, easy like in WhatsApp

Creating a new group for email communication should be as easy as in
WhatsApp.

## Mail: IMAP/SMTP

The following mail issues might be solved by [JMAP](https://github.com/jmapio/jmap)

### Store Metadata on Mails (IMAP)


Use case: I see a mail from a friend in my inbox. But some information is missing. I call him on the phone. He tells me more details. The next step is that I need to do something. But not today, in about one week. I want to add a note to the mail.

Since I use several mail-user-agents (thunderbird on PC and K9 on android) not proprietary solution helps. Notes should be visible on all devices.

One of several solutions: Extend IMAP Spec

Related: http://softwarerecs.stackexchange.com/questions/27065/create-and-store-notes-on-mails

My question in K9 (Android Mail App) forum: https://groups.google.com/forum/#!topic/k-9-mail/fvu3DRdwDic

StackO question "Storing additional data to mail in IMAP": http://stackoverflow.com/questions/41757915/storing-additional-data-to-mail-in-imap


### Recall a sent mail

Even if you carefully read a mail twice before sending it. From time to time you make a mistake and you want
to recall the sent message. All modern communication platforms have this feature.

### One connection to receive and send mails, not two

There are two protocols to handle email with a mail user agent (thunderbird, K9 on android, ...):

 * IMAP for receiving/storing
 * SMTP for sending
 
Why two protocols? It makes setting up a new mail user agent much more complicated. There is no reason (except "historical reason") for two protocols. 

I guess mail server want "talk" SMTP in the future. OK, I don't want to change that. But sending via IMAP would make a lot of things simpler.

It would be nice if https would get used instead an own protocol.

### Create hyperlink to particular mail

UseCase: We have a shared Mail folder and a wiki in our company. A client sent several important documents via email. I want to create a link from the wiki to that particular mail. AFAIK there is not default and simple way. That's really sad.

I am unsure with JMAP does help here.

### Edit Mail Filter Rules

Sieve is a programming language that can be used for email filtering. See https://en.wikipedia.org/wiki/Sieve_%28mail_filtering_language%29

But AFAIK there is not wide spread use of it, since there is no standard way to update a sieve script.

There is a RFC to manage sieve scripts, but it is a new client/server protocol which needs authentication again. See https://tools.ietf.org/html/rfc5804


Updating these rules via https would be great.

### Snooze Mails

gmail and fastmail have a "snooze" feature. But up to now there is no spec which allows a vendor neutral implementation.

Dialog started: [JMAP extension: Snooze Mails](https://github.com/jmapio/jmap/issues/301)


See http://stackoverflow.com/questions/32794863/http-spec-put-without-data-transfer-since-hash-of-data-is-known-to-server

***

## HTTP client-side creation of ETag

Imagine I downloaded foo.tgz from `http://example.com/foo.tgz` some days ago. Now I want to know: Do I need to fetch a new
version?

AFAIK there is no way that a http client can validate that. Except the client stored the etag somewhere.

It would save a lot of bandwith if there was a way to solve the question.

Then a http client could send to the browser something like this:

> I data with hash-sum ... from URL http://example.com/foo.tgz
> Is this still the current version?

The http server could reply with "yes, that's the current version" or "no, I have hash-sum ...".

Of course client and server need to agree on a hashing algorithm. But this is not a huge problem.


## HTTP PUT without data transfer, since hash of data is known to server

The tool rsync can sync directories quickly, since only changed files get transfered. It would be great to have rsync like protocol which works over http.

Up to now DropBox, Nextcloud, Owncloud, Microsoft OneDrive, Google Drive all use their custom protocol.

***
## Alternative zu CSV

[CSV](https://en.wikipedia.org/wiki/Comma-separated_values) is very estalished. A lot of time gets wasted by a lot of people every day because CSV has several weaknesses.

JSON/YAML/XML are not an alternative since CSV is a tabular format.

Please tell me, if you know an alternative.

***
## Mail Header for online shopping

Use case: If you buy stuff via internet you get several mails. Some users (like me) want to move these mails to sub-folders.


The most common types are these:

  * "We received your order"
  * "This is your invoice"
  * "We are shipping your goods"

It would be very nice if there would be a standard for tagging the mails.
Then users can create mail filters to move mails to sub-folders.

Spec: https://en.wikipedia.org/wiki/Email#Message_header

***
## SVG
[Multiline Text](https://stackoverflow.com/questions/58750651/multiline-text-in-svg)

***
## JavaScript / JSON

[Let's fix JavaScript and JSON](https://github.com/guettli/lets-fix-js)

# No Unicode Symbol for "Share Icon"

There is not Unicode Symbol for the "Share Icon" yet.

https://stackoverflow.com/questions/23358594/is-there-a-unicode-character-for-the-share-icon

