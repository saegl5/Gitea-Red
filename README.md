# Gitea-Red

~~Soft~~, Lite and dark red theme. Utilizes Gitea's default themes but with some colors and images from the Gitea-Red-Silver fork.

## Directions

01. Locate your custom directory: Site Administration > Configuration > Custom File Root Path (e.g., /var/lib/gitea/custom)
02. Verify if a public directory exists within the custom directory
03. If the public directory exists, make sure it contains two directories: css and img
04. If the css and img directories do not exist, then create them
05. To add just the themes (not the red Gitea logos), copy [theme-auto-red.css](./public/css/theme-auto-red.css), [theme-red.css](./public/css/theme-red.css), and [theme-arc-red.css](./public/css/theme-arc-red.css) into the css directory
06. To add the red Gitea logos, backup any existing img directory, and copy all the [logos](./public/img/) into your img directory
07. Locate your configuration file: Site Administration > Configuration > Configuration File Path (e.g., /etc/gitea/app.ini)
08. Add to the configuration file:
    ```ini
    [ui]
    THEMES = auto,gitea,arc-green,auto-red,red,arc-red
    DEFAULT_THEME = auto-red
    ```
09. Restart Gitea
10. Existing users: Go to user Settings > Appearance > change default theme

## Photos

Red (Original) \
<img src='./screenshots/home_lite.png' alt="home lite" width="704"/> \
<img src='./screenshots/repo_lite.png' alt="repo lite" width="704"/> \
(redacted)

Arc-Red \
<img src='./screenshots/home_dark.png' alt="home dark" width="704"/> \
<img src='./screenshots/repo_dark.png' alt="repo dark" width="704"/> \
(redacted)

> Disable the Dark Reader web browser extension for your website.

## Known Issue

- [x] Checkmark is not displayed, when fork a repository and select "Make Repository Private." I submitted an issue: [https://github.com/go-gitea/gitea/issues/25076](https://github.com/go-gitea/gitea/issues/25076) Now, a fix is coming: [pull request #25573](https://github.com/go-gitea/gitea/pull/25573). Fixed in [Gitea 1.20.0](https://github.com/go-gitea/gitea/releases/tag/v1.20.0)

Theme coded with &#9829; in VSCodium