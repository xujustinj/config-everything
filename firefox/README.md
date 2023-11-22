# Configure Firefox

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

### Google Scholar Button

[Google Scholar Button](https://addons.mozilla.org/firefox/addon/google-scholar-button/) adds a button to the toolbar that one can click to look up the current webpage on Google Scholar (i.e., to find a paper on Google Scholar).

- **Run in Private Windows** = `Don't Allow`

### Tree Style Tab

[Tree Style Tab](https://addons.mozilla.org/firefox/addon/tree-style-tab/) is a Firefox add-on for nested vertical-style tabs.

- **Run in Private Windows** = `Allow`

TST on its own looks pretty horrid because it does not (cannot) hide the Firefox UI elements that it is supposed to replace. We will need to do that manually instead:

1. Follow [this StackExchange answer](https://superuser.com/a/1619663) which explains how to create and use a `userChrome.css` file to hide the default Firefox tabs and the Tree Style Tab header.
2. Refer to [`userChrome.css`](./userChrome.css) for a CSS file that combines the best of all answers from the above StackExchange thread.

### uBlock Origin

[uBlock Origin](https://addons.mozilla.org/firefox/addon/ublock-origin/) is one of the many ad-blockers, but it's the one I happen to use. No good reason.

- **Run in Private Windows** = `Allow`
