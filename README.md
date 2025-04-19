# Setlist Analysis of Hacken Lee's Three Themed Concerts Using Spotify Data
![](https://img.shields.io/badge/ReadMe-English-blue?link=https%3A%2F%2Fgithub.com%2Fwend1k3%2FSetlist-Analysis%3Ftab%3Dreadme-ov-file
) &emsp; ![](https://img.shields.io/badge/ReadMe-%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87-blue?link=https%3A%2F%2Fgithub.com%2Fwend1k3%2FSetlist-Analysis%2Fblob%2Fmain%2Freadme.zh.md
)
![](https://img.shields.io/badge/python-brightgreen
) ![](https://img.shields.io/badge/jupyter-notebook-brightgreen
)
## Project Introduction
When 

In this project, I 


## Project Goals
Analyze the track selection from three Hacken Lee's concerts that share the same theme. 



Specifically, this project explores:
- <em>How are hit songs and lesser-known sidetracks balanced across the setlists?</em>
- <em>Which albums are most favoured?</em>
- <em>How do the setlists vary across different concert locations?</em>

### Why Hacken Lee?
I like him.

## Data Extraction
There is a Python library for the Spotify Web API called [Spotipy](https://spotipy.readthedocs.io/en/2.25.1/), which I uses for retrieving music data provided by the Spotify platform.

For <b>authorization</b>, I followed the step on <em>Spotipy</em> documentation page and set environment variables.
```python
from spotipy.oauth2 import SpotifyClientCredentials
spo = spotipy.Spotify(client_credentials_manager=SpotifyClientCredentials())
```
The first step is to <b>grab every albums data</b> using `artist_albums`. For example:
```python
albums = []
hacken = spo.artist("https://open.spotify.com/artist/3PV11RNUoGfX9tMN2wVljB")
album = spo.artist_albums(hacken['id'], include_groups='album',limit=50)
albums.extend(album['items'])
while album['next']:
    album = spo.next(album)
    albums.extend(album['items'])
```
<b>Establish dataframe from `albums`and saving it for later use</b>
```python
df = pd.DataFrame(data=albums,columns=['name','id','release_date','album_type'])
df.to_excel(path+"Hacken_Lee_Albums_Full.xlsx",index=False)
```





## Data Analysis and Visualization