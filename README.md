Make all the Python scripts executable (by default they are set to non-executable when downloaded from Github, or anywhere for that matter)
```bash
find . -name "*.py" -exec chmod +x {} \;
```

Then build:
```bash
$ cd ~/f110_ws
$ catkin_make
```

The generated devel and build folders at the root of the workspace are where the linked libraries and the compiled code in machine language resides. Source the environment using
```bash
$ source devel/setup.bash
```

You can now run a launch file using the following. 
```bash
$ roslaunch gap_finding gap_finding_sim.launch
```

TROUBLESHOOTING
If for some reason you get a build error, try deleting the CMakeLists.txt file and running catkin_make again. 