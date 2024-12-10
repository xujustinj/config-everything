# Configure Firefox

## Warning

Firefox is one of those programs that will use as much memory as it can get, and then some more.
At very high memory loads, swap thrashing will begin.
After this point, pray that you can find some program to sacrifice to unlock some memory, otherwise you will either need to kill Firefox or kill the whole computer, taking Firefox with it.

## Settings

Can be found at `about:preferences`.

- **General**
  - **Startup**
    - **Open previous windows and tabs** = `true`
- **Home**
  - **Firefox Home Content**
    - **Shortcuts** = `true`
      - **Sites you save or visit** = `4 rows`
      - **Sponsored shortcuts** = `false`
    - **Recommended by Pocket** = `false`
      - **Sponsored Stories** = `false`
    - **Recent activity** = `false`
    - **Snippets** = `false`
- **Privacy & Security**
  - **HTTPS-Only Mode** = `Enable HTTPS-Only Mode in all windows`
  - **DNS over HTTPS**
    - **Enable secure DNS using:** = `Max Protection`
      - **Choose provider:** = `Cloudflare`

## Extensions

### Dashlane

[Dashlane](https://addons.mozilla.org/firefox/addon/dashlane/) is a Firefox add-on for managing passwords and other secrets.

- **Run in Private Windows** = `Don't Allow`

### DF YouTube (Distraction Free)

[DF YouTube (Distraction Free)](https://addons.mozilla.org/firefox/addon/df-youtube/) uses [uBlock Origin](#ublock-origin) to eliminate distracting elements on YouTube.

- **Hide Notification Bell** = `true`
- **Hide Feed** = `true`
- **Disable Autoplay** = `true`
- **Hide Trending Tab** = `true`
- **Hide Subscriptions Bar** = `false`
  - **Show Only Library/Lists** = `true`
- **Hide Related Videos (end of video)** = `true`
- **Hide Sidebar** = `true`
  - **Hide Live Chat** = `true`
  - **Hide Playlists** = `false`
- **Hide Merch** = `true`
- **Hide Comments** = `true`
- **Disable Playlists** = `false`

- **Run in Private Windows** = `Don't Allow`

### Google Scholar Button

[Google Scholar Button](https://addons.mozilla.org/firefox/addon/google-scholar-button/) adds a button to the toolbar that one can click to look up the current webpage on Google Scholar (i.e., to find a paper on Google Scholar).

- **Run in Private Windows** = `Don't Allow`

### Return YouTube Dislike

[Return YouTube Dislike](https://addons.mozilla.org/firefox/addon/return-youtube-dislikes/)

- **Run in Private Windows** = `Don't Allow`

### Tree Style Tab

[Tree Style Tab](https://addons.mozilla.org/firefox/addon/tree-style-tab/) is a Firefox add-on for nested vertical-style tabs.

- **Run in Private Windows** = `Allow`

TST on its own looks pretty horrid because it does not (cannot) hide the Firefox UI elements that it is supposed to replace. We will need to do that manually instead:

1. Follow [this StackExchange answer](https://superuser.com/a/1619663) which explains how to create and use a `userChrome.css` file to hide the default Firefox tabs and the Tree Style Tab header.
2. Refer to [`userChrome.css`](./userChrome.css) for a CSS file that combines the best of all answers from the above StackExchange thread.

- **Unlock Expert Options** = `true`
- **Appearance**
  - **Shift tabs aside to keep in-tab buttons touchable avoiding covered with the auto-shown scrollbar** = `2px`
- **Context Menu**
  - **Additional Tab Context Menu Options**
    - **Top Menu** = `Close this Tree`, `Bookmark this Tree`
    - **Sub Menu** = nothing
  - **Allow to read and create bookmarks** = `true`
- **Tabs opened from Existing Tabs**
  - **When a tab is opened from existing tab, open it as** = `Next Sibling of the parent tab`
  - **Auto-group tabs opened from same pinned tab** = `false`

### TST More Tree Commands

- **Run in Private Windows** = `Allow`

- **Visible command in the context menu** = `Create New Group from tabs`

### uBlock Origin

[uBlock Origin](https://addons.mozilla.org/firefox/addon/ublock-origin/) is one of the many ad-blockers, but it's the one I happen to use. No good reason.

- **Run in Private Windows** = `Allow`
