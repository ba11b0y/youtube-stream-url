# yt-url-parser

Gets stream url and other video details from youtube video link.

## Installation

With [npm](https://www.npmjs.com/) do:

``` sh
npm install yt-url-parser
```

## Usage

``` js
const Youtube = require('yt-url-parser');

Youtube.getInfo({url: 'https://www.youtube.com/watch?v=9dLKZZN5tSo'})
  .then(video => console.log(video));
  
  /* video
  { videoDetails:
   { videoId: '9dLKZZN5tSo',
     title: 'Ratan Tata Award Winning Speech with BIG Subtitles',
     lengthSeconds: '263',
     keywords:
      [ 'with big subtitles',
        'ratan tata',
        'ratan tata speech',
        'award winning speech',
        'subtitles' ],
     channelId: 'UCC4gyz11gwCkHaVeuO366tg',
     isOwnerViewing: false,
     shortDescription:
      'Ratan Tata\'s speech from Automotive Hall of Fame. 2015 Induction & Awards Gala Ceremony.\n\nHit Like if you found this video helpful.\nComment if not and please let me know how I can improve.\n\nSubscribe for more videos.\n\nWatch Mahua Moitra Parliament Speech with BIG Subtitles:\nhttps://www.youtube.com/watch?v=vzHRBfPl-6Y&',
     isCrawlable: true,
     thumbnail: { thumbnails: [Array] },
     averageRating: 4.9388342,
     allowRatings: true,
     viewCount: '11302491',
     author: 'wow! Rao',
     isPrivate: false,
     isUnpluggedCorpus: false,
     isLiveContent: false },
  formats:
   [ { itag: 18,
       url:
        'https://r1---sn-u5u5n3tpo-w5pe.googlevideo.com/videoplayback?expire=1624291230&ei=PmPQYL6ECOOnz7sPr46biAw&ip=103.22.143.86&id=o-ALjbtirD0bhem-K_FM86suDfgUAxZ3nQwf43Wj7KOvyr&itag=18&source=youtube&requiressl=yes&mh=M6&mm=31%2C29&mn=sn-u5u5n3tpo-w5pe%2Csn-cvh7knek&ms=au%2Crdu&mv=m&mvi=1&pl=24&initcwndbps=1220000&vprv=1&mime=video%2Fmp4&ns=WXFASK-dqNc5hSPn0peRk44F&gir=yes&clen=11791564&ratebypass=yes&dur=262.664&lmt=1579534842937206&mt=1624269421&fvip=1&fexp=24001373%2C24007246&c=TVHTML5&txp=5531432&n=bS-tw8BRTggvXBqCS&sparams=expire%2Cei%2Cip%2Cid%2Citag%2Csource%2Crequiressl%2Cvprv%2Cmime%2Cns%2Cgir%2Cclen%2Cratebypass%2Cdur%2Clmt&sig=AOq0QJ8wRAIgGz---ma3Tj1PrTWRK_4X854q_CNQmOnxP8e5Vbo4sisCIANTvP8wOA7NuJNbApt4dFFXtQ_sfK_STfmeqGq9mLzV&lsparams=mh%2Cmm%2Cmn%2Cms%2Cmv%2Cmvi%2Cpl%2Cinitcwndbps&lsig=AG3C_xAwRQIhAISuLs7gb247_LQuhcZ81y_ebL3TzU9ebMXGh7oFt_BHAiA2Bdh1kzJd0b-RlENb6ZmXnqaytlLg-7ijhh3xDLv4Vg%3D%3D',
       mimeType: 'video/mp4; codecs="avc1.42001E, mp4a.40.2"',
       bitrate: 359231,
       width: 640,
       height: 360,
       lastModified: '1579534842937206',
       contentLength: '11791564',
       quality: 'medium',
       fps: 30,
       qualityLabel: '360p',
       projectionType: 'RECTANGULAR',
       averageBitrate: 359137,
       audioQuality: 'AUDIO_QUALITY_LOW',
       approxDurationMs: '262664',
       audioSampleRate: '44100',
       audioChannels: 2 },
     { itag: 22,
       url:
        'https://r1---sn-u5u5n3tpo-w5pe.googlevideo.com/videoplayback?expire=1624291230&ei=PmPQYL6ECOOnz7sPr46biAw&ip=103.22.143.86&id=o-ALjbtirD0bhem-K_FM86suDfgUAxZ3nQwf43Wj7KOvyr&itag=22&source=youtube&requiressl=yes&mh=M6&mm=31%2C29&mn=sn-u5u5n3tpo-w5pe%2Csn-cvh7knek&ms=au%2Crdu&mv=m&mvi=1&pl=24&initcwndbps=1220000&vprv=1&mime=video%2Fmp4&ns=WXFASK-dqNc5hSPn0peRk44F&cnr=14&ratebypass=yes&dur=262.664&lmt=1579535599211760&mt=1624269421&fvip=1&fexp=24001373%2C24007246&c=TVHTML5&txp=5535432&n=bS-tw8BRTggvXBqCS&sparams=expire%2Cei%2Cip%2Cid%2Citag%2Csource%2Crequiressl%2Cvprv%2Cmime%2Cns%2Ccnr%2Cratebypass%2Cdur%2Clmt&sig=AOq0QJ8wRQIhAKDgHTcU_JGA8k0sf1rOIIQpjrsocOYZHL3-RrhMqxXFAiA7_qc76juvOqoFU6GBJBbrsb4m1QgGqhMR3lsyRA3YXA%3D%3D&lsparams=mh%2Cmm%2Cmn%2Cms%2Cmv%2Cmvi%2Cpl%2Cinitcwndbps&lsig=AG3C_xAwRQIhAISuLs7gb247_LQuhcZ81y_ebL3TzU9ebMXGh7oFt_BHAiA2Bdh1kzJd0b-RlENb6ZmXnqaytlLg-7ijhh3xDLv4Vg%3D%3D',
       mimeType: 'video/mp4; codecs="avc1.64001F, mp4a.40.2"',
       bitrate: 346914,
       width: 1280,
       height: 720,
       lastModified: '1579535599211760',
       quality: 'hd720',
       fps: 30,
       qualityLabel: '720p',
       projectionType: 'RECTANGULAR',
       audioQuality: 'AUDIO_QUALITY_MEDIUM',
       approxDurationMs: '262664',
       audioSampleRate: '44100',
       audioChannels: 2 },
  */
```

## Credits

This project is a fork of https://github.com/dangdungcntt/youtube-stream-url/ and just tweaks some query parameters.