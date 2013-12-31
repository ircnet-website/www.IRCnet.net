---
title: Alis
layout: default
---
While IRCnet has not been offering nickname or channel registration services
since 1994, there exists a special connection class called a "Service", which
can be queried using the "`/SQUERY`" command. The only currently active service
is called Alis and serves as a replacement for the old and unflexible "`/LIST`".

If your IRC client does not support the `SQUERY` command, you can manually
submit a request to Alis (or other services, should there be any in the future)
by using `/quote SQUERY Alis :your command here`

Please note that in this case the `:`-sign after the Service name is important,
otherwise it won't work and you will get the following error message or
something similar instead:

	-Alis(hub.uk)- You didn't specify a channel mask.
	-Alis(hub.uk)- Your query contains 1 errors. Use /SQUERY Alis HELP LIST

### Alis

Alis is a channel listing service. Unlike `/LIST`, Alis supports searching for
channels that match certain criteria, like a mask (`#*irc*` lists all channel
where the name contains irc) or by the number of people (`-min 60` lists only
channels with more than 60 people inside)

The alis help text is quite descriptive:

	/SQUERY Alis LIST mask [-options]
	Searches for a channel
	  mask               channels to search for, * and ? wildcards accepted
	  options:
	   -min x            minimum users on a channel
	   -max x            maximum users on a channel
	   -m mode           check against channel mode
	    +tn means channel has tn set
	    -im means channel has im unset
	    =tn means channel is exactly +tn nothing more and nothing less
	   -mode mode        same as above
	   -t string         topic of the channel shall contain string
	   -topic string     same as above
	   -s [m][t]         show modes (m) and who set the topic (t)
	   -show [m][t]      same as above

	LIST Examples:

	/SQUERY Alis LIST #foo* -min 10 -mode =tn
	Lists all channels who contain foo (#foo.int,#foo,...)
	if the mode is exactly = tn.

	/SQUERY Alis LIST * -min 10 -t http
	Lists all channels who contain http as word in the topic.
	Examples: "http://www.foo.org","http is cool","my httpd crashed"

	/SQUERY Alis LIST * -min 10 -t http -show mt
	Like above, but it will show the modes of the channel
	and the nick who set the topic.
