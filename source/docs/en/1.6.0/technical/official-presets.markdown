---
Type:            article
State:           [ obsolete ]
Title:           Official presets
Project:         HandBrake
Project_URL:     https://handbrake.fr/
Project_Version: 1.6.0
Language:        English
Language_Code:   en
Authors:         [ Bradley Sepos <bradley@bradleysepos.com> (BradleyS) ]
Copyright:       2024 HandBrake Team
License:         Creative Commons Attribution-ShareAlike 4.0 International
License_Abbr:    CC BY-SA 4.0
License_URL:     https://handbrake.fr/docs/license.html
---

Official presets
================

A `Preset` is a group of settings specifically tailored for the software or device you want your videos to play on. Selecting a `Preset` can go a long way toward ensuring your video works where you want it to.

HandBrake includes a number of official `Presets` that select specific settings to ensure compatibility for specific devices, the web, and for general use. When selecting one of these `Presets`, higher resolution video will be downscaled to a maximum resolution, and higher frame rates will be peak limited to a maximum frame rate. Audio and other settings may also be enforced.

Here are some examples of how `Presets` work in practice:

- When selecting one of the 720p30 `Presets`, a Source with 1080p video at 60 frames per second will be downscaled to 720p resolution and peak limited to 30 frames per second
- When selecting one of the 720p30 `Presets`, a Source with 480p video at 30 frames per second will not be scaled or peak limited
- When selecting a `Preset` that does not include surround sound, only stereo audio is encoded; the discrete surround audio is dropped
- When selecting a `Preset` that includes surround sound, stereo audio is encoded and surround audio is "passed through" if possible (or encoded to a compatible format)

Select a `Preset` and explore which settings have changed. These settings will be used to make your new video.

The default `Fast 1080p30` preset is a good choice if you're just getting started. It's fast and compatible across a wide range of software and devices.

## General presets

HandBrake's General `Presets` use the [MP4 container](https://en.wikipedia.org/wiki/MPEG-4_Part_14) and are intended to be broadly compatible across a wide range of software and devices.[^high-quality-settings-less-compatible]

Each General `Preset` is named according to the quality or speed, maximum resolution, and maximum frame rate it produces.

| Preset                            | Type | Video     | Audio                            | Picture Quality | Encoding Speed | File Size      |
|-----------------------------------|------|-----------|----------------------------------|-----------------|----------------|----------------|
| Very Fast 2160p60 4K AV1          | MP4  | **AV1**   | AAC stereo                       | Average         | Very fast      | Small          |
| Very Fast 2160p60 4K HEVC         | MP4  | **H.265** | AAC stereo                       | Average         | Very fast      | Small          |
| Very Fast 1080p30                 | MP4  | H.264     | AAC stereo                       | Average         | Very fast      | Small          |
| Very Fast 720p30                  | MP4  | H.264     | AAC stereo                       | Average         | Very fast      | Small          |
| Very Fast 576p25                  | MP4  | H.264     | AAC stereo                       | Average         | Very fast      | Small          |
| Very Fast 480p30                  | MP4  | H.264     | AAC stereo                       | Average         | Very fast      | Small          |
| Fast 2160p60 4K AV1               | MP4  | **AV1**   | AAC stereo                       | Standard        | Fast           | Average        |
| Fast 2160p60 4K HEVC              | MP4  | **H.265** | AAC stereo                       | Standard        | Fast           | Average        |
| **Fast 1080p30**                  | MP4  | H.264     | AAC stereo                       | Standard        | Fast           | Average        |
| Fast 720p30                       | MP4  | H.264     | AAC stereo                       | Standard        | Fast           | Average        |
| Fast 576p25                       | MP4  | H.264     | AAC stereo                       | Standard        | Fast           | Average        |
| Fast 480p30                       | MP4  | H.264     | AAC stereo                       | Standard        | Fast           | Average        |
| HQ 2160p60 4K AV1 Surround        | MP4  | **AV1**   | AAC stereo; Dolby Digital (AC-3) | High            | Slow           | Large          |
| HQ 2160p60 4K HEVC Surround       | MP4  | **H.265** | AAC stereo; Dolby Digital (AC-3) | High            | Slow           | Large          |
| HQ 1080p30 Surround               | MP4  | H.264     | AAC stereo; Dolby Digital (AC-3) | High            | Slow           | Large          |
| HQ 720p30 Surround                | MP4  | H.264     | AAC stereo; Dolby Digital (AC-3) | High            | Slow           | Large          |
| HQ 576p25 Surround                | MP4  | H.264     | AAC stereo; Dolby Digital (AC-3) | High            | Slow           | Large          |
| HQ 480p30 Surround                | MP4  | H.264     | AAC stereo; Dolby Digital (AC-3) | High            | Slow           | Large          |
| Super HQ 2160p60 4K AV1 Surround  | MP4  | **AV1**   | AAC stereo; Dolby Digital (AC-3) | Super High      | **Very slow**  | **Very large** |
| Super HQ 2160p60 4K HEVC Surround | MP4  | **H.265** | AAC stereo; Dolby Digital (AC-3) | Super High      | **Very slow**  | **Very large** |
| Super HQ 1080p30 Surround         | MP4  | H.264     | AAC stereo; Dolby Digital (AC-3) | Super high      | **Very slow**  | **Very large** |
| Super HQ 720p30 Surround          | MP4  | H.264     | AAC stereo; Dolby Digital (AC-3) | Super high      | **Very slow**  | **Very large** |
| Super HQ 576p25 Surround          | MP4  | H.264     | AAC stereo; Dolby Digital (AC-3) | Super high      | **Very slow**  | **Very large** |
| Super HQ 480p30 Surround          | MP4  | H.264     | AAC stereo; Dolby Digital (AC-3) | Super high      | **Very slow**  | **Very large** |

