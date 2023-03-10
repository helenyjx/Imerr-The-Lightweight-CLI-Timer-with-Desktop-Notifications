# Jiaxin-week10-mini-repo

## Goal
This demo will tell you how to use imerr, it is a command-line interface (CLI) timer that allows users to set a specific amount of time for a task or activity. Once the timer is started, imerr runs silently in the background and sends desktop notifications when the timer is up. This can be particularly helpful for users who want to focus on a task and need a reminder when their time is up.

<img width="570" alt="Screen Shot 2023-03-10 at 4 56 27 PM" src="https://user-images.githubusercontent.com/112274822/224435967-55ced4cf-0e13-47fe-87e8-07de56752227.png">

In addition to setting a specific amount of time, imerr also allows users to extend the timer if they need more time to complete their task. This can be done by typing a simple command in the terminal window where imerr is running. One of the benefits of using imerr is that it is lightweight and does not require a graphical user interface (GUI) like many other timer applications. This means that it can be used on servers or in other situations where a GUI is not available. Overall, imerr is a simple and effective tool for anyone who needs to track their time and wants to receive notifications when their timer is up. Its ease of use and customizable options make it a valuable tool for productivity and time management.

## Preparation
Building and installing a Rust application:

1. `rustup default stable`: This sets the default Rust toolchain to the stable version. Rustup is a toolchain manager for Rust, and this command ensures that you have the correct version of Rust installed.

2. `cargo build`: This command builds the application from the source code using the Cargo build system. Cargo is the official package manager and build tool for Rust, and it manages dependencies, compiles code, and builds executable binaries.

3. `cargo install --path .`: This command installs the application locally on your machine. The --path flag specifies the path to the Rust project directory, and the . indicates the current directory. This command builds and installs the application in one step.

4. `export PATH="${HOME}/.cargo/bin/:${PATH}"`: This command adds the directory where the application is installed (~/.cargo/bin) to your PATH environment variable. This ensures that you can run the application from anywhere in the terminal by typing its name.

## Usage
After installing timerr using the instructions you provided, you can use it to set a timer for a specific duration or time. Here's some examples:

1. `timerr 45 "Laundry is done"`: This command sets a timer for 45 minutes and sends a desktop notification with the title "Laundry is done" when the timer is up.

2. `timerr 15:45 "Meeting in 15 minutes"`: This command sets a timer for 3:45 PM and sends a desktop notification with the title "Meeting in 15 minutes" when the timer is up.

3. `timerr 15 Grab pizza from oven`: This command sets a timer for 15 minutes and sends a desktop notification with the title "Grab pizza from oven" when the timer is up. Note that in this case, the notification title does not need to be quoted.

It's important to note that timerr relies on a notification daemon to display the desktop notifications. A notification daemon is a program that runs in the background and displays notifications on the desktop. Before using timerr, make sure that a notification daemon is running on your system. If you're using a Linux desktop environment, there is likely a notification daemon installed by default. If not, you may need to install one manually.

## Enhancing timerr:
Here are some suggestions on how to implement the features you mentioned for timerr:

1. Support duration suffixes: It would be helpful to allow users to set the duration of a timer using suffixes like "s" for seconds, "m" for minutes, and "h" for hours. For example, a user could set a timer for 30 seconds with the command `timerr 30s "Task complete"`. Similarly, a timer for 1.5 hours could be set with the command `timerr 1.5h "Meeting over"`.

2. Support am/pm times: In addition to specifying times using the 24-hour clock, it would be useful to allow users to set timers using the am/pm format. For example, a user could set a timer for 3:30 PM with the command `timerr 3:30pm "Meeting starts in 30 minutes"`.

3. Optional body text, icon, & sound via CLI flags: Currently, timerr only allows users to specify the title of the desktop notification. It would be helpful to allow users to also specify the body text, icon, and sound of the notification using command-line flags. For example, a user could set a timer with a custom sound using the command `timerr 10 "Task complete" --sound my-sound.wav`.

4. Default icon & sound via config file: Finally, it would be useful to allow users to set default values for the icon and sound of the notification via a configuration file. This would allow users to customize the appearance and behavior of timerr without having to specify command-line flags every time they set a timer.

Implementing these features will make timerr more flexible and customizable for different use cases.

### Reference
https://github.com/GiorgiBeriashvili/cli-timer
https://github.com/regalk13/rust-timer
