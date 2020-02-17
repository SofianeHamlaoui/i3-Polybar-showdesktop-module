# ShowDesktop Polybar Module

A module that allows you to use Show Desktop icon (kind of) on i3 (polybar)
![Show Desktop](http://up.sofianehamlaoui.me/show-desk.jpg)

## Dependencies
- [Polybar](https://github.com/polybar/polybar)
- [AwesomeFonts](https://fontawesome.com/)
- [Happiness](https://github.com/SofianeHamlaoui)

## How does it work
This module works when you click on the Polybar icons,

### Left Click :
that moves the selected windows to scratchpad ```move scratchpad ``` using ``` i3-msg ```

### Right Click :
that shows the hidden windows (sent to scratchpad) ```[class=.*] scratchpad show``` using also ``` i3-msg```.

I added ```[class=.*]``` so it shows all the windows sent to scratchpad and not one by one
## Demo on Youtube on how it works

[![The Youtube Video](http://up.sofianehamlaoui.me/desk-thumb.jpg)](https://www.youtube.com/watch?v=l3qms955nWo)

## Screenshots :

![Polybar Icon](http://up.sofianehamlaoui.me/Screenshot-showdesktop-module.png)

![Desktop with windows](http://up.sofianehamlaoui.me/Screenshot-Showdesk-2.png)

![Desktop with hidden windows](http://up.sofianehamlaoui.me/Screenshot-showdesk-3.png)

## Settings :

``` ini
[module/showdesktop]
type = custom/script
exec = echo ""
click-left = exec i3-msg move scratchpad
click-right = exec i3-msg [class=.*] scratchpad show
```
## How I got the idea : [Reddit r/i3wm 💓]
- [Show Dekstop Hotkey](https://www.reddit.com/r/i3wm/comments/5bgeg2/show_desktop_hotkey/)

- [Show All Scratchpad Windows](https://www.reddit.com/r/i3wm/comments/61r7t8/show_all_scratchpad_windows_without_the_need_of/)
