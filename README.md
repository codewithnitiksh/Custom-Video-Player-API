# Custom Video Player API

Welcome to the Custom Video Player API! This project provides a customizable video player that can be easily embedded into your web applications. It supports multiple video qualities and includes features like play, pause, volume control, and fullscreen mode.

## Features

- **Multiple Video Quality Support**: Easily switch between different video qualities.
- **Fullscreen Support**: Enjoy videos in fullscreen mode.
- **Dynamic Data Handling**: Load video data dynamically through a URL-encoded JSON format.

## Getting Started

To use the Custom Video Player API, you need to provide a JSON object containing the video details, including title, poster, and video URLs. Below is an example of how to implement the player:

### Implementation Examples

```html
<div id="video-container">
    <script>
        const videoData = {
            title: "Demo Video",
            poster: "https://codewithnitiksh.github.io/sample-data/images/spider-man-no-way-home-u7sd6vs76v.webp", // Replace with your poster URL
            urls: [
                { "url": "https://codewithnitiksh.github.io/sample-data/videos/3195394-sd_640_360_25fps.mp4", "quality": "360p" },
                { "url": "https://codewithnitiksh.github.io/sample-data/videos/Happiness(240p).mp4", "quality": "240p" },
                { "url": "https://codewithnitiksh.github.io/sample-data/videos/Happiness(144p).mp4", "quality": "144p" }
            ]
        };

        const jsonString = encodeURIComponent(JSON.stringify(videoData));
        const iframeSrc = "https://codewithnitiksh.github.io/Custom-Video-Player-API/?data=" + jsonString;

        // Create the iframe dynamically
        const iframe = document.createElement('iframe');
        iframe.src = iframeSrc;
        iframe.title = "Video Player";
        iframe.allowFullscreen = true; // Allow fullscreen
        iframe.allow = "fullscreen"; // Set the permissions policy
        document.getElementById('video-container').appendChild(iframe);
    </script>
</div>
```
```html
<div id="video-container"></div>
<script>
    // Function to create the iframe and embed the video player
    function createVideoPlayer(videoData, containerId) {
        const jsonString = encodeURIComponent(JSON.stringify(videoData));
        const iframeSrc = "https://codewithnitiksh.github.io/Custom-Video-Player-API/?data=" + jsonString;

        // Create the iframe dynamically
        const iframe = document.createElement('iframe');
        iframe.src = iframeSrc;
        iframe.title = "Video Player";
        iframe.allowFullscreen = true; // Allow fullscreen
        iframe.allow = "fullscreen"; // Set the permissions policy
        iframe.style.width = "100%";
        iframe.style.height = "500px"; // Optional: Adjust the height

        // Append the iframe to the container
        const container = document.getElementById(containerId);
        container.appendChild(iframe);
    }

    // Define the video data
    const videoData = {
        title: "Demo Video",
        poster: "https://codewithnitiksh.github.io/sample-data/images/spider-man-no-way-home-u7sd6vs76v.webp",
        urls: [
            { "url": "https://codewithnitiksh.github.io/sample-data/videos/3195394-sd_640_360_25fps.mp4", "quality": "360p" },
            { "url": "https://codewithnitiksh.github.io/sample-data/videos/Happiness(240p).mp4", "quality": "240p" },
            { "url": "https://codewithnitiksh.github.io/sample-data/videos/Happiness(144p).mp4", "quality": "144p" }
        ]
    };

    // Call the function to create and embed the video player in the container
    createVideoPlayer(videoData, 'video-container');
</script>
```


## Accessing the API

You can access the live demo of the Custom Video Player API at the following link:
[Live Demo](https://codewithnitiksh.github.io/Custom-Video-Player-API/)

<iframe src="https://www.linkedin.com/embed/feed/update/urn:li:ugcPost:7243199163310477313" height="509" width="504" frameborder="0" allowfullscreen="" title="Embedded post"></iframe>

## Usage

This API is suitable for developers looking to integrate video playback functionality into their applications. You can easily customize the player’s behavior and appearance to fit your project requirements.

## License

This project is open-source and available for public use. Feel free to contribute, modify, and use it in your projects!
