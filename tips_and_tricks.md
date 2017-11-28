# Tips & Tricks

Random tips & tricks that don't really belong to a [specific project](PROJECTS.md), but are useful in general.

## Udacity simulator: Prevent `Player.log` file creation

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

---

Help wanted - add your knowledge, tips & tricks by editing this file! 🎉
