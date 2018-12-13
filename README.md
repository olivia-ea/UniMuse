# <img src="/UniMuse/static/img/_readme/unimuse.png" width="449" height="72">

Tired of opening up different applications for you music needs? Well, you've come to the right place!
UniMuse is a web application that consolidates music services in one, easy-to-use platform. Through
UniMuse, you can create and delete playlists, search for songs, and PLAY the songs without worrying
about the source of your music.


## 🎶 Table of Contents 🎶

* [Tech Stack](#tech-stack)
* [Features](#features)
* [Setup/Installation](#installation)
* [Version 2.0](#future)


## <a name="features"></a>🌟 Features 🌟

Sign-up for UniMuse and log-in to your Spotify account.
Note:
 - Spotify's service requires premium access for the full song.
 - No need to log-in to YouTube and Mixcloud!
  
![UniMuse Signup](/UniMuse/static/img/_readme/unimuse_signup.gif)
<br/><br/><br/>
Create a new playlist.
  
![Create Playlist](/UniMuse/static/img/_readme/unimuse_create_playlist.gif)
<br/><br/><br/>
Delete a playlist.
  
![Delete Playlist](/UniMuse/static/img/_readme/unimuse_delete_playlist.gif)
<br/><br/><br/>
Search for songs from all three music service libraries!
The results from the different services are distinguished by the buttons with their logo and color.
Add songs to your playlist by selecting a playlist and clicking the plus button next to the search result.
  
![Search and Add Songs](/UniMuse/static/img/_readme/unimuse_search_add_songs.gif)
<br/><br/><br/>
Play songs from your playlist by selecting a playlist and clicking the play button in the player controls panel.

![Play](/UniMuse/static/img/_readme/unimuse_playlist_player.gif)


## <a name="tech-stack"></a>Tech Stack

__Frontend:__ HTML5, ReactJS, JavaScript, Jinja, jQuery, Bootstrap <br/>
__Backend:__ Python, Flask, PostgreSQL, SQLAlchemy <br/>
__Testing:__ Selenium <br />
__APIs:__ Spotify, YouTube Data, Mixcloud <br/>


## <a name="installation"></a>Setup/Installation

#### Requirements:

- PostgreSQL
- Python 3.6
- Spotify, YouTube, and API keys

To run UniMuse on your local computer, please follow the below steps:

Clone repository:
```
$ git clone https://github.com/yspark90/UniMuse.git
```
Create a virtual environment in the UniMuse/UniMuse folder:
```
$ virtualenv env
```
Activate the virtual environment:
```
$ source env/bin/activate
```
Install dependencies:
```
$ pip install -r UniMuse/requirements.txt
```
Get your own secret keys for:
[Spotify](https://developer.spotify.com/) and [YouTube](https://developers.google.com/youtube/)
Note: [Mixcloud](https://www.mixcloud.com/developers/) does not require a key to use their API.

Save them to a file `secrets.py`. Your file should look something like this:
```
export SPOTIFY_CLIENT_SECRET=YOUR_KEY
export SPOTIFY_CLIENT_ID=YOUR_KEY
export YOUTUBE_API_KEY=YOUR_KEY
```
Create database 'unimuse'.
```
$ createdb unimuse
```
Create your database tables.
```
$ python3 models.py
```
Run the app from the command line.
```
$ python3 server.py
```


## <a name="future"></a>❤️ Version 2.0 ❤️
* Add more services (e.g., Soundcloud, Pandora)
* Add seamless play-through of songs from playlist
* Add controls for player
* Add social features to share playlists with friends