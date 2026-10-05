# Don't slouch! 

A five-minute installation process will keep your back straight while working at a computer. 

Sends a notification periodically to sit up straight (every 15 minutes by default)
Supports MacOS only. 

### Installation

Open the terminal and enter the following command: 
```crontab -e```

Enter the following line of code into the crontab: 
```*/15 * * * * osascript -e 'display notification "Sit up straight"' > /dev/null```

Save the crontab and you're done! 

### Customization
If you want to change the frequency, change the 15 to the number of minutes between notifications. 
Recommended to use intervals of 10, 12, 15, 20, or 30 minutes.
Hasn't been tested with non-factors of 60; may skip notifications if you use different intervals. 

### What if my computer is asleep?
Don't worry; you won't get notifications if your computer is asleep because the crontab won't run. 

### How it works:
The crontab can schedule tasks and uses the following format:

MINUTE, HOUR, DAY OF MONTH, MONTH, DAY OF WEEK

A * means it doesn't matter.
The */15 indicates a step size of 15, so the program will run every 15 minutes.
