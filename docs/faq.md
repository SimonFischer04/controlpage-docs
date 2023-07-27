# FAQ

!!! Abstract

    This is where you can find info about commonly asked questions / reasons for design decisions of this project.

The philosophy of this project centers around these three main principles:

1. FOSS
2. Software / Web Based
3. Compatibility

??? Question "Why yet another Macro Pad like tool?"

    Before creating this project I looked around if there already exists something fitting my needs. Here is just an (incomprehensive) list on some of the ones I looked at why I deceided against using them. (Conflicting philosophy / solution in brackets).

    !!! Info

        This does not mean that these projects are "bad" in any way! In fact some of them are really great and I want to credit them here, but just don't fit my needs. Also some of these might change in the future. But as I looked at them, this was the current state.

    - First of all the OG. The [Elgato Stream Deck](https://www.elgato.com/). Great solution if you want something that "just works", no setup required, ... BUT:
        - proprietary (1)
            - hardware quite expensive
        - hardware device (2)
        - Windows only (3): I know there are some other community made configuration utilities, but still a lot of the functionality does not work then.

    - [Touch Portal](https://www.touch-portal.com/):
        - proprietary (1): 
            - free version is quite limited
        - Flexibility of button sizes, ... (2)
        - Windows / Android only (3, 2): I somewhere heard that Linux support is planned (?) but didn't see any updates on this so far. Also only Android version.

    - [Macro Deck](https://github.com/Macro-Deck-App/Macro-Deck):
        - FOSS :thumbsup:
        - Windows only (3): seems like there is an App as well as a Web client :thumbsup:. But unfortuneately the main software is still Windows only.

    - [Stream-Pi](https://stream-pi.com/):
        - FOSS: :thumbsup:
        - Cross-Plattform :thumbsup:: Appreciate that there are server builds for Windows and Linux. And Client for Windows / Linux and Android, but still think that web-based app is more versatile **and easier to maintain**.
        - Basically completely built in JavaFX, even the server has no cli option: Sorry, but JavaFX - nothing for me :smiley:.
        - **UNMAINTAINED: This project seems to be unmained (July 2023)** and broken / quite buggy according to some github issues / videos online.

    TODO

??? Question "1) FOSS"

    TODO

??? Question "2) Software / Web Based"

    This being a basically software solution rather than a dedicated hardware product allows a lot of [Customisation](getting-started/features.md#customization). Of course there is this hardware needed but any device with touchscreen (and ability to open a web-page) does the job (like old phone, raspberry pi with screen, ...).

    So why:

    - **No hardware device** (f.e. FreeDeck): Flexibility: Does not allow for flexible button sizes / arrangements / ... 
    - **No APP.** (touch portal already used as an example here but doesn't matter which): Can't run on f.e. a raspberry-pi

??? Question "3) Compatibility"

    This actually kindof ties into philosophy 2. A lot of the other products are Windows, Android only. 
    
    This software provides docker images for hosting the backend and ui (can run on any platform: Windows, Linux, ...). And the client is just your regular favourite browser (you should be able to figure out how to open a webpage on any device :smile:. Could be f.e.: A raspberry-pi, phone, ...

TODO out of s
