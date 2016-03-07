# Changing full screen fade and warning message time

1. Go to about:config
2. To change the animation time for entering and leaving:
  - full-screen-api.transition-duration.enter
    - First integer is how long to animate in, second integer is how long to play the video once it's initialized. Recommended value: 50 0
  - full-screen-api.transition-duration.leave
    - Not sure what the first integer does, I assume it's how long before the video stops playing?
    - Second integer is time for animate out. Recommended value: 0 50
  - full-screen-api.warning.timeout
    - How long to have the full-screen warning dialog on. Something like 1000 and below should be good.
