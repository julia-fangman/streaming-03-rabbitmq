# streaming-03-rabbitmq
## Julia Fangman's Project 3
## Github Link: https://github.com/julia-fangman/streaming-03-rabbitmq 

> Get started with RabbitMQ, a message broker, that enables multiple processes to communicate reliably through an intermediary.

This project requires some free code - beyond that available in the Python Standard Library. To avoid messing up our local default Python installation, and any other Python projects we may have, we  create a local virtual environment to install and use these libraries.

Think of a virtual environment as a safe sandbox. 
We can install whatever we want in our sandbox, and it won't break other Python projects that may require different versions, etc. 

We use the built-in Python utility `venv` to create our virtual environment. 
There are other options, but this is simplest and most common. 
We create the environment as a subfolder of this repo named .venv to keep it away from our project code. 

## Prerequisites

1. Git
1. Python 3.7+ (3.11+ preferred)
1. VS Code Editor
1. VS Code Extension: Python (by Microsoft)
1. RabbitMQ Server installed and running locally

## Before You Begin (streaming-03-rabbitmq)

1. Fork this starter repo into your GitHub account.
1. Clone your repo down to your machine.
1. Explore your new project repo in VS Code on your local machine.

## Task 1. Create a Python Virtual Environment (called .venv)

We will create a local Python virtual environment to isolate our project's third-party dependencies from other projects.

1. Open a terminal window in VS Code.
1. Use the built-in Python utility venv to create a new virtual environment named `.venv` in the current directory.

python3 -m venv .venv 

Verify you get a new .venv directory in your project. 
We use .venv as the name to keep it away from our project files. 

## Task 2. Activate the Virtual Environment

In the same VS Code terminal window, activate the virtual environment.

- On MacOS, run: `source .venv/bin/activate`

Verify you see the virtual environment name (.venv) in your terminal prompt.

## Task 3. Install Dependencies into the Virtual Environment

To work with RabbitMQ, we need to install the pika library.
A library is a collection of code that we can use in our own code.
Learning to use free libraries that others have written to make our projects easier, faster, more reliable is a key skill for a developer.

We keep the list of third-party libraries needed in a file named requirements.txt.
Use the pip utility to install the libraries listed in requirements.txt into our active virtual environment. 

Make sure you can see the .venv name in your terminal prompt before running this command.

`python -m pip install -r requirements.txt`

## Task 4. Verify Setup

In your VS Code terminal window, run the following commands to help verify your setup.
These util files MAY be helpful to ensure you're setup correctly. 
You may have a different configuration and RabbitMQ may still work; the check looks in common places, but may not work for all installations. 
They are meant to be helpful, but are not required.

```shell
python util_about.py
python util_aboutenv.py
python util_aboutrabbit.py
pip list
```

Which creates util_about.txt, aboutenv.txt, aboutrabbit.txt :) 

## Task 5. Read

1. Read the [RabbitMQ Hello World! tutorial](https://www.rabbitmq.com/tutorials/tutorial-one-python.html)
1. Read the code and comments in our 2 project files: emit_message.py and listen_for_messages.py

Don't worry if it doesn't all make sense the first time. 
Approach it like a puzzle and see what you can figure out. 

## Task 6. Execute the Producer/Sender

1. Read v1_emit_message.py (and the tutorial)
1. Run the file. 

It will run, emit a message to the named RabbitMQ queue, and finish.
We can execute additional commands in the terminal as soon as it finishes. 

## Task 7. Execute the Consumer/Listener

1. Read v1_listen_for_messages.py (and the tutorial)
1. Run the file.


## Task 8. Open a New Terminal / Emit More Messages

1. Open a new terminal window.
1. Use this new window to run emit_message.py again.
1. Watch the listing terminal.
 
![Version 1 w/ 5 different messages:](Working%20V1.png)


## Task 9. Save Time & Effort: Don't Repeat Yourself

Did you notice you had to change the message in TWO places?

1. You update the actual message sent. 
1. You also update what is displayed to the user. 
1. Fix this by introducing a variable to hold the message. 
1. Use your variable when sending. 
1. Use the variable again when displaying to the user. 

Now, to send a new message, you'll only make ONE change.
Updating and improving code is called 'refactoring'. 
Use your skills to keep coding enjoyable. 

## Version 2

Now look at the second version of each file.
These include more graceful error handling,
and a consistent, reusable approach to building code.

Each of the version 2 programs include an error as well. 

1. Find the error and fix it. 
1. Compare the structure of the version 2 files. 
1. Modify the docstrings on all your files.
1. Include your name and the date.
1. Imports always go at the top, just after the file docstring.
1. Imports should be one per line - why?
1. Then, define your functions.
1. Functions are reusable logic blocks.
1. Everything the function needs comes in through the arguments.
1. A function may - or may not - return a value. 
1. When we open a connection, we should close the connection. 
1. Which of the 4 files will always close() the connection?
1. Search GitHub for if __name__ == "__main__":
1. How many hits did you get? 
1. Learn and understand this common Python idiom.

![Version 2 w/ Multiple Terminals](Multiple%20Terminals.png)


## Reference

- [RabbitMQ Tutorial - Hello, World!](https://www.rabbitmq.com/tutorials/tutorial-one-python.html)
- [Using Python environments in VS Code](https://code.visualstudio.com/docs/python/environments)
- [RabbitMQ Get Started](https://www.rabbitmq.com/#getstarted)

![Exploring the local virtual environment folder](./images/exploring_dot_venv.PNG)
