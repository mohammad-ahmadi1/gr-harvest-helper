# Harvest Issue Board Plugin

This extension adds a Harvest time tracking button for Jira, Zammad and GitLab issues (active sprints page, issue page). No synchronization to the webpage is done, all data stays in Harvest.

- [Chrome Store](https://chrome.google.com/webstore/detail/jira-harvest-time-trackin/klgljijecjfkdfobihclllkadmoeokgg)
- [Mozilla Addons](https://addons.mozilla.org/de/firefox/addon/jira-harvest-helper)

# Usage

Select the ticket, then click on the extension icon in the upper right corner. A popup will open where you can specify project and task and set the desired starting time (which defaults to now). A permanent link to the selected issue will be added to the Harvest item automatically.

Earlier versions of this plugin displayed a time tracking button on Jira — this got removed. [Details](docs/on-page-tracker.md).

# Why this project was started

The official [harvest-jira](https://www.getharvest.com/apps-and-integrations/jira) integration is done via a Jira plugin — which might not be possible or desirable in some cases (for example you don't have an admin account on your client's Jira instance).

# Screenshot

![Example](./docs/images/modalImage.png)

# Install the development version

## For Chrome:

- Get the code:
  - Either clone this repo (`git clone git@github.com:GreyRook/gr-harvest-helper.git`)
  - Or download as a zip and unzip it (`https://github.com/GreyRook/gr-harvest-helper/archive/master.zip`)
- Go to Chrome's extensions page (`chrome://extensions/`)
- Disable the Chrome Store version of this extension (if installed)
- Enable developer mode via the toggle in the top right
- Click on "Load unpacked" (top left button) and choose the folder of the cloned repo

## For Firefox:

### Development/Testing:
- Get the code (same as above)
- Open Firefox and navigate to `about:debugging#/runtime/this-firefox`
- Click on "Load Temporary Add-on..."
- Navigate to the extension folder and select the `manifest.json` file
- The extension should now be loaded!

### Package for Firefox Add-ons:
To submit to [Mozilla Add-ons](https://addons.mozilla.org/developers/):

1. Create a zip package from the project directory:
   ```bash
   zip -r gr-harvest-helper-firefox.zip .
   ```

2. Upload `gr-harvest-helper-firefox.zip` to [Firefox Add-ons Developer Hub](https://addons.mozilla.org/developers/addon/submit/)

For more detailed Firefox instructions, see [FIREFOX_INSTALL.md](FIREFOX_INSTALL.md)
