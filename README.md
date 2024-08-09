# HoverView Gallery

The HoverView Gallery project is a web application built using HTML, CSS, and JavaScript. Its purpose is to allow users to view images in a larger format by hovering over smaller thumbnail images.

## Main Features

### Image Hover Preview
Users can hover over thumbnail images to view a larger version of the selected image. This feature involves using JavaScript to dynamically update the main image displayed on the screen based on the hovered thumbnail.
## Preview
![Preview](https://github.com/TechTrooperAayush/HoverView-Gallery-jsProject/blob/80b00d02ebdd96eef6b3410df352e14a972d52a3/HoverView%20Gallery/imgs/Preview.jpg)


## Usage
1. Open the `index.html` file in a web browser.
2. Hover over any of the thumbnail images in the gallery.
3. The main image will update to display the hovered image in a larger view.

## Technologies Used
- HTML
- CSS
- JavaScript

## Project Logic Explanation

### Overview
The **HoverView Gallery** is a dynamic image gallery where users can hover over thumbnail images to view them in a larger format. The logic is implemented using HTML, CSS, and JavaScript, with each part playing a crucial role in achieving the desired functionality.

### HTML Structure
- **Container:** The main container is a flexbox that holds two key sections:
  - **Thumbnail Gallery (`img-box`):** This section contains smaller versions of the images (thumbnails) that users can hover over. Each thumbnail is an `<img>` element.
  - **Main Image Display (`package`):** This section displays the larger version of the image that corresponds to the hovered thumbnail. The large image is also an `<img>` element.

### CSS Styling
- **Layout:** The project uses CSS flexbox to align the `img-box` and `package` sections horizontally within the container. This ensures that the gallery looks neat and the images are evenly spaced.
- **Styling:** Additional CSS is used to add shadows, borders, and padding to enhance the visual appeal of the gallery.

### JavaScript Logic
- **Event Handling:** The key functionality is achieved through JavaScript, where `mouseover` events are used to detect when a user hovers over a thumbnail.
  - **Event Listener:** For each thumbnail image (`Selected-img`), a `mouseover` event listener is attached.
  - **Image Swap:** When a user hovers over a thumbnail, the `src` attribute of the main image (`Show-img`) is updated to match the `src` of the hovered thumbnail. This effectively swaps the large image with the one corresponding to the thumbnail.
  
  ```javascript
  let selectimg = document.querySelectorAll(".Selected-img");
  let showimg = document.querySelector(".Show-img");
  
  selectimg.forEach(function(img){
      img.addEventListener("mouseover",function(e){
          showimg.src = e.target.src;
      })
  })


### Looping Through Thumbnails
The JavaScript code uses `forEach` to loop through all the thumbnail images and attaches the event listener to each one, ensuring that any thumbnail hovered over will trigger the image swap.

## Summary
The logic of the project is quite straightforward:

- The HTML structure provides the foundation with sections for thumbnails and the main display.
- CSS ensures the gallery is visually appealing and well-aligned.
- JavaScript handles the interactivity, allowing users to see a larger version of an image when they hover over a thumbnail.

This combination creates a smooth, user-friendly experience where users can easily preview images by simply hovering over them.



## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
