<div align="center">
    <img src="https://github.com/godbout/Wooshy.docs/blob/master/assets/icon.png">
    <h1>Search instantly through the macOS UI. Then click. Or copy.</h1>
</div>

![awesome stuff happening in there again](https://raw.githubusercontent.com/godbout/Wooshy.docs/master/assets/gif.gif "hehe again")

---

# The Site

[wooshy.app](https://wooshy.app) for the handsome marketing thing. Looks like it's using Comic Sans MS but it's not, I swear.

# License

The alphas and betas are free (of course!) and have an expiry date of currently 30 days.
Once v1 is out, the License is a mere coffee a month (USD$3.28 excl. tax).
You'll still be able to use Wooshy without a subscription, but it will take some naps as the day goes by. Software have feelings too!

# Manual

## Search

Wooshy searches through UI elements' metadata, i.e. labels, titles, values, tooltips, placeholders, types etc.
Some of this metadata is visible on the screen, while some is hidden behind the scenes. Currently you can see the hidden metadata with the Accessibility Inspector that comes bundled with Xcode. At a later stage—before the v1 release—an integrated solution will be available in Wooshy.

Wooshy's philosophy is to avoid navigation.
Rather, you start with a gross search—just a few letters—and if needed you narrow down to the specific target you want to reach by typing a few more letters.
This is possible thanks to: 

1. fuzzy matching: Wooshy will look for parts of different words, in any order. it's up to you
2. role search: you can specify the role of the UI element you want, again in any order

So basically the best way to use Wooshy is: 1) you type a bit 2) if you've reached your Target, congratulations 3) if not, continue your current word, or add a new one to the search by adding a space, and start typing more 3) keep doing until you reach your Target 4) or you can also navigate between the Targets highlighted.

If that sounds complicated, just have a look at the examples below:

https://user-images.githubusercontent.com/121373/183301798-b1d8425e-bbe0-4a31-93bf-21ad3ea1495e.mp4

https://user-images.githubusercontent.com/121373/183301804-cf157bfa-ad0b-46d7-9eec-301fab48088e.mp4

The term can also be a star—`*`—that will show you all the UI elements that you can target.

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

If you use [kindaVim](https://github.com/godbout/kindaVim.docs), add Wooshy to the `Key Mapping` Family. Then you'll be able to navigate with Vim moves by entering Normal Mode and:

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

| keyboard               | on the Primary Target |
| :---:                  | :---: 
| `return`               | `left click`
| `control return`       | `right click`
| `option return`        | `option click`
| `shift return`         | `shift click`
| `command return`       | `command click`

If The Input™ is empty and therefore no Primary Target is selected, Wooshy will click at the current mouse position instead. Magic!

## Just Move the Mouse

You can also just move the mouse without clicking. It is less fun though:

| keyboard               | mouse equivalent | 
| :---:                  | :---: 
| `shift command return` | run over there 

## Copy

`⌘C` on a Primary Target will copy the visible (or descriptive for icons, images, etc.) text.
Add any modifier key (`⌃`, `⌥`, or `⇧`) to `⌘C` to copy the metadata instead, i.e., the URL for links, status for checkboxes, tabs, radiobuttons, etc.

# APIs

Wooshy sends [Distributed Notifications](https://developer.apple.com/documentation/foundation/distributednotificationcenter) to macOS when you activate and deactivate The Input.
You can listen to those Notifications with external tools like [BetterTouchTool](https://www.google.com/search?q=bettertouchtool) or [Hammerspoon](https://www.hammerspoon.org) and build your own custom workflows as a result of those Notifications.

The Notifications Names are:
* WooshyInputDidAppear
* WooshyInputDidDisappear

# Need to bring any macOS window to the foreground?

Try our free, open-source Alfred Workflow: [Wooshy: Window to the Foreground!](https://github.com/godbout/WooshyWindowToTheForeground).

# Roadmap

## alpha/beta

- [x] video explaining the Search and Target Navigation
- [ ] show possible matching terms for any potential Target while hovering over them when The Input is showing.
This is necessary for Targets that don't have text like icons, images, etc.
- [x] multi monitors support (current Targets and clicks supported, but not Input position)
- [x] find a way to make the Targets stand out on light backgrounds
- [x] improve clicking. some places don't register the click (e.g. App Store, own account at bottom left)
- [x] **this has been done as an [Alfred Workflow](https://github.com/godbout/WooshyWindowToTheForeground)**.~~(30%) find a way to bring any visible window to the foreground and become the frontmost window.~~

## v1+

- [ ] add a mode without The Input showing, so that focus is not stolen from macOS.
this will allow using Wooshy for menu contents, popovers, notifications, etc.
- [ ] handle double clicks. at first i thought it was not necessary as you can open anything with `⌘o` but some places, at least in the new macOS Ventura, require double clicks (shit iOS-style bs)
but will require the user to type more properly (can still show what is typed a la kV Characters Window, and allow for delete of last character, etc.).
- [ ] ~~allow customization of Targets visual properties~~

## maybe

- [x] (70%) fuzzy search. maybe not wholly fuzzy, but also not just the first letter of words. more like you can type the beginning of a word, a space, and the beginning of another word
- [ ] ~~(10%) grab not only Targets from the frontmost window, but all visible windows.
(although that may pollute the results and ultimately be harder to reach what one wants.)~~
- [ ] ~~(2%) OCR support.
through the Accessibility we grab whole objects, but not specific words in text.
sometimes we may want to target a specific word, or to access objects that are not accessible (e.g. the individual sections in Alfre's Preferences sidebar).~~

# Alternatives

* [Shortcat](https://shortcatapp.com) (closed source, one time purchase)
* [Vimac](https://github.com/dexterleng/vimac) (open source, free)
* [Homerow](https://www.homerow.app) (closed source, one time purchase)
* [Superkey](https://superkey.app) (closed source, one time purchase)
* [VimMotionApp](https://github.com/dwarvesf/VimMotionApp) (closed source, free)
