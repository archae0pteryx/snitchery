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

- Effective in all profiles
 - Only the default system bits and VPN connectivity.

- Home
 - accountsd (443)
 - Addressbook (443)
 - Adobe desktop service (DENY) (I HATE THE AMOUNT OF ADOBE BS.)
 - AGS (see above)
 - Airplay (7000)
 - AKD (443)
 - Alfred (443)
 - Atom (443)
 - Calender Agent (443)
