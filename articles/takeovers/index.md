---
layout: default
title: How to deal with IRC takeovers
---
### Introduction

This document attempts to explain to how to cope in a sane way with IRC
(Internet Relay Chat) takeovers. If you don't know what this is all about,
don't bother to continue reading this -- it's not worth your attention (just
believe me).

In order to get the most out of this document, you need to understand a few
basic things:

Takeovers are of course lame. They disrupt you for at least a short time from
chatting and they can be very disappointing for newbies, who are not yet
familiar with them. Yet, they happen every day. In most cases, someone who
overtakes a channel does this for his ego. That's the old penis-extension issue:
By overtaking a channel, you think your ego (as well as your penis) grows and
you become superior to the regular channel members because now you "own" their
channel and they couldn't hinder you from taking it. Naturally, this is a
fallacy: IRC (as its name implies) is about chatting not about ownership. The
people on IRC are there for chatting and they can do it on an infinite number of
channels. And by overtaking one of those channels, you just gain the temporary
control of this single channel. And controlling a channel on which you are on
your own is one of the most boring things you can imagine for a takeover guy
(see below for details).
That's why in most of the cases they act and appear in a group so they can at
least kick and ban themselves on the new gained channel. =) So what have we
learned from this little excursion?  Exactly: Takeover guys have really small
dicks. ;-)


### Channel design

The following is a description of how i think you should "design" your channel
to make it less attractive for takeovers:
* Don't use bots.
* Don't use auto-ops.
* Don't activate `{nethack,mass-op,mass-deop}`-protections in your script.
* Do only op upon request.

Adapting those measures shows that you don't care much about chanop-status (and
that you are in the first place only interested in chatting) and they represent
very little resistance on takeover attempts. Yes, you read that correctly: Very
little resistance. The less resistance someone will face when trying to takeover
"your" channel, the less interesting it will be for him. The reason for this
being obvious: In order to overtake a channel with huge resistance (ie. tons of
bots and scripts with protections), you need of course a huge penis. So if you
succeed to take such a channel, you prove yourself that your penis is really
huge. But: Taking over a channel with very little resistance does at best prove
that your penis is very small. Therefore, (you get the picture) why bothering
taking over such a channel?

### When someone attempts to takeover your channel

What should you do when there's an attempt to takeover "your" channel? Well,
that depends on how the takeover attempt is being done. If there are only one or
two users who try to take it by deopping all the regular ops, then just make
them lose their chanop-status. But if you see that the takeover is being done
more "professionally" by a more or less large group of users, then you should
just watch the show and log everything. Trying to defeat such an attempt can be
possible but it will just have the effect that the same group will try even
harder next time to take "your" channel.

### What kind of information you should log

When "your" channel is being taken over, you should try to log beside the usual
log information (joins, signoffs, ops, server-ops) the `WHOIS` information of
the users who try to takeover "your" channel. If an abuser is using a server
which is hostmasked (ie. when the WHOIS for him has "`*.TLD`" in the server
line, then you have to type "`/WHOIS Nickname Nickname`" in order to get the
real server he is using. You need all that when you want to report the abuse to
the concerned server admin and/or ISP. The contact address for a server admin
can be obtained by typing "`/ADMIN `".

### When your channel has been taken over

Once you and all the other regular ops on your former channel have lost their
chanop-status and the takeover users have gained it, here is what you should do:
* Relax. Life goes on.
* Get and save the WHOIS information of the takeover users, if you haven't done
  so yet.
* Create/join `#channel2` and invite the regular users from `#channel` to the new
  `#channel2` so you can continue to chat in peace there.

If the channel which has been taken over stays open (ie. that everyone can join
it), then stay on it so you can tell other "regular" users to go to `#channel2`
too.

Mail the log of the takeover to the concerned server admin(s).

It's common use to join `#channel2` if `#channel` has been taken over. Which means
that if, for example, `#blah` got taken over, you just join `#blah2` and continue to
chat there. Should `#channel2` not be free, then try `#channel3` or another
variation.

To make sure that new users find the new channel if the usual channel has been
taken over, you could place a user with the nick of the usual channel on the new
one so that new users would just have to look at his WHOIS information to see
what the name of the new channel is.

Example: `#blah` has been taken over. So you create `#blah2` and place a user with
the nick "`blah`" on it. And now, if someone comes on IRC and sees that #blah is
not usable, he just does "`/WHOIS blah`" and sees that "`blah`" is on `#blah2`.
Therefore he knows now that `#blah2` is the temporary replacement for `#blah`.


### What you should remember

No one can hinder you from chatting if you really want to.
The less resistance on takeovers, the less trouble.


	************** PLEASE NOTE *********************
	Original text by: Kasi
	Original URL: http://home.snafu.de/kl/takeovers.html
	Maintained by: IRCNet.net Team
	Last updated: 24.02.2002
	************************************************
