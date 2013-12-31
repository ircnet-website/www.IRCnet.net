---
title: reop mode
layout: default
copyright: 2013 by ente for www.IRCnet.net. All rights reserved.
---
The so-called Reop-Mode can be set on any channel type that accepts modes (i.e.
`!channels`, `#channels` and `&channels`, but not `+channels`). It takes a
parameter containing a hostmask that you want to be reopped in case the channel
becomes op-less. After a channel becomes op-less, a server will look at the reop
list, match all hostmasks on the channel against the reop list and then reop a
random one matching one of hostmasks on the reop list.

**Note**: This channel mode is currently not mentioned in any of the IRCnet
specific RFCs. This also means that the RFCs as published by the IETF are
outdated information at this point.

### Obtaining the reop list for a channel

In order to obtain the reop mode list for a channel, a client sends
`MODE #channel R` and the server will reply with the numeric replies `344` as
long as there are hostmasks left in the list, and then a final `345` numeric
reply denoting the end of the reop list for a channel.

Example:

	→ MODE #example R
	← :irc.example.com 344 yournick #example user!ident@hostmask.
	← :irc.example.com 344 yournick #example *!*@*
	← :irc.example.com 345 yournick #example :End of Channel Reop List

### Adding or removing a hostmask from the reop list

This works exactly the same way as adding or removing a ban, only that `+R` is
used instead of `+b`.

Example of adding a hostmask:

	→ MODE #example +R *!*@example.net
	← :yournick!you@example.com MODE #example +R *!*@example.net
	
And removing it again:

	→ MODE #example -R *!*@example.net
	← :yournick!you@example.com MODE #example -R *!*@example.net

Note that you should make your reop masks as granular at possible and avoid
adding e.g. internet connections where the IP changes in regular intervals
because either the reop list needs to be updated every time or you make your
channel vulnerable for takeover attempts from the network where your client is
connected from, like other customers of your ISP.

Good example (working identd, no wildcards in hostmask):

	MODE #example +R *!peter@subdom1.example.net

Bad example (no identd required, wildcard in hostmask, hostname looks like it
is a dynamic IP):

	MODE #example +R *!*peter@*.pool.dynamic.isp.net

### Relation between +R and !channel-mode +r

`+r` on a `!channel` has the same effect as "`+R *!*@*`", i.e. after a random
period of time a random client will be given operator status. This renders `+r`
obsolete, also `+R` works on any type of channel. However, `+r` will probably
continue to be supported until at least ircd2.12 is released, but it's
recommended to use `+R` instead. The restriction of `+r` only supporting only
`!channels` was completely arbitrary to begin with so it's a good thing that
this is no longer an issue.
