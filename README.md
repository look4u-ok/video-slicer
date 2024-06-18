# Video Frame Slicer and Subtitle Extractor

## Overview
This Python program slices multiple frames from a given video and extracts the corresponding subtitles from an SRT file. It uses OpenCV for video processing and the pysubs2 library for subtitle parsing. 

## Requirements
* Python 3.x
* opencv-python
* pysubs2

## Usage
1. Place your video file and subtitle file in the same directory as the script.
2. Run the script:
```bash
python slice_and_extract.py --video_path <path_to_video> --srt_path <path_to_srt> --num_frames <number_of_extracted_frames> --output_paht <path_to_output>
```

## Arguments
* `--video_path`: Path to the video file.
* `--srt_path`: Path to the subtitle file.
* `--num_frames`: The number of frames to be sliced and the corresponding subtitles to be extracted.
* `--output_path`: Path to the output directory where the frames and subtitles will be saved.

## Output
The program will generate:

Extracted frames as images saved in the frames directory.
A text file subtitles.txt containing the subtitles corresponding to the specified timestamps.


## Example
If you run the following command:
```bash
python slice_and_extract.py --video_path demo/demo.mp4 --srt_path demo/demo.srt --num_frames 4 --output_path demo/
```
You will get:

Four image files in the frames directory: demo_mp4_frame_00:01.jpg, demo_mp4_frame_00:05.jpg, demo_mp4_frame_00:09.jpg, demo_mp4_frame_00:13.jpg.
A subtitles.txt file containing the subtitles at 00:01, 00:05, and 00:09 and 00:13.


