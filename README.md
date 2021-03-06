# krunner-symbols

A little krunner plugin (Plasma 5) to retrieve unicode symbols, or any other string, based on a corresponding keyword.

![Demonstration](https://raw.githubusercontent.com/domschrei/krunner-symbols/master/img/demonstration1.png)

E.g. you can type `lambda` and krunner will yield the proper unicode symbol λ. It can be used to quickly get a symbol when writing some text, or to retrieve often-needed texts (or links, or emotes ...) by typing a certain abbreviation.

![Demonstration](https://raw.githubusercontent.com/domschrei/krunner-symbols/master/img/demonstration2.png)
![Demonstration](https://raw.githubusercontent.com/domschrei/krunner-symbols/master/img/demonstration3.png)

Which keywords and symbols are supported depends on an open-ended text file (see *Configuration*).

## Why?

krunner is a great tool because it's always accessible, very fast, and really unintrusive, as it temporarily gets focused when called, but then returns the focus to the previously focused view when finished. Because of this, a quick krunner query can be perfectly integrated into a user's workflow, adding efficiency and convenience. This little tool is meant to support this idea of usage.

If you are interested in the project, have any recommendations or suggestions, feel free to contact me or post an issue. As I did not have any experience with Plasma development before, I am happy to hear about how I can improve the code and/or the build process.

## Installation

You can execute the install script (inside the `krunner-symbols` directory, execute the command `bash install.sh`) in order to install the plugin. However, please note that this is in an early stage of development, and errors might occur depending on your setup. In case of doubt, rather manually execute the single commands inside the script and watch the output.

## Configuration

Instead of editing the primary source `~/.config/krunner-symbols`, you can create a second file `~/.config/krunner-symbols-custom` where you can redefine existing definitions or create new ones, thus configuring the recognized symbols without changing the original file. That way, if you update or reinstall this plugin, you won't lose your custom definitions. Keep in mind that you will have to restart krunner (`kquitapp krunner && krunner`) for configuration changes to take effect.

The syntax is easy. Just create lines like this:
```
Keyword=Output
```
, where `Keyword` is what you have to type and `Output` is what you get when typing it. They can be entire sentences, or just single symbols. To insert a comment, you can do this: 

```
# Lalala the program can't hear me
```

Blank lines are okay, too.

TL;DR: Just look at the file `krunner-symbols` and you will get the idea.

## Usage

Open krunner and enter the keyword for the symbol you want to copy. Click on the appearing entry tagged with *Symbols* or press Enter while focusing it. krunner disappears and the result has been copied to your clipboard. With `Ctrl+V`, you can paste it anywhere.

You can also use the plugin as some more general form of alias-resolver (i.e. entering some keyword in order to get the corresponding text) by editing the configuration file appropriately.
