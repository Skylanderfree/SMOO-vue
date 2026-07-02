---
title: "Play"
description: "Outlines the methods available to play the mod. This is separate from setting up the server."
---

::dropdown{title="Setting up the mod"}

:::alert{type="info"}
You only need to select *one* of these options.
:::

:::dropdown{title="Playing on a modded Nintendo Switch"}
::::alert{type="critical"}
[TODO]{style="color: orange;"} We need to make sure the user has already hacked their switch and/or link to the guide.
Also, we could use a `+` button icon.
::::

## Prerequisites

### [**Mod your switch**](https://switch.hacks.guide/)

### Check SMO Version

Before doing anything, check what version of *Super Mario Odyssey* you have installed.
To do this, press `+` on the game on the home screen and pull up its properties.
If you're already on version `1.0.0`, you can skip the downgrading process and move to Installing SMOO.
If you're on ***any other version***, you'll need to use the **Odyssey Downgrader**.

::::row{center}
:::::c-card{description="Ready"}
![Good version](/img/smo_v1.png)
> You're on `1.0.0`
:::::
:::::c-card{description="Not Ready"}
![Bad version](/img/smo_vX.png)
> You're **not** on `1.0.0`
:::::
::::

### Downgrade SMO

::::alert{type="info"}
Skip this if you are already on version `1.0.0`.
::::

If you are on a version *other* than `1.0.0`, you will need to downgrade your game.
We recommend you use the [Odyssey Downgrader](https://github.com/Istador/odyssey-downgrade/releases),
which should apply SMO version `1.0.0` to your game as a mod. This is necessary for a lot of mods to work.

::::alert{type="warning"}
*Many* issues stem from not upgrading your copy of the [*Odyssey Downgrader*](https://github.com/Istador/odyssey-downgrade/releases) or [*LockpickRCM*](https://github.com/Kofysh/Lockpick_RCM).
If you're having trouble downgrading SMO, try updating both.
::::

To get started, make sure:

- You have the cartridge or digital version inserted.
- You have dumped your Switch keys using [Lockpick RCM](https://github.com/Kofysh/Lockpick_RCM).

:separator{label="Once everything is setup..."}

- Place the [Odyssey Downgrader](https://github.com/Istador/odyssey-downgrade/releases) in the `switch` folder in the root of your sd card.
- Launch into your CFW.
- Open the **applets** menu.
- Select the `Odyssey Downgrade` applet:

::::c-card{center}
![Odyssey Downgrade Applet](/img/downgrade_applet.jpg)
::::

:::

:::dropdown{title="Playing on an emulator"}
::::dropdown{title="Ryujinx and forks"}
temp
::::
::::dropdown{title="Yuzu-based / Other"}
temp
::::
:::
::

::dropdown{title="Joining servers"}
:::alert{type="critical" align="center"}
[TODO]{style="color: orange;"}
:::
::

::dropdown{title="Compiling the mod from source (advanced)"}
:::alert{type="warning"}
You do *not* need to do this in order to use the mod. This is for experts and is optional.
:::
:::alert{type="critical" align="center"}
[TODO]{style="color: orange;"}
:::
::
