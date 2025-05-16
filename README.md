# Ex.08 Design of Interactive Image Gallery
# Date:
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
``<html>
    <head>
    <title>Image Gallery</title>
    <style>
        body {
           
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
    background-color: #add8e6; /* Light blue */
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 100vh;
}

        

        .header {
            text-align: center;
            padding: 10px;
            background-color: #1ba1e4a4;
            width: 100%;
            height:100px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            font-family:monospace;
        
        }

        .header h1 {
            font-size: 2.5rem;
            color: #9c28a9;
        }

        .header p {
            font-size: 1.2rem;
            color:#000000;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            padding: 20px;
            margin: 20px 0 10px 0;
            width: 90%;
            max-width: 1200px;
        }

        .gallery-item {
            border-radius: 10px;
            overflow: hidden;
            position: relative;
            cursor: pointer;
            border: 10px solid #2897d6;
            margin-right: 40px;
        }

        .gallery-item img {
            width: 100%;
            height:100%;
            object-fit: cover;
            display: block;
        }

        .gallery-item:nth-child(1) {
            grid-column: span 2;
            grid-row: span 2;
        }

        .gallery-item:nth-child(3) {
            grid-column: span 2;
        }

        .gallery-item:nth-child(6) {
            grid-column: span 2;
        }

        .gallery-item::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom right, rgba(255, 255, 255, 0.2), rgba(0, 0, 0, 0.2));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .gallery-item:hover::after {
            opacity: 1;
        }

        .footer {
            text-align: center;
            margin-top: 20px;
            padding: 10px;
            width: 100%;
            height:40px;
            background-color: #1d9ae8;
        }

        .footer p{
            font-size: 1.2rem;
            color: #000000;
        }

        #lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        #lightbox img {
            max-width: 90%;
            max-height: 80%;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
        }

        #lightbox:target {
            display: flex;
        }

        #lightbox .close {
            position: absolute;
            top: 10px;
            right: 10px;
            background: #1aade8;
            border: none;
            font-size: 2rem;
            cursor: pointer;
        }
    </style>
</head>
<body>

<div class="header">
    <h1>Image Gallery</h1>
   
</div>

<div class="gallery">
    <div class="gallery-item" onclick="showAlert('Image 1 clicked!')">
        <img src="c:\Users\admin\Downloads\shih-tzu-temperament.jpeg-900x510.jpg" alt="Image 1">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 2 clicked!')">
        <img src="c:\Users\admin\Downloads\KOA_Nassau_2697x1517.jpg" alt="Image 2" >
    </div>
    <div class="gallery-item" onclick="showAlert('Image 3 clicked!')">
        <img src="c:\Users\admin\Downloads\hq720.jpg"alt="Image 3">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 4 clicked!')">
        <img src="c:\Users\admin\Downloads\images.jpeg" alt="Image 4">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 5 clicked!')">
        <img src="c:\Users\admin\Downloads\images (1).jpeg" alt="Image 5">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 6 clicked!')">
        <img src="c:\Users\admin\Downloads\Shih-Tzu.jpg" alt="Image 6">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 7 clicked!')">
        <img src="c:\Users\admin\Downloads\istockphoto-1250262738-2048x2048.jpg"  alt="Image 7">
    </div>
    
    <div class="gallery-item" onclick="showAlert('Image 8 clicked!')">
        <img src="c:\Users\admin\Downloads\istockphoto-476533275-612x612.jpg" alt="Image 8">
    </div>
</div>

<div id="lightbox">
    <button class="close" onclick="closeLightbox()">&#215;</button>

    <img src="" id="lightbox-img" alt="Full Image">
</div>

<div class="footer">
    <p><b>Designed by Safira Barveen</b></p>
</div>

<script>
    function showAlert(message) {
        alert(message);
    }

    function openLightbox(imageSrc) {
        document.getElementById('lightbox-img').src = imageSrc;
        document.getElementById('lightbox').style.display = 'flex';
    }

    function closeLightbox() {
        document.getElementById('lightbox').style.display = 'none';
    }

    const galleryItems = document.querySelectorAll('.gallery-item');
    galleryItems.forEach(item => {
        item.addEventListener('click', () => {
            const imgSrc = item.querySelector('img').src;
            openLightbox(imgSrc);
        });
    });
</script>

</body>
</html>
```



# OUTPUT:
![Screenshot 2025-05-16 231126](https://github.com/user-attachments/assets/150ec482-2e08-48b4-8587-df9a43792cba)
![Screenshot 2025-05-16 231145](https://github.com/user-attachments/assets/fd571a3c-3810-4830-90c0-4c67bb30666e)
![Screenshot 2025-05-16 231200](https://github.com/user-attachments/assets/ab928e80-4d4f-493e-ae52-f34b137cc2d1)
![Screenshot 2025-05-16 231221](https://github.com/user-attachments/assets/b5cb2508-65d4-4133-ba9f-05ffb6cab1fa)
![Screenshot 2025-05-16 231234](https://github.com/user-attachments/assets/30362151-baa7-4a8a-a6bd-19b2bb286671)





# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
