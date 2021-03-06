<div align="center">
    <img src="https://github.com/godbout/Wooshy.docs/blob/master/assets/icon.png">
    <h1>Instant search through the macOS UI, and clicks.</h1>
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

Wooshy will search through UI elements' metadata, i.e. labels, titles, values, tooltips, types etc.

Wooshy's philosophy is to avoid navigation.
Rather, you do a gross search, and if needed you narrow down to (hopefully) the specific target you want.
That sounds slower but it's actually way more natural. The way it works is:

1. you type part of what you're looking for
2. if you have multiple results, you narrow down the results with a... _narrower_

E.g. you want something with `bacon`:

|  term             | narrower   | matches                                                    | whole typing                                   
| :---:             | :---:      |  :---:                                                     | :---:
| `bacon`           |            | anything that contains "bacon" (will not match pig sorry)  | `bacon`
| `bacon`           | `^`        | anything that starts with "bacon"                          | `bacon ^` 
| `bacon`           | `$`        | anything that ends with "bacon"                            | `bacon $`
| `bacon`           | `!`        | anything that is exactly "bacon"                           | `bacon !`
| `the bacon`       | `tab`      | anything that contains "the bacon" and is a tab :))        | `the bacon tab`

**You do NOT need to type the whole search term or narrower**. You can type `bac butt` for a bacon button. Actually even `b b` might get your target, depending on the context.
But you currently need to type your letters in order, space included. There's no fuzzy matching. It may come later, but from experience, typing letters in order is faster than _thinking_ how to fuzzy match. You don't want to think. (At least not in this context.)

The term can also be:
1. a star???`*`???that will show all the UI elements that you can target
2. a type of UI element. Don't think too much, just start typing. E.g.: tab, radio, checkbox, button, pop up, toggle, switch, etc. Again, you do not need to type the whole thing. `check`, or `ch` will probably find all the checkboxes.

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

What would be Wooshy without all the clicks.

If The Input??? is empty, Wooshy will click at the current mouse position. Else, it'll go click the Primary Target. The available clicks are:

| keyboard               | mouse equivalent | 
| :---:                  | :---: 
| `return`               | left click
| `control return`       | right click
| `option return`        | option click
| `shift return`         | shift click
| `command return`       | command click

You can also just move the mouse without clicking. It is less fun though:

| keyboard               | mouse equivalent | 
| :---:                  | :---: 
| `shift command return` | run over there 

# Need to bring any macOS window to the foreground?

Try our free, open-source Alfred Workflow: [Wooshy: Window to the Foreground!](https://github.com/godbout/WooshyWindowToTheForeground).

# Roadmap

## alpha/beta

- [x] video explaining the Search and Target Navigation
- [ ] show possible matching terms for any potential Target while hovering over them when The Input is showing.
This is necessary for Targets that don't have text like icons, images, etc.
- [x] multi monitors support
- [x] find a way to make the Targets stand out on light backgrounds
- [ ] improve clicking. some places don't register the click (e.g. App Store, own account at bottom left)
- [x] **this has been done as an [Alfred Workflow](https://github.com/godbout/WooshyWindowToTheForeground)**.~~(30%) find a way to bring any visible window to the foreground and become the frontmost window.~~
- [ ] handle double clicks. at first i thought it was not necessary as you can open anything with `???o` but some places, at least in the new macOS Ventura, require double clicks (shit iOS-style bs)
- [ ] be able to target Notifications

## v1+

- [ ] add a mode without The Input showing, so that focus is not stolen from macOS.
this will allow using Wooshy for menu contents, popovers, notifications, etc.
but will require the user to type more properly (can still show what is typed a la kV Characters Window, and allow for delete of last character, etc.).
- [ ] allow customization of Targets visual properties

## maybe

- [ ] (70%) fuzzy search. maybe not wholly fuzzy, but also not just the first letter of words. more like you can type the beginning of a word, a space, and the beginning of another word
- [ ] (10%) grab not only Targets from the frontmost window, but all visible windows.
(although that may pollute the results and ultimately be harder to reach what one wants.)
- [ ] (2%) OCR support.
through the Accessibility we grab whole objects, but not specific words in text.
sometimes we may want to target a specific word, or to access objects that are not accessible (e.g. the individual sections in Alfre's Preferences sidebar).

# Alternatives

* [Shortcat](https://shortcatapp.com) (closed source, one time purchase)
* [Vimac](https://github.com/dexterleng/vimac) (open source, free)
* [Homerow](https://www.homerow.app) (closed source, one time purchase)
* [Superkey](https://superkey.app) (closed source, one time purchase)
