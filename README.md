**Note**  
This extension will auto update files from the Stremio Cache to the qBittorrent client, so make sure you have installed qBittorrent as the client first!  
  
`Windows` requires administrator privileges to create a symbolic link. You can try running Stremio with administrator.  
  
**BEFORE INSTALL**  
- And you also need to enable the WebUI feature on qBittorrent.
![image](https://github.com/Vance-ng-vn/Stremio-Seeds/assets/88782390/f672a689-f53e-43c8-a23b-aef06c23c4df)


**INSTALL**  
1. Extract extensions.zip to the folder have server.js (same directory as Stremio.exe)
2. Open 'server.js' as a text editor
3. Add this line to the begin of server.js:  
  `require('./extensions/stremio-seeds/stremio-seeds.js');`
4. Save! Restart Stremio.

**CONFIG**  
`START_SEED_PERCENT` Accept seed files that have been downloaded X%, 0 < X <= 100. Default is 90%  
`INTERVAL_CHECK` sec/min/hour/day leave empty to disable  
`CACHE_DIR` your Stremio's cache dir (path/to/stremio-cache) leave empty to use dedault cache dir  
`CUSTOM_CACHE_SIZE` kb/mb/gb/tb Overide Stremio Cache-Size Settings  
`KEEP_TORRENT_LOW_SEEDER` require `CUSTOM_CACHE_SIZE`: Cache Control by extension. When the Cache is FULL, remove the torrents that have highest seeders first!  
`QT_HOST` qBittorrent host  
`QT_PORT` qBittorrent port  
`QT_USERNAME` qBittorrent username  
`QT_PASSWORD` qBittorrent password  
`BLOCK_DOWNLOAD` true: limit download at 1KiB/s  
`SKIP_CHECKING` skip check file when adding it to qBiittorrent  
`UPLOAD_LIMIT` kb/mb/gb limit Upload Speeds  
`RATIO_LIMIT` max share Ratio  
`INCLUDE_STREMIO_TRACKER` Include default trackers from Stremio  
