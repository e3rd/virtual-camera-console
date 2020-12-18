# Virtual camera console

Swap your background images and videos with ease. Write text to your webcam output.

## setup

* Recommendation: Start first this program, add a background, then start Zoom. (Be first to grab the camera.)

```bash
sudo modprobe v4l2loopback devices=3 # or use `modprobe -r v4l2loopback` if already started without multiple devices
```

## command_listener file

Whatever is written to the `command_listener` file in the `temp_dir`, is taken for a command. Useful if you make a shortcut to put there your clipboard contents without switching to console. (ex: run-or-raise `<Super><Ctrl>b,bash -c 'xclip -selection c -o | xargs echo ":b" > /tmp/ram/command_listener'`)