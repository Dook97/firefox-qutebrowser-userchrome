# A minimalist userChrome.css

Firefox allows a great deal of customization. In fact it goes as far as to give
you the option to completely change the look of the program. That's what
userChrome.css does.

![](./screenshots/screencap.png)

This config is a (soft) fork of
[aadilayub's](https://github.com/aadilayub/firefox-i3wm-theme).

The main differences are:

- this one is maintained, because I use it
- navbar isn't completely removed; it shows on focus (hover or Ctrl+l)
- color of text in tabs is determined by the color code of the tab's container

It's goal is to remove all unncessary visual clutter while preserving
functionality. That means you could use this user chrome with an otherwise
normal firefox config, though I recommend you give a try to the
[tridactyl](https://github.com/tridactyl/tridactyl) extension, which I think
goes together great with this user chrome.

## How to use

Enable user chrome in `about:config`:

1) in `about:config` set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`

Enable compact mode in `about:config`:

1) in `about:config` set `browser.compactmode.show` to `true`
2) in the customize toolbar menu set `density` to `compact`

Enable dark theme in settings.

Clone this repo, then copy the `chrome` directory to your firefox profile:

```sh
git clone https://github.com/Dook97/firefox-config
cp -r ./firefox-config/chrome ~/.mozilla/firefox/[YOUR_PROFILE]/
```

If you're not sure, which of the directories is your profile, you can find out
by going to `about:profiles`

If you want the navbar to show on hover go to the bottom of the file and
uncomment the code there. Otherwise you may only toggle the navbar by pressing
`Ctrl+L`

Then either install the Jetbrains Mono font, or change the relevant line
(search for 'Jetbrains Mono') to some other font that you have installed.

## Common issues

### black stripe under tab bar

increase the value of the `--tab-min-height` variable in userChrome.css

## Is it practical?

Absolutely - you just have to get comfortable using keyboard shortcuts. I use it
with the aforementioned Tridactyl extension, which pushes the experience to a
whole new level.

Some tips:

* On linux there will often be a key, which toggles window moving mode. For me
  it's left alt.
* Ctrl+shift+W or Ctrl+Q closes Firefox
* Ctrl+L toggles the navbar
