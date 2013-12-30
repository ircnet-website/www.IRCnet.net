---
layout: default
title: How the new !channels work
---
**Warning: this document is outdated**

As we all know, #channels are subject to collisions which have very annoying
side effects. Channel Delay is intended to prevent the collisions, but is far
from being perfect.

These new channels will make collisions extremely unlikely.

--------------------------------------------------------------------------------

How does it work?

In order to make collisions impossible, the channel name is assiocated to a
unique ID. The pair (name , ID) will thus be unique as well.

The channel real name is built by concatenating the ID and the short name, for
example, channel "`!foo`" might be "`!2B4dfoo`". The ID has a constant length
which makes it easy to separate it from the actual "friendly" name.

The channel creation must be requested. For example to create a the new channel
foo, one must try to join "`!!foo`".

In addition to a unique name, these channels obey to soe new simple rules:


It is not possible to create a channel if one with the same short name (but
different ID) already exists has split recently (e.g. the channel delay was set
and hasn't expired. see definition below).

It is possible to join a channel which has split recently (if the modes allow
it). In this case, the user does not get oped. (Note that this differs from
\#channels which get locked in such a case, until the Channel Delay expires then
allowing a user to re-create it, gaining chanop status).

If only one channel "!foo" exists, it can be joined by giving the short name
only. The JOIN command is the only one accepting shortnames for the channels

If several channels have the same short name, but different ID, a user can
choose to join any of them by specifying the ID.

If a channel becomes opless, and remains opless long enough for the Opless Delay
to expire, all the channel members will be optionnally oped.

The channel delay duration is longer (60m) than for #channels (15m). This is
necessary to avoid several channels having the same short name (but different
ID) as much as possible.

The channel delay is set when any member splits.

The opless delay is set whenever a chanop member leaves the channel.

--------------------------------------------------------------------------------

New modes:

As channel collisions are eliminated, it is possible to enhance the mode system.

general mode:

* `+r`

  reop mode, if the channel becomes opless for long enough, servers will re-op
  users in the channel. Note that not setting this mode can be used to create
  'modeless' channels (such as `+channels`) but with specific characteristics.
  (anonymous, secret...)
  
  Reoping is done randomly by a random server. While it may sound like loading a
  channel with many clones increases greatly the chances of catching the reop, the
  randomization is done in a way which does not favor clones at all.
  
* `+a`

  This is anonymous mode, if toggled by the owner nobody can see who is talking
  or joining.

  All you see is `anonymous@blaha.com has joined`. Example:
  > `06:46 ## Join !3B4OWchat: anonymous (anonymous@anonymous.)`
  You will see that when someone parts too.

user mode:

* `+O`

  This mode is given to the creator of the channel by the server, it cannot be
  passed or gained after the channel was created. The creator is the only person
  able to set/unset r modes, and set (but not unset) `+a`.


		************** PLEASE NOTE *********************
		Original text by: Christophe Kalt
		Original URL: http://www.stealth.net/~kalt/irc/channel.html
		Maintained by: IRCNet.net Team
		Last updated: 24.02.2002
		*********************************************** 	
