# Tips & Tricks

Random tips & tricks that don't really belong to a [specific project](PROJECTS.md), but are useful in general.

## Udacity simulator: Prevent Player.log file creation

The log files created by the Udacity simulator can easily be huge and fill up your whole disk space. This
handy trick disables log file creation:

```bash
# on Linux
rm ~/.config/unity3d/Udacity/self_driving_car_nanodegree_program/Player.log
mkdir -p ~/.config/unity3d/Udacity/self_driving_car_nanodegree_program/Player.log

# on Mac
rm ~/Library/Logs/Unity/Player.log
mkdir -p ~/Library/Logs/Unity/Player.log
```

## Show graphical windows from within a Docker image on Mac

If you run a Docker image on Mac you don't have any graphical output. However, if you have XQuartz installed and follow [this blogpost](https://medium.com/@mreichelt/how-to-show-x11-windows-within-docker-on-mac-50759f4b65cb), you can see X11 windows on your Mac!

---

Help wanted - add your knowledge, tips & tricks by editing this file! 🎉
