# Detect, Crop, and Save Faces from Webcam and Video Files using Python

In the world of computer vision and image processing, face detection has gained a significant amount of attention. Applications range from photo tagging, surveillance, access control to even unlocking your smartphone. In this blog post, we'll discuss how to implement face detection using a webcam feed or from a video file using Python. As a bonus, we will also crop these faces and save them with timestamps!

See the full repo [here](https://github.com/artificialnouveau/face-archive)

## Prerequisites

Before diving into the implementation, you should ensure you have the following prerequisites:

- Python 3.7 or later.
- OpenCV, dlib, face_recognition, PIL (Pillow), and numpy Python libraries installed. You can do this using pip:

```sh
pip install opencv-python dlib face_recognition Pillow numpy
```

- A TrueType Font (TTF) file for writing timestamps onto images. We will use the DejaVuSans-Bold.ttf font file in our script.

Let's dive into the scripts!

## Face Detection from Webcam

Our first script is `webcam_face_detection.py`. This script uses the webcam feed, detects faces, crops them, and saves them with a timestamp. It creates a new directory named after the current date and saves all detected faces in this directory. Once you stop the script (by pressing 'q'), it combines all the faces detected during that session into a single image and saves it.

## Face Detection from Video File

Our second script is `video_face_detection.py`. This script is similar to the first one, but instead of a webcam feed, it takes a video file as input. The script reads the video file frame by frame and performs face detection, similar to the webcam script. Detected faces are saved in a new directory named after the current date. 

For both these scripts, we are using the dlib library's HOG-based model for face detection. This model is quite accurate and performs well on a variety of datasets.

## Handling Duplicate Faces

An interesting challenge in face detection tasks is handling duplicate faces or faces of the same person appearing multiple times. We addressed this issue by introducing face recognition, which helps us to recognize the same person even in different frames. We utilized the face_recognition library's compare_faces function to identify and ignore duplicates. 

## Running the Scripts

Running these scripts is as simple as running a python command. For webcam script:

```sh
python webcam_face_detection.py
```

And for the video script:

```sh
python video_face_detection.py
```

Remember to replace `'video.mp4'` placeholder in the script with the path to your video file before running the video script.

## Conclusion

With these scripts, you can easily perform face detection, crop detected faces, and save them for further processing. This can be a stepping stone for more advanced face-related tasks like face recognition, emotion detection, and much more. Remember that the face recognition used in these scripts is not 100% accurate and can have a harder time recognizing the same person in different lighting conditions, from different angles, with different facial expressions, etc. These scripts are intended for educational and personal use and may not be suitable for high-accuracy face recognition requirements.

We look forward to seeing what you build with this!
