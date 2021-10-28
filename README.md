# Sources for Android SDK

[![Latest API](https://img.shields.io/badge/API-Sv2-blue)](https://developer.android.com/studio/releases/platforms)
[![Download Package](https://img.shields.io/badge/Download-zip-red)](/../../releases/download/vSv2_1635419665/sources-Sv2.zip)
![Total number of downloads](https://img.shields.io/github/downloads/ni554n/sources-for-android-sdk/total?color=eeeeee&label=)

The `Sources for Android SDK` package provides instant access to the documentation and source code of the `android.jar` classes in Android Studio.

Unfortunately, this package does not become available during the Developer Preview, which slows down debugging and development while test-driving the upcoming `compileSdkVersion`.

But in the meantime, this Github Actions workflow can build a package from a developing branch of the [SDK platform source repo](https://android.googlesource.com/platform/frameworks/base). This package can also be updated normally using the SDK updater when the official version becomes available.

You can enable Github [Release Watch](.images/watch-release.png) to get notified when a new build gets released on this repo.

## Usage

1. Download and extract the `android-Sv2` folder from the package
2. Move the extracted folder into the [Android SDK Location's](.images/sdk-location.jpg) `/sources` directory.
3. Restart Android Studio.

## Build

1. Fork this repo on Github.
2. [Create a new token](https://github.com/settings/tokens/new?scopes=repo&description=Sources%20for%20Android%20SDK) with **_No expiration_**.
3. Go to the [Repo Actions Secrets](/../../settings/secrets/actions/new) and add the generated token named as `PAT`.
4. Now go to the [Actions Workflow](/../../actions/workflows/build-package.yml) and select `Run workflow` dropdown menu.
5. Set a *Platform Source Branch Name* from the [Google Android Source Repo](https://android.googlesource.com/platform/frameworks/base), *API Level* and *Version Name* (optional).
6. Run the workflow and wait for the package to appear on the [Releases](/../../releases).

## Acknowledgements

Based on the build instructions from [this gist](https://gist.github.com/cketti/210bb18b6e6112135b7b6468754901bf).

## Information

**Author:** [Nissan Ahmed](https://ni554n.github.io) ([@ni554n](https://twitter.com/ni554n))

**Donate:** [PayPal](https://paypal.me/ni554n)
