## Overview:

Project Status: ALPHA 1.0
This Repository Homelab contains all my homelab documentation files. Here you'll find notes, setups, and configurations for infrastructure, applications, networking, and more.
This project is still in the experimental stage, and I don't use anything critical on it. Expect breaking changes that may require a complete redeployment.
The homelab runs on an older system currently running Ubuntu 24.04.1 LTS x86_64.

## Hardware:

CPU: Intel i7-4790 (8) @ 4.000GHz

GPU 1: NVIDIA GeForce GT 730

GPU 2: Intel HD Graphics

Memory: 7804MiB

## Hosted Services:

### _Casa OS_ (https://github.com/IceWhaleTech/CasaOS):

CasaOS is a lightweight, open sourced server dashboard designed for creating a personal cloud or managing home servers.
Casa OS helps me gives access to all my services with a GUI interface running inside the server in an aesthetic manner. It comes with an in-built file and disk manager. It also comes with its own appstore which allows installing services directly into the server through the web interface of the dashboard.
It provides real-time metrics like CPU and memory usage, network speeds and disk health.

_Insert casaos image here_

### _Portainer_(https://github.com/portainer/portainer):

Portainer is a lightweight service delivery platform for containerized applications that I use to manage my Docker environments. It is designed to be as simple to deploy as it is to use. It allows me to manage all my orchestrator resources (containers, images, volumes, networks and more) through a ‘smart’ GUI and/or an extensive API.
It is currently running :

_insert portainer image here_

### _NetData_ (https://github.com/netdata/netdata):

Netdata is a high-performance, cloud-native, and on-premises observability platform designed to monitor metrics and logs with unparalleled efficiency. It delivers a simpler, faster, and significantly easier approach to real-time, low-latency monitoring for systems, containers, and applications.
It allows me to moniter CPU, GPU, memory, network, hardware, processes, O/S services, containers/VMs, synthetic checks, etc. with graphs and charts in real-time.

_insert netdata waali bhaari image here_

### _Plex Media Server_ (https://github.com/plexinc):

Plex is a popular media server platform that allows me to organize, stream, and access my personal media (like movies, TV shows, music, and photos) across multiple devices. It acts as a centralized server where I can store my media and then stream it to various devices such as smart TVs, smartphones, tablets, and computers. It also supports remote access, enabling me to stream their content from anywhere.

_insert plex image here_

But there's more to plex media server than you'd think.

### _JellyFin_ (https://github.com/jellyfin/jellyfin)

Jellyfin is a Free Software Media System that puts you in control of managing and streaming your media. It is an alternative to the proprietary Emby and Plex, to provide media from a dedicated server to end-user devices via multiple apps. It's an alternative/backup service to plex.

### _Overseerr Media Request Service_ (https://github.com/sct/overseerr):

Overseerr allows users to request media like movies and TV shows in the quality they desire and send the request to the server administrator which can further approve/disapprove the requested media.
_insert overseerr image here_

### _Radarr_ (https://github.com/Radarr/Radarr):

If the admin approves the movie requested by the user, Radarr fetches metadata for the requested movie and creates a folder insidde the server. It provides utilities like movie reviews, crtique rating, cast information, etc. for the user.
Radarr also automates the process of helping plex access the downloaded movie. It directs plex to access only the movie from the download folder and nothing else, so that plex doesnt interfere with media other than movies.
_insert Radarr image here_

### _Sonarr_ (https://github.com/Sonarr/Sonarr):

Sonarr is similar to Radarr except it is designed to process TV shows and web series as they have to be treated differently than movies with each show having multiple episodes and seasons and hence need to be in a collection so that plex doesn't classify each episode as its own movie.
_insert sonarr image here_

### _Lidarr_ (https://github.com/Lidarr/Lidarr):

Lidarr handles all the audio/music files and basically is my own Music Manager.
It does a similar job to Radarr/Sonarr in creating and managing all the music files in the music folder and helps Plex/Swing Music(Music Player) fetch and play it. It can help choose the desired audio quality which we desire to listen to, basically you can fetch studio quality music files through Lidarr using Prowlarr.
_insert Lidarr image here_

### _Prowlarr_ (https://github.com/Prowlarr/Prowlarr):

Prowlarr is an indexer manager/proxy built on the popular *arr .net/reactjs base stack to integrate with Radarr/Lidarr/Sonarr supporting management of both Torrent Trackers and Usenet Indexers. (Indexers serve as search engines that crawl torrent or Usenet files and index them, providing users with links to the content.)
*insert Prowlarr image here\*

### _Qbittorrent_ (https://github.com/qbittorrent/qBittorrent):

qBittorrent is an open-source BitTorrent client that I use for downloading and sharing files via the BitTorrent protocol. It provides a user-friendly interface and a variety of features that make it a versatile tool for managing torrents.
_insert qbittorrent image here_

### _Deluge_ (https://github.com/deluge-torrent/deluge)

Deluge is a BitTorrent client that utilizes a daemon/client model. It has various user interfaces available such as the GTK-UI, Web-UI and Console-UI. It uses libtorrent at its core to handle the BitTorrent protocol.

### _Jdownloader_ (https://github.com/johna23-lab/jdownloader2)

JDownloader is a free, open-source download management tool with a huge community that makes downloading as easy and fast as it should be.

### _Immich_ (https://github.com/immich-app/immich)

Immich is a high performance self-hosted photo and video management solution.

### _MariaDB_ (https://github.com/MariaDB/mariadb-docker)

MariaDB server is a community developed fork of MySQL server. Started by core members of the original MySQL team, MariaDB actively works with outside developers to deliver the most featureful, stable, and sanely licensed open SQL server in the industry.

### _NextCloud_ (https://github.com/nextcloud/all-in-one)

Nextcloud Hub is the industry-leading, fully open-source, on premise content collaboration platform. Teams access, share and edit their documents, chat and participate in video calls and manage their mail and calendar and projects across mobile, desktop and web interfaces.

### _n8n_ (https://github.com/n8n-io/n8n)

n8n is a workflow automation platform that gives technical teams the flexibility of code with the speed of no-code.

### _MineCraft_ (https://github.com/topics/minecraft-server)

A Minecraft server is a player-owned or business-owned multiplayer game server for the 2009 Mojang Studios video game Minecraft. In this context, the term "server" often colloquially refers to a network of connected servers, rather than a single machine. Players can start their own server either by setting one up on a computer using software provided by Mojang, or by using a hosting provider so they can have their server run on dedicated machines with guaranteed uptime.

My friend (https://github.com/ohhitsaryan) challenged me to host a Minecraft server on my HomeLab so I used this service to host one.

### _VScodium_ (https://github.com/VSCodium/vscodium)

VSCodium is a community-driven, freely-licensed binary distribution of Microsoft’s editor VS Code.
This VScodium docker edition allows me to edit codes through my server using a web browser.

### _twingate-connector_ (https://github.com/Twingate)

Twingate is a zero trust network access (ZTNA) platform designed to improve the security and manageability of remote access to internal applications, resources, and networks. It replaces traditional VPNs with a more secure, scalable, and user-friendly solution.

