# yt-dlp

*Copyright (c) 2026 vegahen*

```yaml
- type: source
  urls: https://en.wikipedia.org/wiki/Youtube-dl
- type: repository
  urls: https://github.com/yt-dlp/yt-dlp
```

## Commands

### List available video and audio formats

```sh
yt-dlp --list-formats "_INSERT_VIDEO_URL"
```

### Download with default parameters

```sh
yt-dlp --format "bv*+ba/b" "_INSERT_VIDEO_URL"
```

I think the previous format options will become the default soon whenever you just run

```sh
yt-dlp "_INSERT_VIDEO_URL"
```

I don't really understand any of the stuff in the readme though, so you should ask a free AI model instead of me if you care about the details.

If you don't care about details, this was everything you needed to know.

### Download all formats in separate files

```sh
yt-dlp --all-formats "_INSERT_VIDEO_URL"
```

I never learned how to filter formats, so this is helpful when I just want to look at which audio and video tracks you can actually get.

### Download and merge specific formats

```sh
yt-dlp --format "bv*[ext=_INSERT_VIDEO_FORMAT][height=_INSERT_VIDEO_PIXEL_HEIGHT]+ba[ext=_INSERT_AUDIO_FORMAT]
```

This is probably a stupid way to do it, but it worked for me. For example, I was able to use

```sh
yt-dlp --format "bv*[ext=mp4][height=720]+ba[ext=m4a]" "_INSERT_VIDEO_URL"
```

to download my friend's video with the exact details I wanted.
