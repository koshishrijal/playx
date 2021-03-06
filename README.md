<h1 align=center>
<img src="logo/1024 bg.svg" width=100%>
</h1>

## Search and play any song from terminal.

# playx in action

![GIF](https://i.imgur.com/42mEHQ5.gif)

# playx  

1. [Philosophy](#philosophy)
2. [Requirements](#requirements)
3. [Installation](#installation)
4. [Features](#features)
5. [Usage](#usage)
6. [Example](#example)
7. [Contribution](#contributions)
8. [TO-DO](#to-do)
9. [Acknowledgements](#acknowledgements)

# Philosophy
Play any songs that come in your mind.
> Hoping to make it an awesome music assistant
---------

## Requirements/Dependencies

1. Python3.x

2. pip3

3. MPV

 * Get <a href = https://mpv.io/>MPV (website)</a> from here.

 * Get <a href = https://github.com/mpv-player/mpv>MPV (github)</a> from here.

> **Note**: These dependencies in linux can be installed in other variants.  
> For *arch linux*, you can use **pacman** package manager accordingly.


------------

## Installation

 * Run the following command in the root directory to install playx.

```
pip install -e .
```

* Or install using setup.py as:

```bash
python setup.py install
```

------------

## Features

- play by query
- play by youtube url
- play a youtube playlist
- play from local playlist
- cache support
- CLI using `mpv`
------------

## Usage
For now, the application is in development phase.  

```
usage: playx [-h] [-p] [-n] [-d] [-l] [song [song ...]]

playx - Search and play any song that comes to your mind. If you have any
issues, raise an issue in the github (https://github.com/NISH1001/playx) page

positional arguments:
  song                  Name or youtube link of song to download

optional arguments:
  -h, --help            show this help message and exit
  -p, --play-cache      Play all songs from the cache.
  -n, --no-cache        Don't download the song for later use.
  -d, --dont-cache-search
                        Don't search the song in the cache.
  -l, --lyrics          Show lyircs of the song.
  --pl-start PL_START   Start position in case a playlist is passed. If passed
                        without a playlist it has no effect.
  --pl-end PL_END       End position in case a playlist is passed. If passed
                        without a playlist it has no effect.
```

------------

### Example
**Play by song name**
```bash
playx man sold world nirvana
```
This plays the song titled "The man who sold the world by Nirvana"  
  
**Play by youtube link**  
```bash
playx https://www.youtube.com/watch?v=4zLfCnGVeL4
```
This plays the song *The Sound of Silence*.   
  
**Play from youtube playlist**  
```bash
playx https://www.youtube.com/playlist?list=PLwg22VSCR0W6cwuCKUJSkX72xEvYXS0Zx
```
This plays the songs from my personal (and public) playlist named *Chilld and Wisdom*.

**Play from local playlist**

The local playlist should have an extension ```.playx``` in order for us to recognize it as a playlist.
```sh
playx example.playx
```
This plays a playlist named example.playx

For a playlist every line is considered an entry. Refer to [example.playx](https://github.com/NISH1001/playx/blob/develop/example.playx).
  
------------

## Contributions
Contributions are warmly welcome. Please do go through [CONTRIBUTING](https://github.com/NISH1001/playx/blob/develop/CONTRIBUTING.md).

------------

## TO-DO
- ~~caching of downloaded songs (if the song exists locally, play it right away else play from youtube)~~
- ~~speed up the whole **search->download->convert->play** process~~
- ~~stream/play while downloading the song~~
- ~~play all the songs from the cache~~
- ~~search lyrics~~
- ~~play from youtube playlist~~
- ~~play from local playlist (may be a list of song names)~~
- log activity
- use logs to create simple recommendations


## Acknowledgements
- Thanks to [Deepjyoti Barman](https://github.com/deepjyoti30) for parallelizing streaming + downloading (and other improvements)
- Thanks to [Mirza Zulfan](https://github.com/mirzazulfan) for logo for `playx`. It's neat (and cool)
