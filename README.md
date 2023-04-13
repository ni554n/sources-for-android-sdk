# Sources for Android SDK

[![Latest API](https://img.shields.io/badge/API-33-blue)](https://developer.android.com/studio/releases/platforms)
[![Download Package](https://img.shields.io/badge/Download-zip-red)](/../../releases/download/v33_1654803276/sources-33.zip)
![Total number of downloads](https://img.shields.io/github/downloads/ni554n/sources-for-android-sdk/total?color=eeeeee&label=)

The `Sources for Android SDK` package provides instant access to the documentation and source code of system framework in Android Studio. Without this package, documentations will be loaded from network, and system classes has to be decompiled when you `ctrl + click` on them to view the source.

Unfortunately, this package does not become available during the Developer Preview, which slows down debugging and development while test-driving the upcoming `compileSdkVersion`. This GitHub Actions workflow can build that package from a developing branch of the [SDK platform source repo](https://android.googlesource.com/platform/frameworks/base).

This package can also be updated normally using the SDK updater when the official version becomes available. But my recommendation is to uninstall this package from the SDK Manager first; otherwise it takes a long time to install the update due to the patching mechanism of SDK update.

You can enable GitHub [Release Watch](.images/watch-release.png) to get notified when a new build gets released on this repo.

## Usage

1. Download the package from [Releases](/../../releases) and extract the `android-33` folder from the package
2. Move the extracted folder into the [Android SDK Location's](.images/sdk-location.jpg) `/sources` directory.
3. Restart Android Studio.

## Build Yourself

1. [Fork](https://github.com/ni554n/sources-for-android-sdk/fork) this repo on GitHub.
2. [Create a new token](https://github.com/settings/tokens/new?scopes=repo&description=Sources%20for%20Android%20SDK) with **_No expiration_**.
3. Go to the [Repo Actions Secrets](/../../settings/secrets/actions/new) and add the generated token named as `PAT`.
4. Now go to the [Build Android SDK Sources Package Workflow](/../../actions/workflows/build-package.yaml) and select `Run workflow` dropdown menu.
5. Pick and enter a <u>Platform Source Branch Name</u> from the [Google Android Source Repo](https://android.googlesource.com/platform/frameworks/base), <u>API Level</u> and <u>Version Name</u> (optional).
    > _API Level_ should be Integer only. Builds with String levels like _UpsideDownCake_ don't get recognized in Android Studio.
6. Run the workflow and wait for the package to appear on the [Releases](/../../releases).

## Acknowledgements

Based on the build instructions from [this gist](https://gist.github.com/cketti/210bb18b6e6112135b7b6468754901bf).

## Information

**Author:** [Nissan Ahmed](https://ni554n.github.io) ([@ni554n](https://twitter.com/ni554n))

**Donate:** [PayPal](https://paypal.me/ni554n)
