**A comprehensive KiCad Library for the Raspberry Pi Pico** 🥧
==============================================================

### Providing footprints, symbols, & models for the module's various forms & implementations

> *This git submodule is only the finished library.  For source files, releases, and commit history, see [Ki-Lime Pi Pico][URL-Repository]*.



***Features***
==============

- **KiCad 8.0 support** *(For KiCad 7.0 support, checkout `1.1.0`)*
- **Schematics with alternate pin definitions** to select more specific behaviours for each GPIO, as well as specify power directionality
- **Generic and specific footprints** for the Pico and Pico W
  - Through-hole and surface-mount footprints with and without mounting holes
  - Hand-solderable test points (ie. USB signals) in footprints with underside castellations
  - Optional pin labels as an add-on footprint
  - Optional keepout zone for 2.4 GHz RF on shared footprints
  - Ability to add individual schematic symbols for sockets, and a virtual Pico for the BOM and rendering
- **Diverse 3D models** for surface-mount, through-hole, and socketed forms of the Pico, Pico H, Pico W, and Pico WH using photorealistic materials
- Majority adherence to the [KiCad Library Conventions][URL-KLC] version 3.0.41



***How do I use this library as a git submodule?***
===================================================

> *If you're looking to use this library without submodules, you probably want the source repository [Ki-Lime Pi Pico][URL-Repository].*

- Ensure you are running KiCad 7.0 or later
- Identify the path where you want this library to exist in your project  
  *(below, I will use `<GIT-ROOT>/pcb/project-libraries/ki-lime-pi-pico`)*
- For the latest release (KiCad 8.0+) without any history, from within your git repository call:
  - `git submodule add --name ki-lime-pi-pico --depth 1 https://github.com/recursivenomad/ki-lime-pi-to-go.git pcb/project-libraries/ki-lime-pi-pico`
  - And since this library's history typically won't be needed by downstream users, I'd recommend:  
    `git config -f .gitmodules submodule.ki-lime-pi-pico.shallow true`
- For a specific release (such as 1.1.0 for KiCad 7.0 support) with the complete submodule history, call:
  - `git submodule add --name ki-lime-pi-pico --branch 1.1.0 https://github.com/recursivenomad/ki-lime-pi-to-go.git pcb/project-libraries/ki-lime-pi-pico`  
  *Note that `--branch` and `--depth` [cannot][URL-Git-Submodule-Limitation] be used simultaneously in `submodule add`*
- Open the relevant KiCad project
- Select `Preferences > Manage Footprint Libraries...`
- Select the `Project Specific Libraries` tab
- Click the folder icon in the lower left to `Add Existing`
- Navigate to and select `.../ki-lime-pi-pico/Module_RaspberryPi_Pico.pretty/`
- Click `OK`
- Select `Preferences > Manage Symbol Libraries...`
- Select the `Project Specific Libraries` tab
- Click the folder icon in the lower left to `Add existing library to table`
- Navigate to and select `.../ki-lime-pi-pico/MCU_Module_RaspberryPi_Pico.kicad_sym`
- Click `OK`

To use, simply add a symbol to your schematic as you would any other; symbols should be located under the section `MCU_Module_RaspberryPi_Pico`, and footprints under `Module_RaspberryPi_Pico`.

**You're all set to design exciting new circuit boards using the Raspberry Pi Pico! 🎉**



***Further reading***
=====================

*Further reading available in the [source repository][URL-Repository].*



***License / Access***
======================

This work is made freely available under your choice of the [*MIT-0*](./LICENSE.txt) license or [*CC0-1.0*][URL-CC0] public domain dedication.  
Although attribution is not required, sharing when you've made something with my work is really cool 💖

*No additional/conflicting permissions were present in this repository at the time of release.*

----------------------

*Repository: <https://gitlab.com/recursivenomad/ki-lime-pi-pico/>*  
*Releases: <https://gitlab.com/recursivenomad/ki-lime-pi-pico/-/releases/>*  
*Submodule: <https://github.com/recursivenomad/ki-lime-pi-to-go/>*  
*Contact: <recursivenomad@protonmail.com>*

----------------------



### Donations:

*Accepted, but not expected*

> Online payment: <https://donate.stripe.com/dR6dSU1PueevgKY4gs>

> Monero (XMR): `8Bhyeo232EVDiK7aRSzHGRC28RZ1H6FL55V6CVyCVtxdDRQXHk8btPU8Wr5G8K3AWgaK19JfYbshKfHWqc177jwtCtCSaz1`

> Ether (ETH): `0xD1b824f2Ec3D609e816B04A301124129602A5238`

> Bitcoin (BTC): `bc1qadq5kyuuc7etgu5ywlygnaepqhzgc2u7gxkze2`






[URL-MIT-0]: <https://opensource.org/license/mit-0/>
[URL-CC0]: <https://creativecommons.org/publicdomain/zero/1.0/>

[URL-Repository]: <https://gitlab.com/recursivenomad/ki-lime-pi-pico/>

[URL-Git-Submodule-Limitation]: <https://lore.kernel.org/git/1410455473-2367-1-git-send-email-cole.minnaar@gmail.com/>
[URL-KiCad-Forums-cdwilson]: <https://forum.kicad.info/t/21104>
[URL-KiCad-Forums-mgyger]: <https://forum.kicad.info/t/35844/12>
[URL-KLC]: <https://klc.kicad.org/>
[URL-Official-Example]: <https://datasheets.raspberrypi.com/rp2040/hardware-design-with-rp2040.pdf#page=15>
