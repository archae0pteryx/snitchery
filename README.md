## Snitchery
### [Little snitch](https://www.obdev.at/products/littlesnitch/index.html) Rule set(s)
---
### Installation:
1. Open Littledsnitch config
2. Place hot_pocket in wave: do
3. cook on high for 2.5 min
4. click import rules (where applicable i.e. "all over")

### Theory / Mechanics / General Thoughts

Litle snitch has some really amazing features, namely, auto profile switching for different networks.

I always begin with setting a "deny connections" for everything, then, allowing what I need. It took me a long time to figure this part out. This will save you from having a pop up every goddamn second when you fire this baby up.

When you import these rules you'll most certainly have applications that I don't and vice versa. You will see this expressed in the approprate menu on the left side of the Little Snitch config.

This set is nowhere near finished but it's a great starting point for someone to "train" their own firewall. My general "rule of thumb" (sorry ladies) has been to adhere to the rule of least permissions. This is great in theory but unfortunately in the real world it becomes extrememly annoying to approve rules on a domain by domain basis. So, I have been training the snitch via Port and Protocol and not the full-on, super annoying, domain based rules.

### Rules and Profiles

#### Profiles:
- Home
 - Obviously, home network with very permissive rules.
- Hotspot
 - This one is a work in progress as I rarely use "hotspots"
- iPoop (iPhone)
 - This is similar to the Hotspot but should be used with a "trusted device"
- Public
 - Super strict ruleset for public networks.
- Public +
 - Similar to Public but a bit more permissive in order to get work done.
- Vadded (VPN)
 - I used [mullvad](https://mullvad.net) as my preferred VPN provider for a long time. Now, I configure my own VPN's through digital ocean. The idea is the same either way, because of encryption, we can use this as the permissive set.


#### Rules:


- __Effective in all profiles__

 - Only the default system bits and VPN connectivity.


- __Home__

 - accountsd (443)
 - Addressbook (443)
 - Adobe desktop service (DENY) (I HATE THE AMOUNT OF ADOBE BS.)
 - AGS (see above)
 - Airplay (7000)
 - AKD (443)
 - Alfred (443)
 - Atom (443)
 - Calender Agent (443)
 - Clip Menu (DENY)
 - CloudD (443)
 - com.geod (80, 443) (For device tracking)
 - Safe Browsing (443)
 - Contacts (443)
 - Core Sync (Adobe) (DENY)
 - Creative Cloud (443)
 - Docker (443)
 - Firefox (ANY)
 - Gamed (DENY) (I fucking hate gamed!)
 - Google Update (DENY) (I prefer to do this manually)
 - helpd (DENY) (i google anyway)
 - imagent (5523) (This is for messages to work)
 - iStat Menus (443)
 - iTerm2 (ALLOW ALL)
 - iTunes (443)
 - ksfetch (DENY) (This is for google update and I have no faith in google. Again. Manually take care of updates. Also, when / if you use Chrome it will tell you there're updates anyway.)
 - Little Snitch Update (443)
 - locationd (443) (This is for find my mac to work. I always keep this enabled for all profiles because if my laptop is ever stolen, i'd hate to have little snitch block me from finding it! (this HAS happened to me!))
 - Mail (443, 585, 143, 993, 465)
 - mapspushd (443 to domain: apple)
 - MEGAclient (ANY)
 - Messages (DENY 80, ALLOW 443)
 - nbagent (ANY) (This is for NETBIOS and the Bonjour service as far as I have read... I need to play with this one a bit more)
 - node (ANOTHER ADOBE BS... DENY)
 - node (for creative cloud allow 443)
 - nsurlsessiond (ANY) (This is for proper name server addressing. I need to investigate this one as well)
 - OPENVPN (ALLOW ANY) (both user processes and system)
 - photolibraryd (DENY) (I don't use the photo cloud BS... so... deny.)
 - Photos Agent (443) (as far as I can tell, this one is just for photo app updates and the like.)
 - Safari (ANY)
 - Slack (443)
 - SoftwareUpdateD (deny) (i need to revisit this one)
 - Spectacle (443) (another one I need to revisit)
 - Stocks (443)
 - Store Accountsd (ANY)
 - Store Assets D (443)
 - Thunderbird (DENY 80, ALLOW mail protocol ports only)
 - Transmission (DENY) (We don't want un-encrypted torrents on our home network do we?)
 - Unity (443)
 - User event agent (80) (revisit)
 - Weather (443 to apple only)
