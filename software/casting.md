# Technical Overview: Casting & Wireless Content Transmission Methods

## Comparison Table

| Protocol / Method | Type of Transmission              | Compatible Apps / OS                                                                    | Compatible Receiver Devices / OS                       | Network / Signal Used |
|-------------------|-----------------------------------|-----------------------------------------------------------------------------------------|--------------------------------------------------------|-----------------------|
| Google Cast       | Media streaming, screen mirroring | YouTube, Netflix, Chrome, VLC, Spotify (Android, iOS, Windows, macOS, Linux)            | Chromecast, Google TV, Android TV, Smart TVs, speakers | Wi-Fi (LAN)           |
| Miracast          | Screen mirroring                  | Windows (native), Android (native/apps), Linux (limited), macOS (limited)               | Smart TVs, Windows PCs, Miracast dongles               | Wi-Fi Direct          |
| DLNA/UPnP         | Media streaming, file sharing     | Windows Media Player, VLC, BubbleUPnP, AllConnect (Windows, macOS, Linux, Android, iOS) | Smart TVs, media players, Windows, macOS, Linux        | Wi-Fi, LAN            |
| Bluetooth         | Audio streaming, file sharing     | System audio/file apps (Android, iOS, Windows, macOS, Linux)                            | Speakers, headphones, TVs, computers                   | Bluetooth             |
| AirPlay           | Media streaming, screen mirroring | iOS, macOS (native), AirScreen, AllCast (Android, Windows)                              | Apple TV, AirPlay-enabled TVs, Windows (with software) | Wi-Fi (LAN)           |
| Web-based Casting | Media streaming, screen sharing   | Chrome, Firefox, Edge, Safari, WebRTC apps (Windows, macOS, Linux, Android, iOS)        | Any device with browser, Smart TVs                     | Wi-Fi, LAN            |

## Ecosystem / OS Compatibility Summary

- **Android / iOS → Google TV / Android TV / Chromecast**: Google Cast (media, mirroring), DLNA (media), Bluetooth (audio).
- **Windows → Smart TV / Chromecast / Miracast dongle**: Google Cast (via Chrome), Miracast (native), DLNA (media), Bluetooth (audio).
- **macOS / iOS → Apple TV / AirPlay-enabled TV**: AirPlay (media, mirroring), DLNA (media via apps), Bluetooth (audio).
- **Linux → Smart TV / Chromecast / Miracast dongle**: Google Cast (via Chrome), DLNA (media), Miracast (limited), Bluetooth (audio).
- **Cross-platform (any OS) → Browser / Smart TV**: Web-based casting (media, screen sharing), DLNA (media), Bluetooth (audio).

**Strengths & Limitations:**

- **Latency:** Google Cast and AirPlay offer low latency; Miracast moderate; DLNA and Bluetooth higher.
- **Stability:** Google Cast and AirPlay are stable on native devices; Miracast and DLNA depend on network quality.
- **Use Cases:** Media streaming (Google Cast, DLNA, AirPlay), screen mirroring (Google Cast, Miracast, AirPlay), audio (Bluetooth), cross-platform (Web-based, DLNA).
