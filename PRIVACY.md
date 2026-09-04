# Privacy

The public 4789 build requires no 4789 account and contains no advertising or behavioral-tracking
SDK.

## On the device

Library state, playback progress, settings, and downloads are stored locally. Credentials and
credential-bearing URLs are stored in the system Keychain. A settings export is user initiated and
can contain sensitive configuration, so keep it private.

## Direct connections

4789 connects directly to compatible services a person chooses. Those independent services may
receive the device's IP address and the requests needed to perform the selected action under their
own privacy policies. The public build does not proxy those requests through a 4789 media server.

## Not included

The public build includes no maintainer credential, private catalog snapshot, private recovery seed,
or owner-only service configuration.

The Apple Account used for local IPA signing is handled by the chosen sideloader and Apple. It is
never provided to 4789.
