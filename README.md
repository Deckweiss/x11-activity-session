# x11-activity-session

A script to start a set of programs and put their windows in specified arrangements. 

![x11-activity-session](https://user-images.githubusercontent.com/10449980/209897951-21c7ec9c-e784-4349-9c9a-a44634a26a6a.gif)


# Usecases:
1. Instead of juggling multiple apps and windows every time you start a specific workflow, you can write a config once, run this through a `.desktop` file and be ready to start your task in no time.
2. In conjunction with KDE Activities and its feature of triggering scripts.

If you put a script into `~/.local/share/kactivitymanagerd/activities/ACTIVITY_UUID/started`, it will be executed when the activity starts. Other supported events are `stopped`, `activated` and `deactivated`.

# Example config file:
```
{
  "apps": [
    {
      "exec": "kalendar",
      "position": "0,0",
      "size": "960,1016"
    },
    {
      "exec": "dolphin",
      "position": "960,0",
      "size": "960,493"
    },
    {
      "exec": "konsole",
      "position": "960,523",
      "size": "960,493"
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
