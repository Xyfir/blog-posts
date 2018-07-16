If you're familiar with [proxy servers](https://en.wikipedia.org/wiki/Proxy_server), which allow you to mask your IP address to send and receive requests from another IP without showing your own, you should understand proxy emails, which are essentially the same thing, just instead of servers and IP addresses we're talking about email addresses.

Let's expand upon that, and say that you have a real, non-proxy email address called me@example.com, and then you create proxy email, for example proxy@ptorx.com, and configure it to redirect incoming mail to me@example.com. Now, whenever mail is sent to proxy@ptorx.com, that mail will be redirected to me@example.com, and whoever sent the original message will have no idea if it was redirected somewhere else or not, and even if they were certain that the mail _was_ forwarded, they would still be unable to determine where the mail was ultimately forwarded _to_.

A visual example:

- Mail is sent from `incoming-mail@example.com` to
  - `your-proxy-email@ptorx.com` which redirects to
    - `your-real-email@example.com` where you see the mail in your normal inbox

This is why proxy emails are a great way to hide your real email addresses from companies, hackers, spammers, and so on, to protect both your privacy and security. In addition to receiving mail, a proxy email can also send mail, and reply to received mail, all while keeping the real email address that it is a proxy for hidden away from whoever receives your sent mail.

Proxy emails also allow for lots of special abilities because they act as a middleman between the outside world and the email addresses they hide. Filters are one of those abilities, allowing you to blacklist incoming mail by ignoring anything from a certain address, domain, or any message containing specific content within the email's body or headers. Filters also allow you to whitelist incoming mail, meaning if _all_ of your whitelist filters _don't_ match when a piece of mail is received, it will be ignored and kept out of your real email's inbox, which is a great way to stop spam, phishing, and other unwanted mail.

While filters can prevent undesirable incoming mail from reaching you, _modifiers_ grant you the power to manipulate and modify allowed mail before it is finally redirected to your main email. Subject tagging, HTML-stripping (meaning text-only), and much more is offered through modifiers, including manually rebuilding an email's content by creating Builder modifiers that put together an email's content using its variables. Modifiers can be very simple, or very complex, depending on your needs and expertise.

Yet another useful feature of proxy emails is the ease of which you can disable redirects, or update where they redirect to on-the-fly. Anytime a proxy email starts redirecting spam or any other type of mail you'd rather not receive, all you have to do, if you wish not to configure filters, is disable redirects from the proxy email, or just delete it entirely, and your inbox will stay free of the unwanted mail it was redirecting to you. Should you ever decide to change your real email address, as most people occasionally do, it becomes a breeze, because all you have to do is update your proxy emails, which are all in a single place, to redirect to your new address. If all mail to that address was routed through proxy emails, then you can safely abandon your old email, knowing that you won't be missing any important messages, because it's all being sent to your new address.

Want to know how you can set up your own proxy email? See the next post: **[How to setup a proxy email](/blog/ptorx/2018/07/2-how-to-setup-a-proxy-email)**.
