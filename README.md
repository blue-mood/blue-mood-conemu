# Blue Mood theme for Conemu and Cmder

A port of emacs Blue Mood theme's colors for [Conemu](https://conemu.github.io) and [cmder](https://cmder.net).

## Activation

You have to manually modify the ConEmu config file.

- Open `ConEmu.xml` file. It is in the installation directory of ConEmu or the user directory like `C:\Users\UserName`.
- Find the palette definition. It is an xml tag that starts with the following code:
```
<key name="Palette1" modified="2016-02-21 19:15:02" build="160218">
<value name="Name" type="string" data="ThemeName"/>
<value name="ExtendColors" type="hex" data="00"/>
...
<value name="ColorTable00" type="dword" data="00000000"/>
<value name="ColorTable01" type="dword" data="00800000"/>
...
```
- If you don't find the xml above, you may not have any custom color scheme. So open ConEmu Settings dialog (Win+Alt+P), and go to Features -> Colors -> Schemes, enter a name and click Save, then the palette definition will be generated. Close ConEmu.
- Replace the color table in the palette tag with the blue-mood color table (see blue-mood.xml, there are 32 color values), save the `ConEmu.xml`.
- Reopen ConEmu.
- Note that ConEmu's color scheme may not change in the later version, because the `<Current color scheme>` is used by ConEmu instead of blue-mood, you need to go to Features -> Colors -> Schemes and switch to blue-mood.

## Credits

This theme was generated by using the theme generating script `gen-theme.py` provided by [dracula's conemu theme](https://github.com/dracula/conemu).
