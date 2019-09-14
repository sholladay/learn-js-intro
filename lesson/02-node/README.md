# Lesson #2: Setting up Node.js

Throughout this course, we will be writing JavaScript code and then using Node.js to run the code that we saved. Node is a command line program, similar to the commands you learned about in the previous lesson. However, unlike those commands, Node is not installed on your computer yet. Let's go get it!

Now is also a good time to install some of the other tools mentioned below, however Node is the only requirement to proceed.

## Install Homebrew

Homebrew is a package manager, which is useful to have because it can install, update, and remove other software. It helps you keep track of the apps and tools you have installed and makes it easy to search for and find other software that you might need, all from your terminal.

For the most up-to-date instructions on installing Homebrew, see their [official documentation](https://brew.sh/). Or just run the command below in your terminal.

*__Tip:__ Strictly speaking, a package manager is not required to install Node.js or any other program, nor is it necessary to complete any of the lessons in this course. However, they will make your life easier. Homebrew is a good choice, but other package managers could be used instead.*

```console
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## Install Visual Studio Code

Visual Studio Code is a code editor, which we can use to write and save our code. A code editor is very similar to a word processor, such as Microsoft Word. In fact, VS Code is also made by Microsoft. The difference is simply that a code editor is optimized for writing computer code. Unlike a word processor, code editors save your work in plain text, meaning that the saved file does not include any information about the font family, font size, or text color. You can customize the look of the code in your editor, however those changes are only be visible to you. This allows code files to be small and easily comparable across computers, regardless of which software is used to create or view them.

Use Homebrew to install Visual Studio Code by running the command below in your terminal.

*__Tip:__ You can use any code editor or plain text editor you want. VS Code uses a graphical interface like many of the apps you are probably familiar with. There are also command line code editors, such as Vim, however these are typically considered a bit more advanced. Using a word processor is not recommended.*

```console
$ brew install visual-studio-code
```

## Install Node.js

Node.js is a runtime environment for JavaScript, which we will use to run the JavaScript programs that you write in this course.

Use Homebrew to install Node by running the command below in your terminal.

```console
$ brew install node
```

## Next up

When you are done with this lesson, proceed to [Lesson #3: JavaScript Overview](../03-overview/README.md).
