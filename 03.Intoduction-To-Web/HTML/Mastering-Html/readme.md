## chapter 1

- tags : p
- element : <p>This is p content</p>
- self-closing tag : br, hr, img , meta

## chapter 5

```
<!-- link to open in new tab -->
<a
      href="https://chaicode.com/learn"
      target="_blank"
      rel="noopener noreferrer"
      >Learn More</a
    >

     <!-- link to download file  that hosted in same domain -->
    <a href="files/sample.pdf" download>Download Sample PDF</a>
```

## Multimedia

```
<!-- Multimedia -->

<video controls width="250">
  <source src="/shared-assets/videos/flower.webm" type="video/webm" />

  <source src="/shared-assets/videos/flower.mp4" type="video/mp4" />
  <p>Your browser does not support video </p>

  Download the
  <a href="/shared-assets/videos/flower.webm">WEBM</a>
  or
  <a href="/shared-assets/videos/flower.mp4">MP4</a>
  video.
</video>

<!-- attributes -->
controls,
controlslist="nodownload nofullscreen noremoteplayback"
disablepictureinpicture
poster="https://someposter.png"
playsinline
width , height, autoplay, loop, muted

```

## multimedia

```js
// to embed yt videos in html we used iframe tag
// you have to used /embed/videoID
// when you paste video link it includes ?watch=videoID so remove it and add /embed/videoId
// some other query you can add in src like
- ?rel=0&modestbranding=1
// rel=0 :- it helps to suggest the other videos from same channel after videos playback finish if not give rel=0 then it show any videos from any channel
// - ?autoplay=	1 or 0	Makes the video start playing automatically when the page loads (use with caution, as it may be blocked if not muted).
/*
<iframe
      width="560"
      height="315"
      src="https://www.youtube.com/embed/q8EevlEpQ2A?modestbranding=1&rel=0"
      title="YouTube video player"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen
    ></iframe>
*/
```
