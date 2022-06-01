## Extract Video to Image

### Requirements
1. Python 3.x
2. Pip3 
3. Virtual Environment (venv) 
4. Sample video file (.mp4 format) 

### Steps 

1. Create folder for your project.
    
    ```sh
    mkdir -p py-video2img/frames    
    cd py-video2img
    ```

2. Create virtual environment using `venv`, then activate. (Skip if you already have existing)
    
    ```sh
    python3 -m venv project-video
    
    # activate venv
    source project-video/bin/activate
    ```

3. Install `opencv`

    ```sh
    # version 4.5.5.64
    pip3 install opencv-python
    ```

4. Move your video/mp4 to project folder.
5. Open your terminal and run `python3`

    ```python
    import cv2
    # change the <video-filename> that you want to capture per frame
    vidcap = cv2.VideoCapture('<video-filename>.mp4')
    success,image = vidcap.read()
    count = 0
    while success:
        cv2.imwrite("frames/frame%d.jpg" % count, image)     # save frame as JPEG file      
        success,image = vidcap.read()
        print('Read a new frame: ', success)
        count += 1
    ```
6. Images will be save inside `py-video2img/frames` folder.