---
title: "Music and Audio"
datePublished: Thu Apr 18 2024 04:41:54 GMT+0000 (Coordinated Universal Time)
cuid: clv4r8ls2000308mdc3vegqzq
slug: music-and-audio

---

Sound is another way to engage your visitors, pass on information, or evoke emotions.

```xml
<audio>
    <!--audio file-->
</audio>
```

`source` tag is used to add source options for audio.

```xml
<audio>
<source src="audiofile.mp3" type="audio/mpeg">
<source src="audiofile.ogg" type="audio/ogg">
</audio>
```

The source tag is an empty tag.

`type` attribute adds the format.

Just like video, you can add audio files in different formats. Common audio formats are MP3, OGG and WAV.

You can use **autoplay, muted** and **loop** attributes to control the behavior of the multimedia element. Just like **controls,** these attributes have their default values omitted.