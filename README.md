# imagegallery
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Gallery</title>
    <link rel="stylesheet" href="styles.css"> <!-- Link to your CSS file -->
</head>
<body>
    <div class="gallery">
        <div class="gallery-item">
            <img src="image1.jpg" alt="Image 1">
        </div>
        <div class="gallery-item">
            <img src="image2.jpg" alt="Image 2">
        </div>
        <div class="gallery-item">
            <img src="image3.jpg" alt="Image 3">
        </div>
        <!-- Add more gallery items as needed -->
    </div>
</body>
</html>

CSS

/* Reset default styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Center align the gallery */
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0; /* Light gray background */
}

/* Gallery grid layout */
.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); /* Responsive grid, minimum 300px width */
    gap: 20px; /* Gap between grid items */
    max-width: 1200px; /* Max width of the gallery */
    padding: 20px;
}

/* Style each gallery item */
.gallery-item {
    overflow: hidden; /* Hide overflowing content */
    border-radius: 8px; /* Rounded corners */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Shadow effect */
}

.gallery-item img {
    width: 100%; /* Ensure images fill their container */
    height: auto; /* Maintain aspect ratio */
    display: block; /* Remove default image spacing */
    transition: transform 0.2s ease; /* Smooth zoom effect */
}

.gallery-item:hover img {
    transform: scale(1.1); /* Zoom in slightly on hover */
}
