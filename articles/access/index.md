---
layout: default
title: IRCnet servers access troubles
---

You ask, why can you not access our IRC-server (K/+r). The answers are very likely to be found here.

1.  You SHOULD run identd (auth, RFC1413).

    If you do not run an ident-service (on port 113), it will be too complex to work out the persons actually misusing the service. Practically this means the whole host is likely to get restricted.  The easiest way of avoiding this is installing identd. Or asking your local site-administrator or security-coordinator to open it up for you.  Running it also points out you actually care who is using your service.  It's basically a bit like wearing tidy clothes. People may like you more if you do, even that very few are likely to force you to.  

1.  You MUST make sure your reverse-DNS (PTR) works together with your IN A.

    In English: Your hostname should always resolve when accessing our IRC-
    servers.  If you are not the network-administrator yourself, e-mail him/her
    and ask him to enable it. There are no reasons not to. Only reasons *to* do
    it.
    Having a working DNS also points out that: 

    1. Your hostname was intended for actual usage and it's not just somebody
       taking advantage of an unused IP to abuse it.

    1. Your ISP cares (and might even handle some of the abuse).

    1. Your ISP is competent. If it doesn't even know how to run a DNS-server,
       which is one of the most basic services on the Net, it has no business
       accessing our services, either.

1. Your geographical location SHOULD match the top-level domain (TLD).

   In English: If you are Finnish, you should be dot-FI.  As having a United
   Kingdom domain-name under Finnish IP-blocks is very unlikely to have a real
   purpose, it is often assumed you may either be trying to fake somebody else or
   simply do not understand the concept of TLDs.
   Or perhaps you are just trying to impress somebody. Bad idea. Words should
   work better than silly domains.  That could also be an idea to add: If you
   are restricted or K:lined on a foreign server, it shouldn't be much of an
   issue for you. It's trivial to retrieve a list of local servers in your
   region - `/links *.TLD *.TLD`

1. Your hostname SHOULD serve a purpose.

   In English: A hostname like 'this.sux.badly.com' is unlikely to get you much
   credit. First of all, COM was originally meant for commercial organizations,
   try picking something more appropriate (assuming there is no company called
   Badly, Inc). The 'this.sux' part is vanity. It contains one 'unused' dot. It
   also relays a message, while the IRCNAME field or PRIVMSG should be used for
   this purpose. The longer your hostname is (and the less use it is / the more
   offending it is), the more likely it is to get cut off IRC.

1. One client SHOULD be enough for everyone.

   There is no need for you to have eight 'screened' IRC-sessions or bots on one
   single IRC-server. It does not serve a purpose.
   Maybe you need two - one client on a UNIX-box, one on Windows. But that
   should already cover it. Definitely. If you need to run a bot, just run one.
   Nobody will want to take over a very tiny channel that nobody really goes to.
   This is the case with most user-created ones.
   On the other hand, if it has a huge load of bots, the people taking it over
   will:

   1. Think it's big and thus ''worth'' taking over.

   1. There is a challenge. They want to fight with your army of 50 bots. It's
      just about the same as provocating them.

   1. You SHOULD keep your bots off botnets.

   Botnets on IRC do not serve a direct purpose. In the end, you will see you
   were actually handing out the control of your bots to a bigger, more organized
   hacking/war-group. You won't want that.
   The fact somebody was abusing your access to a 'bnc' or 'eggdrop' is of no
   excuse. It was your own stupidity to hand out the pass in the first place. Who
   knows, maybe you'll do it again? By accident?

1. You MUST keep yourself away from the clans, groups and crews.

   If you wish to form a group, do it on Quake. Or if you want to kill somebody,
   try doing it on Q2 instead.  There are not many things that are black and white
   to operators. Groups, on the other hand, manage to fit there.  Very few
   operators want any connections to any groups. Asking them to join your group
   would be more or less a suicide (they'll get upset at you for belonging to one,
   anyway).  Not being a groupie includes not joining or operating any of the
   questionable channels. At least if you want to stay on the safe side...

1. You SHOULD keep your IRCNAME-field tidy.

   In addition to belonging to groups, setting an IRC-name of the 'IRC-war since
   1998' kind, is suicidal. Especially if it contains all that elite- talk
   (numbers as letters).

1. You SHOULD run your clients with proper nicknames.

   You mailing us, telling your client '`}[004010`' got K:lined will, at most
   make us grin. What is the idea with not picking a proper nickname? That
   doesn't look like anything but a clone or abuser to the lot of us.

1. You MUST not become a nuisance.

   Nobody wants to provide a free service to somebody doing nothing but annoying
   others.  Being a nuisance is, ultimately, the most efficient way of earning a
   big, permanent ban.



	
		************** PLEASE NOTE **************
		Original text by viha.
		Maintained by: IRCNet.net Team
		Last updated: 24.12.2002
		*****************************************
