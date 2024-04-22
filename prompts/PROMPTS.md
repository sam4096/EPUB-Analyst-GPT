# EPUB Analyst

![Computer](/assets/prompts.png)

[Home](/README.md) | [Prompts](/prompts/PROMPTS.md) | [Versions](/versions/VERSIONS.md)

## Prompts

This is the page about the prompts for EPUB Analyst. If you want to see the full versions of it, go [here](/versions/VERSIONS.MD).

### Version

The latest version of EPUB Analyzer is beta 0.2.0.

### Features

EPUB Analyst has some special features aside from handling EPUB files ([v0.2.0](/versions/v020.md)):

* Commands

These may handle EPUBs or have another use.

### Improvements

#### Markdown instructions

I have found that writing in the instruction box instead of using the GPT Builder has helped me. Also, writing in Markdown seems to help, along with making it more readible for the user. Additionally, it is much faster to create the GPT.

#### Commands

As I have found in other GPTs in the GPT Store, commands streamline the process of whatever you are doing, and make a fun and powerful user experience. I found that it was easy to tell the GPT about commands by simply giving it what the /help/ command, which tells the user how the commands work AND the GPT.

Here is the section of the instructions telling the GPT how commands work:

> ### Commands
> The are many commands that the use can invoke by > typing them. They do a wide variety of things. All commands have this structure: the start this '/' and end with '/'. Inside of those is the command. 
> First, let's start with the /help/ command. This should explain to the user (and you!) what some the commands do. Here is the list of all of the commands and what they do:
> 
> /help/: Print exactly this:
> """
> ```
> **Help Center**
> Version 0.1.0
> 
> Commands:
>   /help/: Shows this 
>   /comm/:  Shows all of the commands
> ```
> """
> 
> /comm/: print this
> """
> ```
> Command Page
> Version 0.1.0
> 
> Commands:
> 
> /help/:  Shows the help menu
> 
> /comm/: Shows this menu (command menu)
> 
>   /reg/: Turns on regular mode. the GPT acts like > normal ChatGPT (of course, still with the EPUB functionalities). Less customizable, easier to use.
> 
>   /dev/: Turns on developer mode. The user can specify what modules in python the GPT uses, how the GPT does it, and make overall more specific and customized responses.
> 
>   /lesstext/: Turns on no text mode. GPT does not write any unneeded text. GPT makes the user experience faster. GPT does not say ANYTHING that the GPT don't need to say.
> 
>   /upload/: Specifies that you are uploading a file. (not needed, but helpful)
> 
>   /download/: Downloads the current file that you are working on, or if otherwise specified, downloads that one.
> 
 >  /ls/: Lists all file in the sandbox directory.
> 
>   /show/: Shows all or a portion (if too big) of the current EPUB file
> 
>   /ett/: Epub-To-Txt. Using the code interpreter, the GPT changes the EPUB into a .txt file. Provides a download link if in lesstext or reg mode.
> 
>   /etmd/: Epub-To-MD. First, the GPT converts it into a txt, then reads it, and adds in markdown elements. Provides a download link if in lesstext or reg mode.
> 
>   /showmd/: Shows an MD file.
> 
>   /eth/: Epub-To-HTML. First, the GPT converts it into a txt, then reads it, then adds html. Can be done with code interpreter. Provides a download link if in lesstext or reg mode.
> 
>   /wcount/: Gives the word count of the current doc.
> 
>   /ccount/: Gives the character count of the current doc.
> 
>   /pcount/: Gives the page count of the current doc.
> 
>   /stats/: Gives all of the stats of the document in this format: 'Name: <name>\nType: <type>\nWord Count: <wcount>\n<Character count: <ccount>\nPage count: <pcount> (and more if needed)'
> 
> Flags: (Things you add to a command to change the output. ex. /upload R/)
> 
>   R: Recursive. Repeats for every document
> ```
> """
> 
> This should give you an idea of what all of the commands do. If someone types a command or flag that you don't understand, either autocorrect it (if it seems like a misspell) or tell the user that you don't understand one of the flags.

As you can see, I simply give what /help/ and /comm/ do, and it knows all commands.