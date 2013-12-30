---
title: Unofficial new server linking guidelines
layout: default
---

### DISCLAIMER
IRCnet is administrated in a distributed way by special designated bodies (more
or less a TLD), the whole linking procedure and the policy is handed by each
body autonomously.

This document provides rough hints on what most administrators agree to be
prerequisites for a new server to be linked. Therefore this document is
unofficial in its nature. Please also note that administrators of different
IRCnet bodies may have totally different requirements. You need to inquire with
them, if you want to be sure what those exact requirements are. However we are
not providing any contact information within this document apart from IRCnet.net
owns.

By submitting your application to us you agree, that it will be review by in
depended support staff of IRCnet.net and if deemed appropriate it will be
forwarded to responsible body of IRCnet for further consideration.

-----

Guidelines:

1. The IRC server must be permitted and supported by administration of the
   machine and network it is on.

2. The machine you run must be dedicated and adequate for the job.

   The machine can not contain other users (i.e. people you do not know) or
   bots. Public FTP's and not related WWW services are not permitted also.

3. If you're a Bot Service Provider (BSP) you're not allowed to link IRCnet.

   There are definitely enough bots on IRCnet already. We don't need a server
   just bringing in more. Bots attract unnecessary DoS'es (Denial of Service).
   It does not exactly raise your trust ability

4. If your status is bad (you are a groupie), it's unlikely we would let you run
   a server, considering we don't even let you connect to ours. The opinion of a
   number of operators is asked (just in case others just were not familiar with
   the case).

5. The server should be multihomed. i.e. it is not enough if you have
   connectivity to just one uplink.

   The link may very well go down at some point, as there is possible DoS or
   another problems, like physical damage which takes time to fix. If there are
   multiple links, the risk of total black-out is considerably smaller. Please
   note, that T1 is not enough, ADSL is not enough, Cable-modem is not enough.
   It have to be OC3 at last.

6. We only link servers with NSP/backbone-acknowledgement.

   Because otherwise filtering will be too difficult and the server may not
   actually be able to stay with our net (NSP/ISP ends contract).

7. The administrator must work for the company or have administrative privileges
   (UID 0/root) on the boxes involved. It is not rare to also expect the
   administrator to have access to the firewall-configuration. It is actually very
   common.

Physical access is useful to fix some error-conditions.

8.  Dedicated machines should be resource powerful enough to handle hundreds of
    users and run ircd approved by IRCnet.

9.  Your TLD (Top Level Domain) must have enough users to connect.

10. Foreign server administrators can not override a local coordinator's
    decision on what is to be linked and what not.

    The local administrators will know best whether the people requesting a link
    indeed are reliable enough and if they have a sufficient amount of users.
    
    If this was not the case, the network's topology would be all wrecked as a
    route from server A to server B, both in TLD X would go via TLD Y. All this
    just because a new server was 'required'? Not likely.
    
11. The server administration has to have reasonable knowledge in IRC and UNIX,
    and have to be willing and able to help and answer most user questions.


Please be aware, that usually administrators never link servers from people, who
apply for a link.  If there is really need for a server, the administrators of
that TLD will look around which organization would be most appropriate, and then
ask them, if they would like to support an IRCnet server.

Still feeling lucky?

Feel free to join `#eu-opers` and ask for more information.
See disclaimer for rules.

	************** PLEASE NOTE ****************
	Original text by: viha
	Last updated: 2013-12-30 by ente
	****************************************** 
