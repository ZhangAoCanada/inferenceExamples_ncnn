# Inference Object Detection/Segmentation models with ncnn

## Requirements

So I only inferenced them on CPU(laptop), haven't tried GPU yet.

```
OS:           Linux (Ubuntu 18.04)
Libraries:    OpenCV, ncnn
```

More info could be found at [OpenCV](https://opencv.org/) and [ncnn](https://github.com/Tencent/ncnn)

*Note:* execute the following line (or add it to `~/.bashrc`/`~/.zshrc`)
```bash
export ncnn_DIR=$(path_to_your_ncnn_directory)/build/install/lib/cmake/ncnn
```

## How to use

Basically, the name of the folder indicates which model it contains. So go into the that directory, try
```
./build.sh
```
for compiling it. Change the image/video path in `./inference.sh` and run
```
./inference.sh
```

## Waiting for improvement

- Consistency: make the usage of all inferences as `./program mode path_to_video_or_image`, where mode can be 0, 1, 2, with 0 as webcam mode, 1 as image mode, 2 as video mode. Currently, all of them are following this rule.
