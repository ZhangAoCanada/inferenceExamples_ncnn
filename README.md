# Inference Object Detection/Segmentation models with ncnn

## Requirements

So I only inferenced them on CPU(laptop), haven't tried GPU yet.

```
OS:           Linux (Ubuntu 18.04), MacOS 11.1
Libraries:    OpenCV, ncnn
```

More info could be found at [OpenCV](https://opencv.org/) and [ncnn](https://github.com/Tencent/ncnn)

*Note:* execute the following line (or add it to `~/.bashrc`/`~/.zshrc`)
```bash
export ncnn_DIR=$(path_to_your_ncnn_directory)/build/install/lib/cmake/ncnn
```

## How to use

Basically, the name of the folder indicates which model it contains. So go into the that directory, try
```bash
./build.sh
```

- If you want to inference on a specific video, change the video path in `./inference.sh` which follows the format as
```bash
./build/$(target_executable) 2 $(path_to_your_video)
```
then run `./inference.sh`.

- If you want to inference on a specific image, change the image path in `./inference.sh` which follows the format as
```bash
./build/$(target_executable) 1 $(path_to_your_image)
```
then run `./inference.sh`.

- If you want to inference on a webcam(like the one that most laptops have), run
```bash
./webcam.sh
```

## Waiting for improvement

- Consistency: make the usage of all inferences as `./program mode path_to_video_or_image`, where mode can be 0, 1, 2, with 0 as webcam mode, 1 as image mode, 2 as video mode. Currently, all of them are following this rule.
