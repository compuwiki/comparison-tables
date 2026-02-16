# Media Streaming Diagrams

Below are Mermaid diagrams that illustrate library clients, streaming aggregators, IPTV, and Netflix-style streaming. These are conceptual flows meant for comparison.

## Library Client (server-based)

```mermaid
flowchart LR
  User((User)) --> Ombi[Ombi - optional requests]
  Ombi --> Sonarr[Sonarr - TV PVR]
  Ombi --> Radarr[Radarr - Movie PVR]

  Sonarr --> Indexers[Usenet indexers]
  Radarr --> Indexers
  Sonarr --> Trackers[Torrent trackers]
  Radarr --> Trackers

  Indexers --> NZB[NZB file]
  NZB --> Sabnzbd[NZB client]
  Sabnzbd --> Provider[Usenet provider - SSL]

  Trackers --> TorrentFile[.torrent or magnet]
  TorrentFile --> Client[Torrent client]
  Client --> Swarm[Peer swarm]

  Provider --> Download[Downloaded media]
  Swarm --> Download

  Download --> Library[Plex/Emby/Jellyfin library]
  Library --> User
```

## Streaming Aggregator Client (addons + debrid)

```mermaid
flowchart LR
  User((User)) --> Client[Stremio or similar client]
  Client --> Addons[Addons - catalogs and sources]
  Addons --> Sources[Content sources]
  Sources --> Debrid[Debrid API]
  Sources --> Direct[Direct stream]
  Debrid --> Cached[Cached stream or download]
  Cached --> Player[Client player]
  Direct --> Player
  Player --> User

  User -. optional .-> VPN[VPN]
  VPN -. optional .-> Sources
```

## IPTV workflow (client + provider)

```mermaid
flowchart LR
  User((User)) --> IPTVApp[IPTV client app]
  IPTVApp --> Portal[M3U/Portal + EPG]
  Portal --> Provider[IPTV provider]
  Provider --> Stream[Live stream]
  Stream --> Device[Playback device]
  Device --> User
```

## Netflix (centralized streaming)

```mermaid
flowchart LR
  User((User)) --> App[Netflix App]
  App --> CDN[Netflix CDN]
  CDN --> Stream[Adaptive streaming segments]
  Stream --> Device[Playback device]
  Device --> User
```

## Pros and Cons by Workflow

| Workflow                          | Pros                                                | Cons                                               |
| --------------------------------- | --------------------------------------------------- | -------------------------------------------------- |
| Library client (server-based)     | Full library control; automation friendly           | More services and setup; storage required          |
| Streaming aggregator client       | Simple app UX; broad catalogs; fast cached streams  | Addon churn; third-party risk; uneven metadata     |
| IPTV workflow                     | Live channels; simple client setup                  | Provider quality varies; unstable lineups          |
| Netflix (centralized streaming)   | Stable quality; easy setup; consistent UX           | Region-locked catalog; ongoing cost; DRM limits    |
