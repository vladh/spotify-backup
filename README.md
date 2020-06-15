# spotify-backup

A Python 3 script that exports all of your Spotify playlists, useful for paranoid Spotify users like me, afraid that one day Spotify will go under and take all of our playlists with it!

Run the script like so:

    python spotify-backup.py playlists.tsv
    
It will ask you for a filename and then pop open a web page so you can authorize access to the Spotify API. Then the script will load your playlists and save a tab-separated file with your playlists that you can open in Excel. You can even copy-paste the rows from Excel into a Spotify playlist.

Adding `--format=json` will give you a JSON dump with everything that the script gets from the Spotify API. If for some reason the browser-based authorization flow doesn't work, you can also [generate an OAuth token](https://developer.spotify.com/web-api/console/get-playlists/) on the developer site (with the `playlist-read-private` permission) and pass it with the `--token` option.

## Acknowledgements

Original by [caseychu](https://github.com/caseychu) with improvements by [vladh](https://github.com/vladh).

Improvements:
* Add support for collaborative playlist and playlist folders.
* Prevent crashes.
