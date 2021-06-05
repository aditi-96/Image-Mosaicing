# Image Mosaicing
- Stitch multiple overlapping images together to form a single panoramic image
- The directory structure as shown below: 
  ```
  ├── code.ipynb           
  └── images            //images to be stitched
  ```

### Algorithm
1. Used SIFT with bruteforce matcher to find matches between overlapping images
2. Used RANSAC to find the homography matrix using the matched points
3. Transformed perspective of one of the 2 images to be joined using homography matrix and warpPerspective method.
4. Joined the 2 images and removed the vertical black pixels at the end of the joined images.
5. Repeated 3 and 4 until all the images in a set were joined together. 

### Results
- For all the set of images, the result is a panorama of given images
