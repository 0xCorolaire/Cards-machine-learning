# CardsCVML

Computer Vision generative Dataset and Machine learning on playing cards

This project is using
  - python 3.6.7 and several libraries
  - opencv
  - CV libraries
  
  
## Explanation
1. Define the alphamask
  The alphamask has 2 purposes:
  - clean the border of the detected cards,
  - make that border transparent. Cards are not perfect rectangles because corners are rounded. We need to make transparent the zone between the real card and its bounding rectangle, otherwise this zone will be visible in the final generated images of the dataset
2. Function extract_card
  Extract from scene image (cv2/bgr) the part corresponding to the card and transforms it
  to fit into the reference card shape.
3. Finding the convex envelop
4. Load all card image, calculate their convex envelops
5. Generating scene with 2,3....x randoms cards on an image with a random background



