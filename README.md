
# <img src="docs/images/t9Logo.png" height="25"> Tyzen9 - docker-servarr-seedbox
[Servarr](https://wiki.servarr.com/) is a collection of applications that automate and manage media collections for Radarr, Sonarr, Readarr and Prowlarr which is an indexer manager that syncs with the "*Arr" apps. All of this is done behind a [Private Internet Access](https://www.privateinternetaccess.com/) (PIA) VPN connection that provides enhanced privacy and security for the internet connection. 

<p align="center">
<img src="docs/images/PIA-logo.png" height="50">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<img src="docs/images/prowlarr-logo.png" height="50">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<img src="docs/images/radarr-logo.png" height="50">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<img src="docs/images/sonarr-logo.png" height="50">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<img src="docs/images/bazarr-logo.png" height="50">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<img src="docs/images/recyclarr-logo.png" height="50">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<img src="docs/images/readarr-logo.png" height="50">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
</p>  

> [!IMPORTANT]
> Disclaimer: The content GitHub is intended for experimentation and educational purposes only. Use at your own risk.

> [!CAUTION]
> Warning: Downloading media from torrents can be illegal and may result in copyright infringement charges. Proceed with caution as you could face legal consequences.

This PIA and Servarr stack offers the following services:


# What's Inside?
The docker-pia-servarr stack contains everything you need for a stable Servarr experience. To get started experimenting with this technology all you is a Linux host, some curiosity, and an affordable [Private Internet Access](https://www.privateinternetaccess.com/) (PIA) VPN account. The [PIA Servarr Wiki](https://github.com/tyzen9/docker-pia-servarr/wiki) should get even the least experienced Ubuntu Linux user off the ground and running.



1. [PIA VPN](https://github.com/thrnz/docker-wireguard-pia) - A PIA VPN tunnel is created for ALL activity on this Docker Stack.  
   > [!IMPORTANT]
   > In the case where the VPN container becomes non-functional, all the following activity will stop.

1. [Prowlarr](https://prowlarr.com/) - an indexer manager/proxy built on the popular *arr .net/reactjs base stack, designed to integrate with various PVR applications like Sonarr, Radarr, Lidarr, and Readarr. It supports the management of both Torrent Trackers and Usenet Indexers, streamlining the process of adding and maintaining indexers across multiple media management applications.
1. [Sonarr](https://sonarr.tv/) - a personal video recorder (PVR) for TV shows, designed for both Usenet and BitTorrent users, which automatically searches for new episodes of your favorite series, downloads them, and organizes your media library. It monitors RSS feeds, manages inventory, renames files, and can upgrade the quality of your media collection by replacing lower-quality episodes with higher-quality versions when available.
1. [Radarr](https://radarr.video/) - an open-source application designed for automating movie downloads, similar to how Sonarr handles TV shows. It monitors multiple RSS feeds for new movie releases, integrates with Usenet or BitTorrent clients to download, sort, and rename movies, and can automatically upgrade existing movie files to higher quality versions when available.
1. [qBittorrent](https://www.qbittorrent.org/) - a free, open-source BitTorrent client designed to be lightweight and feature-rich, offering a clean, ad-free interface for downloading torrents. It supports multiple platforms including Windows, macOS, Linux, and FreeBSD, with features like an integrated search engine, RSS feed support, and remote management via a web UI.
1. [qBittorrent Listening Port Helper](https://github.com/tyzen9/docker-qbittorrent-port-helper) - a tool designed to simplify the process of port forwarding for the qBittorrent client, particularly useful when used with VPNs like Private Internet Access. It automates the retrieval of port information from the VPN service and configures qBittorrent accordingly to ensure optimal connectivity and download speeds.
1. [Striparr](https://github.com/mikenye/docker-striparr) - A utility designed to remove metadata from media files imported by media management systems like Sonarr and Radarr. It operates by stripping out title and comment metadata fields, ensuring that file names are based on metadata collected by media scanners rather than potentially unwanted embedded information.
1. [Flaresolver](https://github.com/FlareSolverr/FlareSolverr) - an open-source proxy server designed to bypass Cloudflare's anti-bot protections, enabling seamless web scraping from Cloudflare-protected websites
1. [Unpackerr](https://github.com/Unpackerr/unpackerr) - prevents rar files getting stuck in the activity queue.
1. [Bazarr](https://www.bazarr.media/) - a companion application to Sonarr and Radarr that manages and downloads subtitles based on your requirements.
1. [Recyclarr](https://recyclarr.dev/) - Automatically synchronize TRaSH Guides to Sonarr and Radarr
1. [lftp-mirror](https://github.com/tyzen9/docker-lftp-mirror) - a container for mirroring the contents of a source server to a target server using an ssh tunnel and lftp to perform efficient file transfers through a secure connection.
1. [Myanonamouse (MAM) Dynamic Ip Helper](https://github.com/tyzen9/docker-myanonamouse-ip-helper) - scripting to keep a dynamic [myanonamouse](https://www.myanonamouse.net/) dynamic seedbox IP up to date.

1. [Readarr](https://readarr.com/) (❌Sunset) - an ebook and audiobook management application designed for automation and organization, similar in concept to Sonarr for TV shows or Radarr for movies. It allows users to automatically manage their library by searching for new releases, downloading them from various sources, and organizing them into a predefined directory structure. 


## Getting Started
Deploy the stack into your Docker environment. This can be done by cloning this repository, by downloading the most recent release, or just by simply copying the content of the `compose.yml` file and `sample.env` above. 

1. Make a copy of `sample.env`, and name it `.env`
1. Set the configuration options as desired in the `compose.yaml` and `.env` files.
1. Navigate to the project's root directory and run the following command:

```
docker compose up
```

## Where to go from here?
 The [Servarr Seedbox Wiki](https://github.com/tyzen9/docker-servarr-seedbox/wiki) should get even the least experienced Ubuntu Linux user off the ground and running. However, **all of the detailed configurations for each component can be found on the pages linked above**.