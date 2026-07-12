---
title: "FAQ"
description: "Frequently asked questions and their solutions."
---

> *There is an alternate FAQ available at https://smoo.it/#/faq*

::dropdown{title="How do I get SMOO?"}
**Official release:**
<br />
The latest official release of the mod can be found [here](https://github.com/CraftyBoss/SuperMarioOdysseyOnline/releases/latest).
<br />
<br />
**Variations and gamemodes:**
<br />
Join the [Discord](https://discord.gg/fJ3nxa2r4a) and ask for a specific version such as **Freeze Tag**, usually we can direct you to it.
::


::dropdown{title="What are the controls?"}
- **¹ Open the menu:** :s-icon{name="zl"} + :s-icon{name="a"} / :s-icon{name="b"}
- **Turn off background music:** :s-icon{name="l"} + :s-icon{name="up"}
- **Hide and Seek**
    - **Enable/Disable H&S:** :s-icon{name="l"} + :s-icon{name="left"}
        - **Switch roles between:** :s-icon{name="hider"} | :s-icon{name="seeker"}: :s-icon{name="up"}
        - **As** :s-icon{name="hider"} **Reset time:** :s-icon{name="l"} + :s-icon{name="down"}
        - **As** :s-icon{name="hider"} **Lower time:** :s-icon{name="left"}
            - *__Note:__ This may not go below 59 seconds. You can reset your time to go lower.*
        - **As** :s-icon{name="hider"} **Increase time:** :s-icon{name="right"}
- **Open the debug menu:** :s-icon{name="zr"} + :s-icon{name="up"}
    - **Next page:** :s-icon{name="zr"} + :s-icon{name="right"}
    - **Previous page:** :s-icon{name="zr"} + :s-icon{name="left"}
    - **Next player:** :s-icon{name="zl"} + :s-icon{name="right"}
    - **Previous player:** :s-icon{name="zl"} + :s-icon{name="left"}

:::alert{type="info" justify="text-left"}
*¹ While the game is paused or on the main menu.*
:::
::

::dropdown{title="Do emulators work with this mod?"}
Anything that can play Switch games *should* work with this mod, but make sure you are __not__ using the default profile if you use an emulator. Our [compatibility](/compatibility) page should list each one.
::


::dropdown{title="How do I switch gamemodes?"}
Go to the SMOO menu — see the **controls** section — and there should be options for some gamemode tweaks.

:::alert{type="info"}
**Note:** base SMOO does *not* have any gamemodes. It can only enable custom gravity.
:::
::


::dropdown{title="How can I fix my game crashing?"}
Try a different version of SMOO such as [Sardines](https://github.com/DaDev123/Super-Mario-Odyssey-Online-EXTENSIONS/releases/tag/Sardines) by [**Amethyst-szs**](https://github.com/Amethyst-szs) or [SMOO+ (unaffiliated)](https://github.com/DaDev123/SMOO-Plus/releases) by [**SecretDev**](https://github.com/DaDev123).

:::alert{type="warning"}
Be sure you ***replace SMOO with the new version***. It may not prompt you for a new IP address on launch.
:::
::


---
---

::alert{type="critical"}
Putting the lines here because we still need to replace the **smoo.it** links in the section below.
::

::dropdown{title="Where can I find servers to play on?"}
There's a [list](https://smoo.it/#/servers)! There are also text and voice channels for most servers.
::

::dropdown{title="My friend and I can't see each other!"}
- Make sure the [server is online](https://smoo.it/#/servers).
- Check your debug menu ( :s-icon{name="zl"} + :s-icon{name="up"} while unpaused) for the `Socket Connection Status: Socket Connected` line.
- Get everyone to warp at least once.
- If you are on emulator, make sure the profile you are using:
    - Has less than 10 characters in its name.
    - Is *not* the default profile and does not have the default profile name.

For more in-depth solutions, take a look at [these quick fixes from the Discord](https://discord.com/channels/481991664085499924/481993523424395297/1149492186254163968).
::

::dropdown{title="How do I host my own server?"}
Check [smoo.it](https://smoo.it/#/faq/112) for instructions for public and private servers. If you want to make a public server in the Discord, ask a moderator for a channel and role once you've prepared and tested your server.

:::alert{type="critical"}
**__Do not host it from your real IP!__** If you are playing with people you do not know personally and very well.
:::
::

---
---


::dropdown{title="I have the mod installed and I can see the SMOO icon but was never asked for an IP address"}

Most likely:

- Your **game** is not on `1.0.0`.
    - SMOO only works on `1.0.0` and it's highly likely it will stay that way. Modding for SMO `1.3.0`+ is more convoluted and thus not realistic for a mod of this complexity.
- You didn't install the mod correctly.
    - Make sure the mod folder has the following two folders in it: `romfs` and `exefs`. Also make sure those files have contents in them.
::

::dropdown{title="What do I do if I still have questions?"}
If your questions aren't answered by the website or pinned messages in our [Discord](https://discord.gg/fJ3nxa2r4a).
::
