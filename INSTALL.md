# Install 4789 for iPhone

**The first public beta is being prepared. No IPA has been published yet.**

This guide explains the installation process for the forthcoming release. It does not provide an
installable app today. Use the [official Releases page](https://github.com/4789-app/4789-ios-releases/releases)
for published files, version/build metadata, checksums, and known limitations. The
[website installation guide](https://4789library.com/install) presents the same process.

## Before you start

- An iPhone running iOS 26 or later, with a passcode.
- Your Apple Account and access to its authentication prompts. No paid developer account or
  jailbreak is required. You do not need a 4789 account.
- A Mac or Windows computer and USB cable for initial sideloader setup, plus Wi-Fi.
- Time to complete setup and confirm the app opens before disconnecting.

The public IPA must be signed with your Apple Account using a sideloading tool. Enter that account
only in your chosen tool's authentication flow; 4789 does not receive it.
**Downloading an IPA in Safari or opening it in Files does not install it.**

Already have a working SideStore or AltStore Classic installation? Continue to
[download and import](#download-and-import-the-ipa). Otherwise, save this page and open it on your
computer to set up one of these tools.

| Tool | Initial setup | Later installs and refreshes |
| --- | --- | --- |
| SideStore | Computer, USB, iloader | On iPhone with Wi-Fi and LocalDevVPN connected |
| AltStore Classic | Computer, USB, AltServer | AltServer running and reachable over USB or the same Wi-Fi network |
| Sideloadly | Computer and USB | Computer running, iPhone reachable over USB or configured Wi-Fi |

## Set up SideStore

1. Follow the [official prerequisites](https://docs.sidestore.io/docs/installation/prerequisites)
   for your computer. Install iloader there and LocalDevVPN on your iPhone. Windows also needs the
   Apple device software listed in that guide.
2. Connect your unlocked iPhone by USB and accept **Trust This Computer**. In iloader, sign in,
   select your iPhone, then choose **Install SideStore (Stable)**.
3. Follow the [official installation guide](https://docs.sidestore.io/docs/installation/install)
   to trust the developer app and enable Developer Mode. The shared settings path is below.
4. Connect LocalDevVPN, open SideStore, and sign in with the same Apple Account. In **My Apps**,
   refresh SideStore itself before importing 4789.

For later installs, updates, and refreshes, keep Wi-Fi and LocalDevVPN connected. Refresh both
SideStore and 4789. If pairing expires, including after an iOS update or reset, return to the
official guide to repair it using your computer.

## Set up AltStore Classic

1. Install AltServer using the [official Mac guide](https://faq.altstore.io/altstore-classic/how-to-install-altstore-macos)
   or [official Windows guide](https://faq.altstore.io/altstore-classic/how-to-install-altstore-windows).
   Windows setup includes specific iTunes and iCloud prerequisites; use that guide's downloads.
2. Connect your unlocked iPhone by USB and accept **Trust This Computer**. Enable Wi-Fi sync in
   Finder on Mac or iTunes on Windows.
3. From AltServer's menu-bar or system-tray icon, choose **Install AltStore**, select your iPhone,
   and authenticate with your Apple Account.
4. Trust the developer app and enable Developer Mode below. Open AltStore Classic and sign in.
5. Keep AltServer running and reachable when importing or refreshing 4789. Use **My Apps → Refresh
   All** and confirm success. See [AltStore's refresh guidance](https://faq.altstore.io/altstore-classic/your-altstore).

## Install with Sideloadly

1. Download Sideloadly from its [official website](https://sideloadly.io/). Follow the Windows
   iTunes and iCloud prerequisites there if applicable.
2. Once released, download the verified 4789 IPA to your computer.
3. Connect your unlocked iPhone by USB and accept **Trust This Computer**.
4. Open Sideloadly, select the iPhone, drag in the IPA, and enter your Apple Account. Start the
   installation and complete authentication prompts in the tool.
5. Trust the developer app and enable Developer Mode below, then open 4789.
6. Configure automatic refresh or repeat the signing install before expiry. Wireless refresh
   requires the tool's Wi-Fi setup and both devices on the same network.

## Download and import the IPA

These steps apply **after** a verified public release is published.

1. Open the [official Releases page](https://github.com/4789-app/4789-ios-releases/releases).
   Read the release's requirements and known limitations. Download its IPA and checksum file;
   check the version, build, file size, and SHA-256 against the release metadata.
2. On iPhone, Safari downloads appear in **Files → Downloads**, under iCloud Drive or On My iPhone,
   depending on your settings. Wait for the entire download to finish.
3. In SideStore or AltStore Classic, open **My Apps**, tap **+**, and choose the IPA from Files.
   Keep the connection required by that tool active until installation completes. Sideloadly
   uses the computer flow above instead.
4. If the release provides an official source feed, you may add that exact feed through your
   sideloader's Sources interface. Use only the feed linked by the release; none is available yet.

To check a downloaded file on a computer, replace the example path with its actual location and
compare the complete hash to the published checksum:

Mac Terminal:

```sh
shasum -a 256 "/path/to/downloaded.ipa"
```

Windows PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath "C:\path\to\downloaded.ipa"
```

A matching filename is not a checksum check. If the hash differs, do not sign that file; download
it again from the official release.

## Trust the signed app and open it

1. In **Settings → General → VPN & Device Management**, select your Apple Account under
   **Developer App** and trust it. Complete **Allow & Restart** if shown.
2. In **Settings → Privacy & Security → Developer Mode**, turn it on. Restart and confirm when
   prompted. Follow the sideloader's current guide if your iOS wording differs.
3. Open 4789 from the Home Screen.
4. Add a compatible manifest or install URL, a public collection, or your own local files.
   Optional feature setup appears when you activate that feature.

4789 supplies software, not media or credentials. Connect services and files you are authorized to use.
The iPhone IPA and television APK are separate installations; see the
[4789 TV guide](https://4789library.com/player) for television setup.

## Refresh, update, and protect your data

Free signing normally lasts seven days. Confirm a successful refresh before the displayed expiry;
do not rely solely on background refresh. Free accounts normally allow three active sideloaded
apps, including SideStore or AltStore itself.

Install updates over the existing app using the same Apple Account and app identifier. Changing
these can create a separate app or prevent an update. **Do not delete 4789 for a routine refresh
or update.**

Before unavoidable removal, export settings and protect that file. **A settings export is plaintext
and can contain live credentials, tokens, and private URLs.** Saving it in Files or iCloud Drive does
not make the export itself encrypted. Use private storage and never attach it to a public issue.
Do not assume a settings export backs up downloaded media or every piece of local app data.

## If something goes wrong

- **IPA opens in Files:** import it through the sideloader; downloading alone does not install it.
- **App stopped opening:** check expiry and refresh or sign it again with your existing tool.
- **AltServer cannot be found:** check that it is running and that USB or configured Wi-Fi is working.
- **SideStore cannot refresh:** check Wi-Fi and LocalDevVPN, then follow its pairing troubleshooting.
- **App limit reached:** review the sideloader's app slots before removing anything with local data.
- **Developer profile or Developer Mode is missing:** finish the signing installation first, then
  follow the tool's troubleshooting guide.

For app bugs, [open an issue](https://github.com/4789-app/4789-ios-releases/issues/new?template=bug.yml)
with the build, iOS version, sideloader, and exact error. Remove passwords, account details, tokens,
private URLs, and settings exports from screenshots and logs.
