---
layout: default
title: Connecting to IRCnet
---
### Where should I connect to?

* For several countries, there exist wildcard DNS records users can connect to.
  See the table below to check if your country is one of them.
* If there is no known wildcard record for your country, chances are that there
  exists a local server you can access anyway. See the 
  [list of all servers][all servers] to see whether this is the case or not.
* If all else fails (and for instance all local servers keep rejecting your
  connection attempts), there are currently 5 servers allowing connections from
  all around the world. These servers are called open servers and can be
  accessed by connecting to `open.ircnet.net`. Alternatively, there's also 
  `eu.ircnet.net` and `us.ircnet.net` containing only the European or American
  open servers. Use these addresses if you want to avoid your connection
  needlessly crossing the pond.
* There is also an open access SSL server. The address is
  `ssl.irc.atw-inter.net` on port 6697. We are currently working to encrypt
  larger parts of IRCnet using SSL. This is work in progress.
  Please note that SSL is not reliable end-to-end-encryption, so be advised to
  use an OTR plugin for your IRC client instead, if you're worried about your
  privacy.

The order of preference is of course up to you, but it's generally best to
choose local wildcard records over specifying two or more local servers over
using the open servers for reliability reasons.

### Wildcard domains

The following wildcard domain names are available. This list was made to the
best of my knowledge. (Remember that IRCnet is decentral and this is merely a
semi-official page).

{% include wildcard-domain-table.html %}

### I'm trying to connect to the open servers, but I keep getting connection timeouts

Try a different port. The open servers listen on Port 6660-6669. Chances are
that your Internet Service Provider is blocking port 6667. If this isn't enough
and it just keeps not working, you can connect to `irc.portlane.se` on port
8080. This port will generally be open even with the most stupid ISPs because
it is a common alternative port for HTTP (which is all the internet consists of
these days). If all else fails, you can still use one of the [webchats](/webchat).

### I'm having trouble staying connected to IRC from my mobile device

IRC is based on TCP and sessions are bound to a single TCP connection with no
way to "reopen" a session after the connection has been lost, e.g. because your
mobile device switched from a Wifi network to a 3G network or you ping
timeouted because you were driving through a tunnel. There are services to
mitigate this, most of them work by keeping you permanently connected (like a
[bouncer][BNC]), but unlike a bouncer they expose the IRC session over a Web
API, which is more robust to sudden connection loss compared to IRC. One example
for software like this would be [IRCAnywhere][ircanywhere] but there's also
paid services offering similar features.

### Where can I get a list of all servers I have access to?

You can use the `!servers` command in the channel `#ircnet` to get a list of all
servers you can access using the IP address you're currently using. Since your
IP is used as your ident on the web chat, this also works using the web clients.

Example output (probably outdated) using a German IP:

    * You are talking on #ircnet
    <ente> !servers
    <@826HAAABC> ente => Performing lookup on your host to find what servers you can access
    <@826HAAABC> ente => Based on your host and ip you can use the following servers:
    <@826HAAABC> ente => irc.atw-inter.net irc.fu-berlin.de irc.man-da.de ircnet.choopa.net
    <@826HAAABC> ente => ircnet.eversible.com ircsrv.informatik.tu-muenchen.de openirc.snt.utwente.nl


[all servers]: http://irc.tu-ilmenau.de/all_servers/
[BNC]: https://en.wikipedia.org/wiki/BNC_%28software%29
[ircanywhere]: http://ircanywhere.com/
