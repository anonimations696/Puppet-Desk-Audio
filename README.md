# Puppet Desk Audio (PDA)

**Puppet Desk Audio — for Virtual Camera Streaming** is a Windows OBS Studio dock plugin for sharing browser music and microphone audio during calls while privately monitoring a second browser/caller.

Developed by **Hate and LaMDA**.

> **Release status:** Public download package is being prepared. **No release binary is published yet.** Do not download third-party builds claiming to be an official PDA release.

## What PDA does

| Source | Outbound call / stream | OBS recording | Local headphones |
| --- | --- | --- | --- |
| Music browser (e.g. Firefox) | Yes | Yes | Yes |
| Caller browser (e.g. Chrome) | No, avoids echo | Yes | Yes |
| Selected microphone / voice changer | Yes | Yes | Optional via source setup |

PDA provides separate local listening controls for music and caller audio, an OBS microphone source selector, and a **Mute Mic to Call** control. It is designed to work with **OBS virtual camera** and an external calling application, including Discord.

## Compatibility

- Windows 11; tested during development with OBS Studio 32.2.2.
- Two OBS **Application Audio Capture** sources (music and caller) and an OBS **Audio Input Capture** microphone source.
- VB-Audio Virtual Cable for the established OBS monitoring → Discord input arrangement.
- Headphones or earbuds for private local listening. Device compatibility varies.

## Quick setup overview

1. In OBS, create independent **Application Audio Capture** sources for the music and caller browsers.
2. Add an **Audio Input Capture** microphone source. In PDA's top microphone dropdown, select the OBS source you want to transmit and record.
3. Set OBS monitoring device to **CABLE Input (VB-Audio Virtual Cable)** and Discord's input to **CABLE Output**, if using VB-CABLE. Do **not** monitor caller audio into that cable.
4. In PDA, select the two browser sources and your mic source, then start capture. Music and mic belong on the outbound stream track (Track 1) and recording track (Track 2); caller audio belongs on Track 2 only.
5. Test your outbound call and an OBS recording before a real stream. Select the correct recording audio track when playing back multitrack files.

### Voice.ai users

A working Voice.ai setup uses **Samson/physical microphone → Voice.ai → processed OBS audio source selected as PDA's microphone**. **Mute the separate raw `desktop mic` OBS audio source** to prevent simultaneously transmitting the unchanged voice. Keep the physical microphone enabled inside Voice.ai. Do not confuse the separate Voice.ai virtual device with the VB-CABLE already used for Discord; verify the signal using OBS meters and a test call.

## Downloads and updates

Official Windows packages will be published on this repository's [Releases page](https://github.com/anonimations696/Puppet-Desk-Audio/releases). **There is no public release yet.** A downloadable release and updater pointing to this **public repository** are required before PDA is ready for outside users. The private development build's updater is not intended for public distribution.

## Support

Please use this repository's [Issues](https://github.com/anonimations696/Puppet-Desk-Audio/issues) to report installation, routing, compatibility, or playback problems once the first release is available. Include your OBS version, Windows version, and the audio route you configured; never post passwords or private recordings.
