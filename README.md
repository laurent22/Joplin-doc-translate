# Joplin-doc-translate

<!-- DONATELINKS -->
[![Donate using PayPal](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/badges/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=E8JMYD2LQ8MMA&lc=GB&item_name=Joplin+Development&currency_code=EUR&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHosted) [![Sponsor on GitHub](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/badges/GitHub-Badge.svg)](https://github.com/sponsors/laurent22/) [![Become a patron](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/badges/Patreon-Badge.svg)](https://www.patreon.com/joplin) [![Donate using IBAN](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/badges/Donate-IBAN.svg)](https://joplinapp.org/donate/#donations)
<!-- DONATELINKS -->

<img width="64" src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/LinuxIcons/256x256.png" align="left" /> **Joplin** is a free, open source note taking and to-do application, which can handle a large number of notes organised into notebooks. The notes are searchable, can be copied, tagged and modified either from the applications directly or from your own text editor. The notes are in [Markdown format](#markdown).

Notes exported from Evernote [can be imported](#importing) into Joplin, including the formatted content (which is converted to Markdown), resources (images, attachments, etc.) and complete metadata (geolocation, updated time, created time, etc.). Plain Markdown files can also be imported.

The notes can be securely [synchronised](#synchronisation) using [end-to-end encryption](#encryption) with various cloud services including Nextcloud, Dropbox, OneDrive and [Joplin Cloud](https://joplinapp.org/plans/).

Full text search is available on all platforms to quickly find the information you need. The app can be customised using plugins and themes, and you can also easily create your own.

The application is available for Windows, Linux, macOS, Android and iOS. A [Web Clipper](https://github.com/laurent22/joplin/blob/dev/readme/clipper.md), to save web pages and screenshots from your browser, is also available for [Firefox](https://addons.mozilla.org/firefox/addon/joplin-web-clipper/) and [Chrome](https://chrome.google.com/webstore/detail/joplin-web-clipper/alofnhikmmkdbbbgpnglcpdollgjjfek?hl=en-GB).

<div class="top-screenshot"><img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/home-top-img.png" style="max-width: 100%; max-height: 35em;"></div>

# Installation

Three types of applications are available: for **desktop** (Windows, macOS and Linux), for **mobile** (Android and iOS) and for **terminal** (Windows, macOS, Linux and FreeBSD). All the applications have similar user interfaces and can synchronise with each other.

## Desktop applications

Operating System | Download
---|---
Windows (32 and 64-bit) | <a href='https://github.com/laurent22/joplin/releases/download/v2.9.17/Joplin-Setup-2.9.17.exe'><img alt='Get it on Windows' width="134px" src='https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeWindows.png'/></a>
macOS | <a href='https://github.com/laurent22/joplin/releases/download/v2.9.17/Joplin-2.9.17.dmg'><img alt='Get it on macOS' width="134px" src='https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeMacOS.png'/></a>
Linux | <a href='https://github.com/laurent22/joplin/releases/download/v2.9.17/Joplin-2.9.17.AppImage'><img alt='Get it on Linux' width="134px" src='https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeLinux.png'/></a>

**On Windows**, you may also use the <a href='https://github.com/laurent22/joplin/releases/download/v2.9.17/JoplinPortable.exe'>Portable version</a>. The [portable application](https://en.wikipedia.org/wiki/Portable_application) allows installing the software on a portable device such as a USB key. Simply copy the file JoplinPortable.exe in any directory on that USB key ; the application will then create a directory called "JoplinProfile" next to the executable file.

**On Linux**, the recommended way is to use the following installation script as it will handle the desktop icon too:

<pre><code style="word-break: break-all">wget -O - https://raw.githubusercontent.com/laurent22/joplin/dev/Joplin_install_and_update.sh | bash</code></pre>

## Mobile applications

Operating System | Download | Alt. Download
---|---|---
Android | <a href='https://play.google.com/store/apps/details?id=net.cozic.joplin&utm_source=GitHub&utm_campaign=README&pcampaignid=MKT-Other-global-all-co-prtnr-py-PartBadge-Mar2515-1'><img alt='Get it on Google Play' height="40px" src='https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeAndroid.png'/></a> | or download the APK file: [64-bit](https://github.com/laurent22/joplin-android/releases/download/android-v2.9.8/joplin-v2.9.8.apk) [32-bit](https://github.com/laurent22/joplin-android/releases/download/android-v2.9.8/joplin-v2.9.8-32bit.apk)
iOS | <a href='https://itunes.apple.com/us/app/joplin/id1315599797'><img alt='Get it on the App Store' height="40px" src='https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeIOS.png'/></a> | -

## Terminal application

Operating system | Method
-----------------|----------------
macOS, Linux, or Windows (via [WSL](https://msdn.microsoft.com/en-us/commandline/wsl/faq?f=255&MSPPError=-2147217396)) | **Important:** First, [install Node 12+](https://nodejs.org/en/download/package-manager/).<br/><br/>`NPM_CONFIG_PREFIX=~/.joplin-bin npm install -g joplin`<br/>`sudo ln -s ~/.joplin-bin/bin/joplin /usr/bin/joplin`<br><br>By default, the application binary will be installed under `~/.joplin-bin`. You may change this directory if needed. Alternatively, if your npm permissions are setup as described [here](https://docs.npmjs.com/getting-started/fixing-npm-permissions#option-2-change-npms-default-directory-to-another-directory) (Option 2) then simply running `npm -g install joplin` would work.

To start it, type `joplin`.

For usage information, please refer to the full [Joplin Terminal Application Documentation](https://joplinapp.org/terminal/).

## Web Clipper

The Web Clipper is a browser extension that allows you to save web pages and screenshots from your browser. For more information on how to install and use it, see the [Web Clipper Help Page](https://github.com/laurent22/joplin/blob/dev/readme/clipper.md).

## Unofficial Alternative Distributions

There are a number of unofficial alternative Joplin distributions. If you do not want to or cannot use appimages or any of the other officially supported releases then you may wish to consider these.

However these come with a caveat in that they are not officially supported so certain issues may not be supportable by the main project. Rather support requests, bug reports and general advice would need to go to the maintainers of these distributions.

A community maintained list of these distributions can be found here: [Unofficial Joplin distributions](https://discourse.joplinapp.org/t/unofficial-alternative-joplin-distributions/23703)