<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phone Webcam</title>
</head>
<body>
    <h1>Phone Webcam</h1>
    <video id="video" width="100%" autoplay></video>
    <script>
        navigator.mediaDevices.getUserMedia({ video: true })
            .then(stream => {
                document.getElementById('video').srcObject = stream;
            })
            .catch(error => {
                console.error("Error accessing camera:", error);
            });
    </script>
</body>
</html>
