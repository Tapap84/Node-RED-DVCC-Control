Yes, I used AI to check for errors, clean up issues, and add context.

Running on my system for about three months without issues.

This is a Node-RED flow for either Cerbo GX or raspberry pi running venus OS, JKBMS on the battery, and DVCC enabled.

Designed for small solar systems that stat at 100% all day. The goal is to get the battery to use its capacity and not stay at high SOC to prolong battery life. Also has a cell monitor to prevent a single cell from over-volting

The battery is allowed to charge to 100% and has a two hour window to allow charging. After this, DVCC is set to 0a until the battery reaches 30% for two weeks. The MPPT will still "float" charge during this time with a battery possibly gaining 2% SOC per day. Once at 30%, it'll be allowed to charge to 80%. It'll stay between 30-80% until two weeks has passed and 100% SOC is allowed again.

The cell monitor will reduce charging current to 15a at 3.35v and taper to 1a at 3.45v and 0a at 3.50v. This is useful for packs that drift in cell difference or you want another layer of stopping cell over volting. 
