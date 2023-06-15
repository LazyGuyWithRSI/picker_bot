# Pick and Place Robot
## Pick and place robot utilizing computer vision

![pickerbot](https://github.com/LazyGuyWithRSI/picker_bot/assets/72579524/bb77bf60-588c-48b6-a611-3b8f46f03f70)

https://github.com/LazyGuyWithRSI/picker_bot/assets/72579524/45c4740a-b62d-4c5d-a7f2-4dbaa8470a9b

The control software for this robot was a massive learning experience. It was the first time I had to build a multithreaded application that could handle communication with multiple serial devices AND another process. Using safe message queues for this was a good solution.

The software consists of 2 major parts:
- the C# GUI with all the control logic
- the C++ OpenCV vision application, which handled all the heavy image processing to find items in the camera's field of view and figuring out how to grab them with the gripper.

Example of the UI mid-picking operation. The robot would pick a whole "pack" of parts (100 packs consisting of 1 part A, 1 part B, 3 part C, etc):
![picker_new_ui_1](https://github.com/LazyGuyWithRSI/picker_bot/assets/72579524/e390c701-7cd6-4590-afe8-9fd27fccc2e8)

The testing UI shown below was not the final product. The test UI was in WinForms, with the new UI in WPF and much more user friendly. Why winforms and WPF? My partner (who was working primarily on the hardware) used to be a C# guy, so I figured I would keep as much of the project in C# and I could.

### Sadly, the robot has been decomissioned and I only have screengrabs from a video I took years ago.
![IMG_20201002_153116](https://github.com/LazyGuyWithRSI/picker_bot/assets/72579524/103ccd4b-4182-4ee4-8643-0606bc86909c)

![vlcsnap-2023-06-13-18h46m15s426](https://github.com/LazyGuyWithRSI/picker_bot/assets/72579524/50f5f93f-1ee9-4d3a-9fe1-1b0dde6db811)

![vlcsnap-2023-06-13-18h47m05s119](https://github.com/LazyGuyWithRSI/picker_bot/assets/72579524/fa4e92d7-8a37-4c5b-9ffb-b289b4f1aa37)

There was a V2 robot planned, which could move at 5 times the speed. However, the project was put on hold and it was never finished.
