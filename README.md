# GCCE_verification
This repo is the verification code for "Automatic Edge Error Judgment in Figure Skating Using 3D Pose Estimation From Inertial Sensors."

# Example of sensing results using IMU
We used Perception Neuron 3, inertial sensor units from NOITOM, to analyze figure skating jumps.

![Sensing results using IMU](https://github.com/ryota-takedalab/GCCE_verification/assets/102862947/32e15852-7197-4cc5-ad77-ad97d554a7d0)

# Usage
You can validate our paper's data using the following code.
`python main.py training.csv`
By default, The model is trained using preprocessed data of 17 joint position coordinates of the whole body and the left skate pose angle, each at 60 fps.

The joint position coordinates and the left skate pose angle can each be downsampled to 12 fps using the option `--pos_fps 12` and `--rot fps 12`.

If you want to use only either the joint position coordinates or the left skate pose angle, options `--no_pos` and `--no_rot` can be used to reduce the unnecessary features.

In the random validation, you can change the number of trials using the option `-t (int)` or `--trials (int)`.

If you want to use keypoints only on the lower half of the body, not the whole body, you can use the option `--lower`.

You can save the validation result as a graph using the option `--plot`

# Author

Ryota Tanaka - tanaka.ryota@g.sp.m.is.nagoya-u.ac.jp
