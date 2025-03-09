> A modular UI customization for Firefox, removing borders in the favor of shadows to emphasize the layer elevation.

![Preview](assets/preview.gif "Preview")

## Install

1. Set Firefox theme to `Dark` in: Firefox settings > Extensions & Themes > Themes.
2. Go to `about:config` (in the URL bar) and set `toolkit.legacyUserProfileCustomizations.stylesheets = true`.
3. Go to `about:support` > Search for "Profile Directory" > Open > Copy the "chrome" folder to this location.
4. Restart Firefox.
5. *(Optional)* Vertical tabs using Sidebery:
    * Go to `about:config` and set `sidebar.revamp = false`.
    * Install the [Sidebery extension](https://addons.mozilla.org/en-US/firefox/addon/sidebery/).
    * Go to Sidebery settings (right-click extension) > Help > Import addon data > Choose file `sidebery/settings.json`.
    * *(Optional)* For tab previews: Sidebery settings > Search for "Tabs preview" > Enable and grant permissions.

## Uninstall

Set `toolkit.legacyUserProfileCustomizations.stylesheets = false` or delete the `chrome` folder from the profile.\
For Sidebery: Sidebery settings > Help > Reset settings.

## Customization

* It's recommended that additions or updates of the default styles to be done in the following files (which should be created by you). This way, your local changes will persist when this repository is updated.
    * `chrome/DownToneUI/override_chrome.css` for changes to `chrome/userChrome.css`
    * `chrome/DownToneUI/override_content.css` for changes to `chrome/userContent.css`
* Changing the color scheme:
    * This can be done in `chrome/DownToneUI/_globals.css` by modifying the `--dtui-theme` variables.
    * **NOTE:** if vertical tabs are used, these changes also have to be applied to: Sidebery settings > Style editor.
* See [addons](addons/) for some modifications of the defaults. The content of these files is intended to be copied as follows:
    * `chrome_` files to `chrome/DownToneUI/override_chrome.css`
    * `content_` files to `chrome/DownToneUI/override_content.css`
    * `sidbery_` files to Sidebery's Style editor (at the end)

## Notes

* To open the sidebar tabs (in case you've gone to History or entered Private Mode): click on the Sidebery extension or use shortcut CTRL+E (shortcut is not working in Windows).

## Credits

* Contributors to the [firefox-csshacks](https://github.com/MrOtherGuy/firefox-csshacks) repository and [Zen Browser](https://zen-browser.app) for some ideas.
* Community on [/r/FirefoxCSS](https://www.reddit.com/r/FirefoxCSS/) for the various snippets of information.
