## Extract Video on Youtube

### Requirements
1. Python 3.x
2. Pip3 
3. Virtual Environment (venv) 

### Steps 

1. Create folder for your project.
    
    ```
    mkdir py-extract-youtube
    cd py-extract-youtube
    ```

2. Create virtual environment using `venv`, then activate.
    
    ```sh
    python3 -m venv project-video
    
    # activate venv
    source project-video/bin/activate
    ```

3. Install `pytube`

    ```
    pip3 install pytube
    ```

4. Open the `extract-youtube-video.py` and change 
   
    ```python
    yt = YouTube('<youtube-url-you-want-to-download')

    # sample
    yt = YouTube('https://www.youtube.com/watch?v=hm_d4UkKKJo') 
    ```

5. Open python cli by typing on your terminal `python3`
6. File will be saved as MP4 and stored to current directory.