<div align="center">
    <img src="https://github.com/godbout/Wooshy.docs/blob/master/assets/icon.png">
    <h1>Search instantly through the macOS UI. Then click. Or copy.</h1>
</div>

![awesome stuff happening in there again](https://raw.githubusercontent.com/godbout/Wooshy.docs/master/assets/gif.gif "hehe again")

---

# The Site

[wooshy.app](https://wooshy.app) for the handsome marketing thing. Looks like it's using Comic Sans MS but it's not, I swear.

# License

Wooshy is young and tends to take random naps 🥺️
If you're willing to let him take a rest from time to time then you're all set.
Else you may consider treating Wooshy [one coffee a month](https://subscribe.wooshy.app).
Yes software have feelings but hey Wooshy time to grow up!

# Manual

## Search

### What does Wooshy search through?

Wooshy searches through UI elements' metadata, i.e. labels, titles, values, tooltips, placeholders, types etc.
Some of this metadata is visible on the screen, while some is hidden behind the scenes. 
To discover all the terms you can use to reach a Target, check out [The Inspector 🕵️‍♂️️](#the-inspector-%EF%B8%8F%EF%B8%8F%EF%B8%8F)

### The Art of Searching

**Wooshy's philosophy is to avoid navigation**.
Rather, you start with a gross search—just a few letters—and if needed you narrow down to the specific target you want to reach by typing a few more letters.
This is possible thanks to: 

1. fuzzy matching: Wooshy will look for parts of different words, in any order. it's up to you
2. role search: you can specify the role of the UI element you want, again in any order

So basically the best way to use Wooshy is: 1) you type a bit 2) if you've reached your Target, congratulations 3) if not, continue your current word, or add a new one to the search by adding a space, and start typing more 3) keep doing until you reach your Target 4) or you can also navigate between the Targets highlighted.

For example to specifically target a `Log in` button, you could type `log but`. See the videos below for more examples:

https://user-images.githubusercontent.com/121373/183301798-b1d8425e-bbe0-4a31-93bf-21ad3ea1495e.mp4

https://user-images.githubusercontent.com/121373/183301804-cf157bfa-ad0b-46d7-9eec-301fab48088e.mp4

The term can also be a star—`*`—that will show you all the UI elements that you can target.

## The Inspector 🕵️‍♂️️

While Wooshying, hover over potential Targets to get The Inspector 🕵️‍♂️️ to investigate and let you know which terms will reach them.
Especially useful for icons, images, buttons without text, etc. But you can use it anywhere to perfect your search skills on pages or apps that you use frequently.
You can also call The Inspector 🕵️‍♂️️ with [your keyboard](#call-the-inspector-%EF%B8%8F%EF%B8%8F%EF%B8%8F).

https://user-images.githubusercontent.com/121373/197319091-6ade5f0f-5647-4cf2-af9a-b799cb27ebb7.mp4

## Navigate

If you still need or want to navigate through the results, you can with:

| target          | key | 
| :---:           | :---:
| next            | `tab` or `down` or `control n`
| previous        | `shift tab` or `up` or `control p`
| first           | `command up`
| last            | `command down`
| halfway up      | `control up`
| halfway down    | `control down`

If you use [kindaVim](https://github.com/godbout/kindaVim.docs), then you'll be able to navigate with Vim moves by entering Normal Mode and:

| target          | kindaVim move | 
| :---:           | :---: 
| next            | `j` or `down` or `control j` or `control n`
| previous        | `k` or `up` or `control p`
| first           | `gg`
| last            | `G`
| halfway up      | `control b` or `control u` 
| halfway down    | `control f` or `control d`

## Click

What would be Wooshy without all the clicks:

| keyboard                                          | on the Primary Target |
| :---:                                             | :---: 
| `return`                                          | `left click`
| `control return`                                  | `right click`
| `option return`                                   | `option click`
| `shift return`                                    | `shift click`
| `command return`                                  | `command click`
| `fn return` or `control option command return`    | `double left click`

If The Input™ is empty and therefore no Primary Target is selected, Wooshy will click at the current mouse position instead. Magic!

## Just Move the Mouse

You can also just move the mouse without clicking. It is less fun though:

| keyboard               | mouse equivalent | 
| :---:                  | :---: 
| `shift command return` | run over there 

## Call The Inspector 🕵️‍♂️️

| keyboard                                          | on the Primary Target |
| :---:                                             | :---: 
| `command h` or `command i` or `shift command /`   | show The Inspector 🕵️‍♂️️'s discoveries

## Copy

`⌘C` on a Primary Target will copy the visible (or descriptive for icons, images, etc.) text.
Add any modifier key (`⌃`, `⌥`, or `⇧`) to `⌘C` to copy the metadata instead, i.e., the URL for links, status for checkboxes, tabs, radiobuttons, etc.

# APIs

## Distributed Notifications

Wooshy sends [Distributed Notifications](https://developer.apple.com/documentation/foundation/distributednotificationcenter) to macOS when you activate and deactivate The Input.
You can listen to those Notifications with external tools like [BetterTouchTool](https://www.google.com/search?q=bettertouchtool) or [Hammerspoon](https://www.hammerspoon.org) and build your own custom workflows as a result of those Notifications.

The Notifications Names are:
* WooshyInputDidAppear
* WooshyInputDidDisappear

## Custom URLs

You can control Wooshy programmatically by calling the following Custom URLs:
* open The Input: `wooshy://openTheInput`
* close The Input: `wooshy://closeTheInput`
* toggle The Input: `wooshy://toggleTheInput`

You can pass a URL query to fill The Input and start searching through UI Elements right away:
* open: `wooshy://openTheInput?with=rick%20astley`
* toggle: `wooshy://toggleTheInput?with=ryan%reynolds`


# Need to bring any macOS window to the foreground?

Try our free, open-source Alfred Workflow: [Wooshy: Window to the Foreground!](https://github.com/godbout/WooshyWindowToTheForeground).

# Alternatives to Wooshy

* [Shortcat](https://shortcatapp.com) (closed source, one time purchase)
* [Vimac](https://github.com/dexterleng/vimac) (open source, free)
* [Homerow](https://www.homerow.app) (closed source, one time purchase)
* [Superkey](https://superkey.app) (closed source, one time purchase)
* [VimMotionApp](https://github.com/dwarvesf/VimMotionApp) (closed source, free)
