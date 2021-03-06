# Youtube v3 Livestream Downloader

I wanted something to download and save livestreams from a certain channel since I'm not always around when they stream and they don't save the videos to their channel.

This script runs forever watching and waiting for a livestream to start, then downloads the video and converts it to mp4 for more universal playback.

*WIP*


# Convert to mp4

    ffmpeg -i input.ts -acodec copy -vcodec copy out.mp4

# Download stream using streamlink

    streamlink -v --http-no-ssl-verify --hls-live-restart -o 2019-05-26.ts https://www.youtube.com/watch?v=nDIsueMUy-c best

https://github.com/streamlink/streamlink

# Resources

- [Google API Quotas](https://console.developers.google.com/iam-admin/quotas)
- [Youtube v3 API](https://godoc.org/google.golang.org/api/youtube/v3#LiveStreamsListCall)
- [How to use the `part` parameter](https://developers.google.com/youtube/v3/getting-started#part)
- [Go Examples](https://github.com/youtube/api-samples/tree/master/go)
- [list live streams (PHP)](https://github.com/youtube/api-samples/blob/master/php/list_streams.php)
