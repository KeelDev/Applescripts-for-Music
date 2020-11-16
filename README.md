# Applescripts for Music: Year and/or Genre from Discogs

Scenarios:
- You have a disco compilation that was released in 2018, but contains tracks from 1975-1985. Tagging these tracks with 2018 makes little sense: your smart playlist of "70s Disco" will not pick these tracks up, and instead these tunes show up between modern disco songs by Jessie Ware and Dua Lipa.
- You have ripped your cherished red and blue Beatles best-of CDs, released in 1993. To your frustration, these songs keep appearing in your "90s Rock" playlists.
- You have a big folder of loose tracks you downloaded on Napster back in the 1990s, but they have no genre or year tags.

Clearly, these songs need to be tagged with their *original* release year. But looking up every single song, checking its original release year, and writing that in the tags is tedious manual work. MusicBrainz Picard is pretty awesome, but will still tag compilation album tracks with the release date of the album, not years of the original tracks. This is where these scripts come in.

How to install:
1. Create new script in macOS Script Editor
2. Copy/paste the code from this repository
3. Replace the text "please_insert_your_own_API_key_here" in the QueryDiscogs function with your own Discogs API key, see https://www.discogs.com/developers/
4. Save script as .scpt
5. Put script in /Library/Music/Scripts (all users) or /User/johndoe/Library/Music/Scripts (one user)

*YearFromDiscogs*

1. Select one or more tracks, run the script
2. The script performs a Discogs search for "Artist Song Name" for the master single, gets the year back
3. Writes this year in the Year field
4. Optionally writes the "Artist - Release" of the Discogs item to the Comments field, so you can check afterwards which master release this year came from.

Note: even though this Discogs search query specifies that only singles should be included in the search, in fact Discogs seems to ignore this, and will also return years from albums, compilations etc. Hence, the option to write Artist - Release to the comments field, so you can check.

