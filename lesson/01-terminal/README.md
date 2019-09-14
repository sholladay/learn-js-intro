# Lesson #1: Using a Terminal

Before we dive into JavaScript, we need to talk about an alternative way to interact with your computer that you may not be familiar with. A [terminal](https://en.wikipedia.org/wiki/Terminal_emulator) is a program that provides a textual interface to the computer, allowing you to type commands to tell your computer what to do, instead of pointing a mouse and clicking on buttons.

In the early days of computing, a terminal was the only way to use a computer. Graphical interfaces came later. Believe it or not, a terminal is still the most efficient way to use a computer. Once you learn to use a terminal, you will be able to work much faster than before. Additionally, because it takes time and effort to build a graphical interface, some programs are *only* available from a terminal. Thus, learning to use a terminal will give you access to new capabilities that you haven't had before. One such program is Node.js, which you will use to run the JavaScript code that you write in future lessons.

Learning and using a terminal is relatively simple in concept. You type a command, hit <kbd>Enter</kbd>, and wait for the computer to perform whatever task you told it to do. Usually, there will be some text output when the task is complete. Then you can type another command for the next task and so on and so forth.

The hard part about using a terminal is knowing which commands you can type, remembering them, and understanding how to combine them to achieve the behavior that you want. This will become easier with practice. You can also read the manual pages for specific commands to read about how they work, by running `man x`, where `x` is the name of the command you want to read about.

## Open a terminal

On macOS, you can open a terminal like this:

1. Press <kbd>Command</kbd> + <kbd>Space</kbd> to open Spotlight search
2. Type "Terminal"
3. Press <kbd>Enter</kbd>

A terminal window should open, with a mostly blank white screen aside from a few bits of text, and you should be able to type. We call this typing area the "command line", because that is where you will type commands to tell your computer what to do.

## Meet the shell

The shell is a program that interprets the commands you type into the command line, in order to carry out your instructions. The shell began running as soon as you opened the terminal and it is waiting for you to tell it what to do.

*__Tip:__ If you find the distinction between "terminal", "shell" and "command line" to be confusing, don't worry. While they are technically separate concepts, these terms are often used interchangeably in casual conversation. For now, just remember that this is where you type commands.*

Let's make the shell do something fun!

Try running the command below. Note that you should not type the leading dollar sign and space `$ `, that is only there by convention, to indicate that we are talking about running this on the command line (as opposed to other places we can run code). Simply type the command and then press <kbd>Enter</kbd>. You will know the task is complete when a new dollar sign appears, at which point you can type another command.

```console
$ whoami
```

If it worked, you should see your username in your terminal. It is always fun to know who we are, right?

Okay, what else can we do? Run the command below to find out what date and time it is!

```console
$ date
```

On macOS, there is a very cool command called `say` that causes the computer to speak outloud anything you give to it. Let's try it! In the example below, `"Hello, world!"` is known as an _argument_, which is simply a piece of data that we need to give to `say` in order for `say` to do something useful.

*__Tip:__ We put the argument in quotes to ensure it is treated as a single argument containing multiple words, rather than multiple arguments containing single words. That distinction does not matter in this case because `say` is smart enough to handle it correctly either way, but some programs would behave incorrectly if we didn't put the argument in quotes. When in doubt, use quotes, it is a good practice.*

```console
$ say "Hello, world!"
```

Now let's get more fancy. We can combine the tools we learned about above to make the computer say our username outloud without having to type it by hand. There are many ways to combine commands on the command line. In the example below, we are using the `|` pipe operator, which takes the output of the command on the left and sends it to the command on the right as input.

```console
$ whoami | say
```

Using what you learned above, see if you can figure out how to get the computer to say the date and time outloud.

## Paths and directories

When using a terminal, it is important to know where you are, just as it is in real life. When you run a command, it is executed in the context of the _current working directory_, which is your current location within the directory tree of your computer's hard drive. By default, when you open a terminal, your working directory is set to your home directory. That is, it's set to the directory that contains the files that belong to you.

Conceptually, the files on your computer are all organized into directories. Those directories can be, in turn, nested inside of other directories, for organizational purposes. If you follow this chain of directories, eventually you will find the _root directory_, which is where everything is ultimately stored. We call this hierarchy a tree because that's how it looks visually, if you were to draw a diagram of it.

Your computer may have other user accounts on it besides your own, in which case those users' home directories would be siblings of your home directory. The parent of your home directory is the directory that contains all of the user directories, and the parent above that (at least on macOS) is the root directory.

You can find out where you are within the directory tree by running the command below.

```console
$ pwd
```

If it worked, you should see the full path of the current working directory. It will look like `/a/b/c`, except to the right of each slash will be an actual directory name. The path is like a breadcrumb trail, showing you the path from the root directory to your current location. The root directory is simply `/`, anything after that is a directory that is nested somewhere within the tree and each directory is separated by a `/`.

## Next up

When you are done with this lesson, proceed to [Lesson #2: Setting up Node.js](../02-node/README.md).