## Web presets

HandBrake's Web `Presets` use the broadly compatible [MP4 container](https://en.wikipedia.org/wiki/MPEG-4_Part_14) and are tailored for sharing videos on the Internet.

Creator `Presets` produce videos suitable for uploading to video hosting services such as [Vimeo](https://vimeo.com/) and [YouTube](https://www.youtube.com/).[^video-hosting-services] These `Presets` generally produce higher quality audio and video to reduce generational loss commonly accrued during re-encoding into multiple formats and resolutions by video hosting services.

Email `Presets` are designed to guarantee video up to a certain duration will produce a file less than 25 [MB](abbr:megabytes) for sharing via an online email service such as [Gmail](https://www.google.com/gmail/).[^email-size-limit] The maximum `Source` duration is part of each `Preset` name. Audio quality is slightly reduced, and visually noisy/grainy or high motion scenes may show a reduction in quality in order to achieve the target file size.

Social `Presets` are designed to guarantee video up to a certain duration will produce a file smaller than a specific size for sharing with online social communities such as [Discord](https://discordapp.com/).[^social-services] The maximum `Source` duration and target file size are part of each `Preset` name. Audio quality is slightly reduced, and visually noisy/grainy or high motion scenes may show a reduction in quality in order to achieve the target file size.

| Preset                              | Type | Video | Audio      | Picture Quality   | Encoding Speed | File Size         |
|-------------------------------------|------|-------|------------|-------------------|----------------|-------------------|
| Creator 2160p60 4K                  | MP4  | H.264 | AAC stereo | High              | Medium         |             Large |
| Creator 1440p60 2.5K                | MP4  | H.264 | AAC stereo | High              | Medium         |             Large |
| Creator 1080p60                     | MP4  | H.264 | AAC stereo | High              | Medium         |             Large |
| Creator 720p60                      | MP4  | H.264 | AAC stereo | High              | Medium         |             Large |
| Email 25 MB Large 3 Minutes 720p30  | MP4  | H.264 | AAC stereo | Depends on source | Fast           |     25 MB or less |
| Email 25 MB Medium 5 Minutes 480p30 | MP4  | H.264 | AAC stereo | Depends on source | Fast           |     25 MB or less |
| Email 25 MB Small 10 Minutes 288p30 | MP4  | H.264 | AAC mono   | Depends on source | Fast           |     25 MB or less |
| Social 100 MB 5 Minutes 1080p30     | MP4  | H.264 | AAC stereo | Depends on source | Fast           |    100 MB or less |
| Social 50 MB 5 Minutes 720p30       | MP4  | H.264 | AAC stereo | Depends on source | Fast           |     50 MB or less |
| Social 50 MB 10 Minutes 480p30      | MP4  | H.264 | AAC stereo | Depends on source | Fast           |     50 MB or less |
| Social 8 MB 3 Minutes 360p30        | MP4  | H.264 | AAC mono   | Depends on source | Fast           |      8 MB or less |

## Devices presets

HandBrake's Devices `Presets` target specific devices and classes of devices, such as mobile phones, tablets, TV media players, and game consoles.

Most Devices `Presets` use the broadly compatible [MP4 container](https://en.wikipedia.org/wiki/MPEG-4_Part_14), while a select few use the [Matroska Multimedia Container](https://en.wikipedia.org/wiki/Matroska) to support advanced features such as [Ultra HD 4K resolution](https://en.wikipedia.org/wiki/4K_resolution) and additional audio types compatible with target devices.

Each Devices `Preset` is named according to the device name or class, maximum resolution, and maximum frame rate it produces.

| Preset                               | Type    | Video     | Audio                            | Encoding Speed |
|--------------------------------------|---------|-----------|----------------------------------|----------------|
| Amazon Fire 2160p60 4K HEVC Surround | MP4     | **H.265** | AAC stereo; Dolby Digital (AC-3) | Slow           |
| Amazon Fire 1080p30 Surround         | MP4     | H.264     | AAC stereo; Dolby Digital (AC-3) | Medium         |
| Amazon Fire 720p30 Surround          | MP4     | H.264     | AAC stereo                       | Medium         |
| Android 1080p30                      | MP4     | H.264     | AAC stereo                       | Medium         |
| Android 720p30                       | MP4     | H.264     | AAC stereo                       | Medium         |
| Android 576p25                       | MP4     | H.264     | AAC stereo                       | Medium         |
| Android 480p30                       | MP4     | H.264     | AAC stereo                       | Medium         |
| Apple 2160p60 4K HEVC Surround       | MP4     | **H.265** | AAC stereo; Dolby Digital (AC-3) | Slow           |
| Apple 1080p60 Surround               | MP4     | H.264     | AAC stereo; Dolby Digital (AC-3) | Medium         |
| Apple 1080p30 Surround               | MP4     | H.264     | AAC stereo; Dolby Digital (AC-3) | Medium         |
| Apple 720p30 Surround                | MP4     | H.264     | AAC stereo; Dolby Digital (AC-3) | Medium         |
| Apple 540p30 Surround                | MP4     | H.264     | AAC stereo; Dolby Digital (AC-3) | Medium         |
| Chromecast 2160p60 4K HEVC Surround  | MP4     | **H.265** | AAC stereo; Dolby Digital (AC-3) | Slow           |
| Chromecast 1080p60 Surround          | MP4     | H.264     | AAC stereo; Dolby Digital (AC-3) | Medium         |
| Chromecast 1080p30 Surround          | MP4     | H.264     | AAC stereo; Dolby Digital (AC-3) | Medium         |
| Playstation 2160p60 4K Surround      | MP4     | H.264     | AAC stereo; Dolby Digital (AC-3) | Slow           |
| Playstation 1080p30 Surround         | MP4     | H.264     | AAC stereo; Dolby Digital (AC-3) | Medium         |
| Playstation 720p30                   | MP4     | H.264     | AAC stereo                       | Medium         |
| Playstation 540p30                   | MP4     | H.264     | AAC stereo                       | Medium         |
| Roku 2160p60 4K HEVC Surround        | **MKV** | **H.265** | AAC stereo; AAC, Dolby Digital (AC-3), Dolby Digital Plus (E-AC-3), DTS, or MP3 | Slow |
| Roku 1080p30 Surround                | MP4     | H.264     | AAC stereo; Dolby Digital (AC-3) | Medium         |
| Roku 720p30 Surround                 | MP4     | H.264     | AAC stereo; Dolby Digital (AC-3) | Medium         |
| Roku 576p25                          | MP4     | H.264     | AAC stereo                       | Medium         |
| Roku 480p30                          | MP4     | H.264     | AAC stereo                       | Medium         |
| Xbox 1080p30 Surround                | MP4     | H.264     | AAC stereo; Dolby Digital (AC-3) | Medium         |

## Matroska presets

HandBrake's Matroska `Presets` target software and devices supporting the [Matroska Multimedia Container](https://en.wikipedia.org/wiki/Matroska). MKV files support virtually all video and audio types, including many that the [MP4 container](https://en.wikipedia.org/wiki/MPEG-4_Part_14) does not.

Each Matroska `Preset` is named according to the video type, maximum resolution, and maximum frame rate it produces.

| Preset               | Type | Video | Audio         | Encoding Speed |
|----------------------|------|-------|---------------|----------------|
| AV1 MKV 2160p60 4K   | MKV  | AV1   | AAC stereo    | **Slow**       |
| H.265 MKV 2160p60 4K | MKV  | H.265 | AAC stereo    | **Slow**       |
| H.265 MKV 1080p30    | MKV  | H.265 | AAC stereo    | **Slow**       |
| H.265 MKV 720p30     | MKV  | H.265 | AAC stereo    | **Slow**       |
| H.265 MKV 576p25     | MKV  | H.265 | AAC stereo    | **Slow**       |
| H.265 MKV 480p30     | MKV  | H.265 | AAC stereo    | **Slow**       |
| H.264 MKV 2160p60 4K | MKV  | H.264 | AAC stereo    | Standard       |
| H.264 MKV 1080p30    | MKV  | H.264 | AAC stereo    | Standard       |
| H.264 MKV 720p30     | MKV  | H.264 | AAC stereo    | Standard       |
| H.264 MKV 576p25     | MKV  | H.264 | AAC stereo    | Standard       |
| H.264 MKV 480p30     | MKV  | H.264 | AAC stereo    | Standard       |
| VP9 MKV 2160p60 4K   | MKV  | VP9   | Opus stereo   | **Ultra slow** |
| VP9 MKV 1080p30      | MKV  | VP9   | Opus stereo   | **Ultra slow** |
| VP9 MKV 720p30       | MKV  | VP9   | Opus stereo   | **Ultra slow** |
| VP9 MKV 576p25       | MKV  | VP9   | Opus stereo   | **Ultra slow** |
| VP9 MKV 480p30       | MKV  | VP9   | Opus stereo   | **Ultra slow** |

## Hardware presets

HandBrake's Hardware `Presets` encode video using dedicated media engines provided by modern graphics hardware, and are optimized for maximum encoding speed.

More information on specific hardware encoders:

- [Intel Quick Sync Video (QSV)](video-qsv.html)
- [Nvidia NVENC](video-nvenc.html)
- [AMD VCN](video-vcn.html)
- [Microsoft Media Foundation (MF)](video-mediafoundation.html)
  - For Windows on ARM devices such as Qualcomm Snapdragon

HandBrake will disable any Hardware `Preset` where the associated hardware and software drivers are not detected, or are outdated.

| Preset                 | Type | Video | Audio      | Encoding Speed |
|------------------------|------|-------|------------|----------------|
| AV1 QSV 2160p60 4K     | MP4  | AV1   | AAC stereo | Very Fast      |
| H.265 NVENC 2160p60 4K | MP4  | H.265 | AAC stereo | Very Fast      |
| H.265 NVENC 1080p60    | MP4  | H.265 | AAC stereo | Very Fast      |
| H.265 QSV 2160p60 4K   | MP4  | H.265 | AAC stereo | Very Fast      |
| H.265 QSV 1080p60      | MP4  | H.265 | AAC stereo | Very Fast      |
| H.265 VCN 2160p60 4K   | MP4  | H.265 | AAC stereo | Very Fast      |
| H.265 VCN 1080p60      | MP4  | H.265 | AAC stereo | Very Fast      |
| H.265 MF 2160p60 4K    | MP4  | H.265 | AAC stereo | Very Fast      |
| H.265 MF 1080p60       | MP4  | H.265 | AAC stereo | Very Fast      |

## Production presets

HandBrake's Production `Presets` create mastering grade, short GOP, constant frame rate video with high bit rate audio, suited for professional video editing workflows. These presets typically create files much larger than most compressed sources and are not suitable for general use.

Production Proxy `Presets` create fast to encode, Intra-only video limited to one-quarter the desired editing resolution.

| Preset                    | Type | Video | Audio      | Max Resolution | Picture Quality | Frame Types | GOP Size | Encoding Speed    | File Size |
|---------------------------|------|-------|------------|----------------|-----------------|-------------|----------|-------------------|-----------|
| Production Max            | MP4  | H.264 | AAC stereo | Unlimited      | Max Master      | I/P         | 1-12     | Depends on source | Gigantic  |
| Production Standard       | MP4  | H.264 | AAC stereo | Unlimited      | Standard Master | I/P         | 1-12     | Depends on source | Huge      |
| Production Proxy 1080p    | MP4  | H.264 | AAC stereo | 1/4 2160p 4K   | Proxy           | Intra-only  | 1        | Fast              | Average   |
| Production Proxy 540p     | MP4  | H.264 | AAC stereo | 1/4 1080p HD   | Proxy           | Intra-only  | 1        | Very Fast         | Small     |

## Compatible replacements for deprecated or removed presets

From time to time, official `Presets` may be deprecated or removed. Compatible replacements are listed here.

### Legacy Web presets

| Preset                        | Compatible Preset                  | Notes                                                                                           |
|-------------------------------|------------------------------------|-------------------------------------------------------------------------------------------------|
| Discord Tiny 5 Minutes 240p30 | None                               | Web > Social 8 MB 3 Minutes 360p30 may be suitable for durations up to 3 minutes.               |
| Vimeo YouTube 720p30          | Web > Creator 720p60               |                                                                                                 |

As of HandBrake 1.6.0, the Vimeo YouTube HQ `Presets` have been renamed Creator, the Gmail `Presets` have been renamed Email 25 MB, and the Discord `Presets` have been renamed Social.

### Legacy Devices presets

| Preset                       | Compatible Preset                | Notes                                                                                           |
|------------------------------|----------------------------------|-------------------------------------------------------------------------------------------------|
| Apple 240p30                 | None                             | Obsolete.                                                                                       |
| Windows Mobile 1080p30       | General > Fast 1080p30           | Later Windows Mobile and Windows Phone devices, and Windows 10 Mobile devices.                  |
| Windows Mobile 720p30        | General > Fast 720p30            | Add vbv-bufsize=10000:vbv-maxrate=10000 to the additional encoder options for older devices.    |
| Windows Mobile 540p30        | General > Fast 480p30            | Add vbv-bufsize=4000:vbv-maxrate=4000 to the additional encoder options for older devices.      |
| Windows Mobile 480p30        | General > Fast 480p30            | Add vbv-bufsize=2000:vbv-maxrate=2000 to the additional encoder options for older devices.      |
| Xbox Legacy 1080p30 Surround | Devices > Apple 1080p30 Surround | Disable anamorphic, dimensions must be evenly divisible by 8, video must be H.264 Main Profile. |

### Legacy Matroska presets

| Preset          | Compatible Preset | Notes                                                                 |
|-----------------|-------------------|-----------------------------------------------------------------------|
| VP8 MKV 1080p30 | None              | Obsolete. AV1 is the successor to VP9, which is the successor to VP8. |
| VP8 MKV 720p30  | None              | Obsolete. AV1 is the successor to VP9, which is the successor to VP8. |
| VP8 MKV 576p30  | None              | Obsolete. AV1 is the successor to VP9, which is the successor to VP8. |
| VP8 MKV 480p30  | None              | Obsolete. AV1 is the successor to VP9, which is the successor to VP8. |

As of HandBrake 1.6.0, all 2160p60 presets have been renamed 2160p60 4K.

### Legacy 0.10.x presets

| Preset              | Compatible Preset                | Notes                                                                                                                                   |
|---------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Normal              | General > Fast 1080p30           | Decomb filter, peak limited to 30 FPS, slightly decreased video bit rate, improved motion quality, foreign audio search.                |
| High Profile        | General > HQ 1080p30 Surround    | Peak limited to 30 FPS, reduced video bit rate spikes, foreign audio search.                                                            |
| Universal           | None                             | General > Fast 576p25/480p30 may be suitable replacements where compatibility with ancient devices and surround sound are not required. |
| iPod                | None                             | Obsolete.                                                                                                                               |
| iPhone & iPod touch | Devices > Apple 540p30 Surround  | Decomb filter, slightly increased video bit rate, surround sound, foreign audio search.                                                 |
| iPad                | Devices > Apple 720p30 Surround  | Decomb filter, slightly decreased video bit rate, surround sound, foreign audio search.                                                 |
| AppleTV             | Devices > Apple 540p30 Surround  | Decomb filter, foreign audio search.                                                                                                    |
| AppleTV 2           | Devices > Apple 720p30 Surround  | Decomb filter, slightly decreased video bit rate, foreign audio search.                                                                 |
| AppleTV 3           | Devices > Apple 1080p30 Surround | Decomb filter, slightly decreased video bit rate, foreign audio search.                                                                 |
| Android             | Devices > Android 576p25/480p30  | Decomb filter, peak limited to 25 FPS (Android 576p25 only), slightly increased video bit rate, foreign audio search, chapter markers.  |
| Android Tablet      | Devices > Android 720p30         | Decomb filter, slightly increased video bit rate, foreign audio search, chapter markers.                                                |
| Windows Phone 8     | None                             | Obsolete.                                                                                                                               |

[^high-quality-settings-less-compatible]: Higher quality General `Presets` may include settings that are incompatible with older or slower devices.

[^video-hosting-services]: Creator presets are designed and tested to meet these specific services' video guidelines. Compatibility with other services is possible, but neither tested nor guaranteed.

[^email-size-limit]: Email presets are designed and tested to meet these specific services' file attachment size limits, which may change in the future. Compatibility with other services is possible, but neither tested nor guaranteed. It is generally recommended to use a [file hosting service](https://en.wikipedia.org/wiki/Comparison_of_file_hosting_services) when sharing large or long videos.

[^social-services]: Social presets are designed and tested to meet these specific services' video guidelines. Compatibility with other services is possible, but neither tested nor guaranteed.
