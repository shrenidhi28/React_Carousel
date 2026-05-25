# Ex05 Image Carousel
## Date: 25-06-26

## AIM
To create a Image Carousel using React 

## ALGORITHM
### STEP 1 Initial Setup:
Input: A list of images to display in the carousel.

Output: A component displaying the images with navigation controls (e.g., next/previous buttons).

### Step 2 State Management:
Use a state variable (currentIndex) to track the index of the current image displayed.

The carousel starts with the first image, so initialize currentIndex to 0.

### Step 3 Navigation Controls:
Next Image: When the "Next" button is clicked, increment currentIndex.

If currentIndex is at the end of the image list (last image), loop back to the first image using modulo:
currentIndex = (currentIndex + 1) % images.length;

Previous Image: When the "Previous" button is clicked, decrement currentIndex.

If currentIndex is at the beginning (first image), loop back to the last image:
currentIndex = (currentIndex - 1 + images.length) % images.length;

### Step 4 Displaying the Image:
The currentIndex determines which image is displayed.

Using the currentIndex, display the corresponding image from the images list.

### Step 5 Auto-Rotation:
Set an interval to automatically change the image after a set amount of time (e.g., 3 seconds).

Use setInterval to call the nextImage() function at regular intervals.

Clean up the interval when the component unmounts using clearInterval to prevent memory leaks.

## PROGRAM

```
import { useState } from "react";

function Car() {
  const images = [
    "https://picsum.photos/300/200?1",
    "https://picsum.photos/300/200?2",
    "https://picsum.photos/300/200?3"
  ];

  const [index, setIndex] = useState(0);

  return (
    <div>
      <img src={images[index]} alt="img" width="300" />

      <br />

      <button onClick={() => setIndex(index - 1)}>
        Prev
      </button>

      <button onClick={() => setIndex(index + 1)}>
        Next
      </button>
    </div>
  );
}

export default Car;

```

## OUTPUT
<img width="1486" height="943" alt="image" src="https://github.com/user-attachments/assets/f65fe6f2-5f0a-4ae4-96cf-88ad558ef46e" />


## RESULT
The program for creating Image Carousel using React is executed successfully.
