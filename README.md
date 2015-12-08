# missing-internet-specs
Missing Internet Specifications

Here is a list of ideas. Each idea is about a internet standard that I am missing.

I love feedback: Please create a github issue if you see typos or if something is not clear. Don't be shy. Tell me what you think.

## Avatar: mail address to image
Use case: Mail user agents like thunderbird or outlook should be able to display the image of a emai sender.

If you get a mail from foo.bar@example.com there should be a way to receive the image and maybe more information.

I asked this at stackoverflow: http://stackoverflow.com/questions/34043435/rfc-for-retrieving-avatar-image-from-email-address

One of several possible solutions: I think DNS could be used. DNS should provide an URL to an image.

## Mail Header for online shopping

Use case: If you buy stuff via internet you get several mails. Some users (like me) want to move these mails to sub-folders.


The most common types are these:

  * "We received your order"
  * "This is your invoice"
  * "We are shipping your goods"

It would be very nice if there would be a standard for tagging the mails.
Then users can create mail filters to move mails to sub-folders.

Spec: https://en.wikipedia.org/wiki/Email#Message_header

## HTTP PUT without data transfer, since hash of data is known to server

See http://stackoverflow.com/questions/32794863/http-spec-put-without-data-transfer-since-hash-of-data-is-known-to-server

## Make notes on Mails (IMAP)

Use case: I see a mail from a friend in my inbox. But some information is missing. I call him on the phone. He tells me more details. The next step is that I need to do something. But not today, in about one week. I want to add a note to the mail.

I use thunderbird on PC and K9 on android. Notes should be visible on both devices.

One of several solutions: Extend IMAP Spec

Related: http://softwarerecs.stackexchange.com/questions/27065/create-and-store-notes-on-mails



