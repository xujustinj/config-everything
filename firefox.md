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

### Tree-Style Tab

[Tree Style Tab](https://superuser.com/a/1424494) is a Firefox add-on for nested vertical-style tabs.

1. Follow [this StackExchange answer](https://superuser.com/a/1619663) which explains how to create and use a `userChrome.css` file to hide the default Firefox tabs and the Tree Style Tab header.
2. Refer to [`userChrome.css`](./userChrome.css) for a CSS file that combines the best of all answers from the above StackExchange thread.
