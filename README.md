# x11-activity-session

A script to start a set of programs and put their windows in specified arrangements. 

Usecases:
1. Called through a `.desktop` file for opening multiple apps in specified arrangements at once.
2. In conjunction with KDE Activities and its feature of triggering scripts.

If you put a script into `~/.local/share/kactivitymanagerd/activities/ACTIVITY_UUID/started`, it will be executed when the activity starts. Other supported events are `stopped`, `activated` and `deactivated`.

# Example config file:
```
{
  "apps": [
    {
      "exec": "kalendar",
      "position": "0,0",
      "size": "960,1016",
      "detectionDelay": 1
    },
    {
      "exec": "dolphin",
      "position": "960,0",
      "size": "960,493",
      "detectionDelay": 0.5
    },
    {
      "exec": "konsole",
      "position": "960,523",
      "size": "960,493",
      "detectionDelay": 0.5
    }
  ]
}
```

# Setup
1. download `x11-activity-session`
2. move it somewhere in your PATH like `~/.local/bin`
3. make it executable
4. create a config file
5. run it through a terminal as a test
6. automate activities
