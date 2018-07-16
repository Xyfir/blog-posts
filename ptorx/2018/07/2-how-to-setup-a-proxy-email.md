This guide will offer two separate ways to create proxy emails that allow you to anonymously send and receive mail: an easy way; and a not-so-easy, developers-only way for those who want to do most of the work themselves. Confused as to what exactly a proxy email is? See the previous guide: **[What is a proxy email?](/blog/ptorx/2018/07/1-what-is-a-proxy-email)**

# The hard way via [MailGun](https://www.mailgun.com)

If you insist on the hard way, you should either _be_, or _hire_ a developer.

1.  Create an account on MailGun, link your credit card, and all that stuff.
2.  Go to `Domains` and click `Add New Domain`.
3.  Follow the instructions through the whole process of setting DNS records for verifying your domain.
4.  Go to `Routes` and click `Create Route`
5.  Under `Expression Type` select `Match Recepient`
6.  For `Recepient` enter in the address you want for your proxy email: `proxy@your-domain.com`.
7.  Under `Actions`, tick the checkbox for `Forward`, and put your _real_ email address in the text box.
8.  Still under `Actions`, tick the checkbox for `Stop`.
9.  Give your route a description.

Now you have a single proxy email that will redirect mail to your real email address and _that's all it will do_. For anything else, you really want (and in some cases _need_) to custom build a site interface and server since MailGun really wasn't built for this sort of thing, and you'll just be fighting MailGun's interface trying to view your mail or create a proxy email. That being said, if you decide to put in the time and money for a custom solution you _will_ be able to do just about anything you want when it comes to emails.

# The easy way via [Ptorx](https://ptorx.com?r=source~blog-2)

This is simple, I promise.

1.  Create a [Ptorx](https://ptorx.com?r=source~blog-2) account.
2.  Click the `+` button at the top right of the app.
3.  Under the `Create a new:` menu click `Email (Instant)`.

That's it. You now have a proxy email that will redirect incoming mail to the email address you created your Ptorx account with.

By choosing the `(Instant)` option you skipped over a lot of optional configuration, so there are more advanced features available if you're interested. We'll glance over those advanced features here, but if you want more detailed explanations you should look no further than Ptorx's [Help Docs](https://ptorx.com/docs/help).

1.  Click the `+` button at the top right of the app (again).
2.  In the `Create a new:` menu click `Email (Custom)`.
3.  Configure things however you want. Don't worry, everything's optional. Go ahead and skip to step 4 if you want.
4.  Click `Create`.

That wasn't very helpful (unless you skipped #3), so let's go over the things you can configure:

- `Name` / `Description`: Hopefully self-explanatory, a name and description for your new proxy email. This is just to make your life easier for when you have dozens or hundreds or thousands of proxy emails and are trying to search through all of them.
- `Address`: This is the _**`address`**_`@domain.com` part of your proxy email address. Set this to whatever you want, or leave it blank and get a random English word followed by some random numbers if you're indecisive or just don't care.
- `Domain`: This is the `address@`**_`domain.com`_** part of your proxy email address. Probably your only option is `ptorx.com` so there's not much you can do here. However, if you've added a domain to your account or were given access to another user's domain, you can select it here.
- `Redirect To`: The _real_ email address that your _proxy_ email address will redirect (allowed) incoming mail to.
- `Spam Filter`: When enabled, any mail Ptorx thinks is spam will be ignored and not redirected.
- `Save Mail`: When enabled, mail will be _temporarily_ stored on Ptorx's servers for you to access at some point in the near future from your proxy email's inbox within the Ptorx app.
- `No Redirect`: Tells Ptorx to ignore `Redirect To` and not actually redirect any mail to it.
- `Direct Forward`: Forwards incoming mail directly to your real email from the original sender and _not_ from your proxy email. Read the docs for this one!
- `Filters`: Create whitelists or blacklists to ignore unwanted mail and prevent it from being redirected to you.
- `Modifiers`: Modify (allowed) incoming mail before it is redirected to your real email.
