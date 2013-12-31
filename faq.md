---
layout: default
title: FAQ
copyright: 2013 by ente for www.IRCnet.net. All rights reserved.
---
* Q: What exactly is this IRC thing?
* A: IRC is a fairly simple text chat system that has existed since 1988. IRC is
  organised in so-called channels. A user can join multiple channels and chat
  with other participants on the channel or via private messages. An IRC
  network consists of multiple servers that are linked together. People connect
  to the network by picking and connecting to one of these servers.

* Q: How do I find a channel for a topic I am interested in?
* A: The old solution to this is the `/LIST` command, which lists all channels
  on the network without any filtering. A new approach is the 
  [Alis service](../articles/alis) which filters for specific criteria.

* Q: What is IRCnet?
* A: In the beginning of IRC history, there was only one network. Since IRC is
  an open standard, and the [server software][ircd] it uses is available under
  an Open Source license, anyone could start a new network, which meant that in
  order to distinguish the networks, they were given names by their operators.
  The original network split into EFnet and Anarchy Net in 1990 over a
  disagreement on who should be allowed to link new servers to the network. As
  you might guess by the name, Anarchy Net allowed anybody to link without prior
  notice, which made the network very unstable, so that it quickly disappeared
  again. IRCnet split from EFnet during 1996, therefore both IRCnet and EFnet
  are considered descendants of the original IRC network. The split happened
  between the european and american part of the network when the trans-atlantic
  network link had died down (which happened way more often in the early days of
  the internet) after another fight about a technical topic that's no longer
  relevant but well-preserved in the history books of the internet. The european
  administrators chose the name IRCnet because the first server along with the
  creator of IRC were linked to the european half of the network.

* Q: Does IRCnet offer nickname and channel registration?
* A: No, not since 1994. IRCnet staff believes that nicknames and channels are
  not owned and that if yours gets "taken over", you have to pick a different
  one. If you want to prevent channel takeovers, use `!channels` or mark one of
  your trustworthy channel operators with the reop-mode `/mode +R <channel>
  *!<ident>@<hostmask>` such that ircd can re-op them as soon as your channel
  loses all ops. For more information, see [the article on reop](../articles/reop).

* Q: Why is this page semi-official?
* A: IRCnet -- unlike some other networks -- has no centrally organised steering
  committee. This means there exists no such thing like an official
  representation of the network as a whole, and any site claiming to be such a
  resource would be blatantly lying to you. However, some servers operate a
  website accompanying their IRC service. This website was started in 2013 as an
  attempt to create a more central resource on information concerning the
  network after a previous website fulfilling such a purpose (ircnet.com, there
  are still some outdated links to the site scattered around the internet) had
  been taken over by a domain squatter.

* Q: Where can I learn more about IRC?
* A: [irchelp.org](http://irchelp.org) has been the number one resource on IRC
  documentation since 1996. If you need help getting started, take a look at
  their website. If you still have questions afterwards, join `#irchelp`.

* Q: Where is the technical documentation about IRC to be found?
* A: The documentation of the original IRC protocol can be found in [IETF RFC
  1459][rfc1459]. However, IRCnet's ircd software uses an extended version of
  the protocol, which is documented in [RFC 2810][rfc2810], [RFC 2811][rfc2811],
  [RFC 2812][rfc2812] and [RFC 2813][rfc2813].

* Q: Who maintains ircd?
* A: Maintainership for the IRC server codebase has changed a few times over
  the decades, a full list of the authors and contributors is available [as part
  of the code base][ircd_authors]. ircd is currently maintained by [Piotr
  "Beeth" Kucharski][Beeth] since the 2.11 release series.

* Q: Who made this site?
* A: The website was created by ente using [jekyll][jekyll].

[rfc1459]: http://tools.ietf.org/html/rfc1459.html
[rfc2810]: http://tools.ietf.org/html/rfc2810.html
[rfc2811]: http://tools.ietf.org/html/rfc2811.html
[rfc2812]: http://tools.ietf.org/html/rfc2812.html
[rfc2813]: http://tools.ietf.org/html/rfc2813.html
[ircd]: http://www.irc.org/ftp/irc/org/
[jekyll]: https://github.com/mojombo/jekyll
[Beeth]: http://42.pl/
[ircd_authors]: http://www.irc.org/ftp/irc/org/irc2.11.2p3/doc/Authors
