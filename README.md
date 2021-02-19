# Torrent Search
[![Build Status](https://travis-ci.com/billyb2/torrent-search-rs.svg?branch=main)](https://travis-ci.com/billyb2/torrent-search-rs)

### Usage:
To search for a torrent, simply use the search_l337x function

 ```
 use torrent_search::{search_l337x, TorrentSearchResult, TorrentSearchError};
 let debian_search_results = search_l337x("Debian ISO".to_string()).unwrap();

 for result in debian_search_results {
     println!("Name of torrent: {}\nMagnet: {}\nSeeders: {}\nLeeches: {}", result.name, result.magnet.unwrap(), result.seeders.unwrap(), result.leeches.unwrap());
 }

 ```

This will return `Result<Vec<TorrentSearchResult>, TorrentSearchError>`, which when unwrapped
gives a Vector of TorrentSearchResults (shocking I know).

You can view more information about the data types of the structs [here](struct.TorrentSearchResult.html)
