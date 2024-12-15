# Overview:

Project Status: ALPHA 1.0
This Repository Homelab contains all my homelab documentation files. Here you'll find notes, setups, and configurations for infrastructure, applications, networking, and more.
This project is still in the experimental stage, and I don't use anything critical on it. Expect breaking changes that may require a complete redeployment.
The homelab runs on an older system currently running Ubuntu 24.04.1 LTS x86_64.

# Hardware:

CPU: Intel i7-4790 (8) @ 4.000GHz

GPU 1: NVIDIA GeForce GT 730

GPU 2: Intel HD Graphics

Memory: 7804MiB

# Hosted Services:

# *Casa OS* (https://github.com/IceWhaleTech/CasaOS):

CasaOS is a lightweight, open sourced server dashboard designed for creating a personal cloud or managing home servers.
Casa OS helps me gives access to all my services with a GUI interface running inside the server in an aesthetic manner. It comes with an in-built file and disk manager. It also comes with its own appstore which allows installing services directly into the server through the web interface of the dashboard.
It provides real-time metrics like CPU and memory usage, network speeds and disk health.

_Insert casaos image here_

# *Portainer*(https://github.com/portainer/portainer):

Portainer is a lightweight service delivery platform for containerized applications that I use to manage my Docker environments. It is designed to be as simple to deploy as it is to use. It allows me to manage all my orchestrator resources (containers, images, volumes, networks and more) through a ‘smart’ GUI and/or an extensive API.
It is currently running :

- 35 docker containers
- 22 container stacks
- 44 docker images
- 8 volumes
- 10 networks

_insert portainer image here_

# *NetData* (https://github.com/netdata/netdata):
Netdata is a high-performance, cloud-native, and on-premises observability platform designed to monitor metrics and logs with unparalleled efficiency. It delivers a simpler, faster, and significantly easier approach to real-time, low-latency monitoring for systems, containers, and applications.
It allows me to moniter CPU, GPU, memory, network, hardware, processes, O/S services, containers/VMs, synthetic checks, etc. with graphs and charts in real-time.

_insert netdata waali bhaari image here_

# *Plex Media Server* (https://github.com/plexinc):
Plex is a popular media server platform that allows me to organize, stream, and access my personal media (like movies, TV shows, music, and photos) across multiple devices. It acts as a centralized server where I can store my media and then stream it to various devices such as smart TVs, smartphones, tablets, and computers. It also supports remote access, enabling me to stream their content from anywhere.

_insert plex image here_

But there's more to plex media server than you'd think.

# *Overseerr Media Request Service* (https://github.com/sct/overseerr):
Overseerr allows users to request media like movies and TV shows in the quality they desire and send the request to the server administrator which can further approve/disapprove the requested media.
_insert overseerr image here_

# *Radarr* (https://github.com/Radarr/Radarr):
If the admin approves the movie requested by the user, Radarr fetches metadata for the requested movie and creates a folder insidde the server. It provides utilities like movie reviews, crtique rating, cast information, etc. for the user.
Radarr also automates the process of helping plex access the downloaded movie. It directs plex to access only the movie from the download folder and nothing else, so that plex doesnt interfere with media other than movies.
_insert Radarr image here_

# *Sonarr* (https://github.com/Sonarr/Sonarr):
Sonarr is similar to Radarr except it is designed to process TV shows and web series as they have to be treated differently than movies with each show having multiple episodes and seasons and hence need to be in a collection so that plex doesn't classify each episode as its own movie.
_insert sonarr image here_

# *Lidarr* (https://github.com/Lidarr/Lidarr):
Lidarr handles all the audio/music files and basically is my own Music Manager.
It does a similar job to Radarr/Sonarr in creating and managing all the music files in the music folder and helps Plex/Swing Music(Music Player) fetch and play it. It can help choose the desired audio quality which we desire to listen to, basically you can fetch studio quality music files through Lidarr using Prowlarr.
_insert Lidarr image here_

# *Prowlarr* (https://github.com/Prowlarr/Prowlarr):
Prowlarr is an indexer manager/proxy built on the popular *arr .net/reactjs base stack to integrate with Radarr/Lidarr/Sonarr supporting management of both Torrent Trackers and Usenet Indexers. (Indexers serve as search engines that crawl torrent or Usenet files and index them, providing users with links to the content.)
*insert Prowlarr image here\*

# *Qbittorrent* (https://github.com/qbittorrent/qBittorrent):
qBittorrent is an open-source BitTorrent client that I use for downloading and sharing files via the BitTorrent protocol. It provides a user-friendly interface and a variety of features that make it a versatile tool for managing torrents.
_insert qbittorrent image here_
