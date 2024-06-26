# PyTermUtils


**PyTermUtils** is a Python library that allows you to easily print colored text to the console/terminal. It provides a simple way to enhance the visual appeal of terminal output by using different colors and styles.

## Features


- Print text in various colors
- Apply different text styles (bold, underline, etc.)
- Easy-to-use Package

## Installation

You can install console via pip:

```bash

pip install PyTermUtils

```

## Usage

Here are some examples of how to use console package in your project:

### Basic Usage

```python

from PyTermUtils import *

# Print text in bright red and Highlight in bright green (16 colors)
Console.Print16C("Bright Red", ConsoleColor.Bright_Red, 
                 ConsoleColor.Bright_Green, resetmode=ResetMode.ResetAll)

# Print text in Magenta and bold (256 colors)
Console.Print256C("Magenta", 90, textmode=TextMode.Bold)

# Print text in Magenta and Italic (rgb colors = 1,67,77,216)
Console.Printrgb("Red", (210, 0, 0), textmode=TextMode.Italic)

```

## Available Colors

>[!NOTE]
> Forground color -> Text color
>
> Background color -> Highlight color

### 4 bits color (16 colors)

Sure! Here is a table for the 16 ANSI colors, which are often used in terminal applications for text coloring.


| Color Name     | fg code | bg code |
|----------------|---------|---------|
| Black          | 30      | 40      |
| Red            | 31      | 41      |
| Green          | 32      | 42      |
| Yellow         | 33      | 43      |
| Blue           | 34      | 44      |
| Magenta        | 35      | 45      |
| Cyan           | 36      | 46      |
| White          | 37      | 47      |
| Bright Black   | 90      | 100     |
| Bright Red     | 91      | 101     |
| Bright Green   | 92      | 102     |
| Bright Yellow  | 93      | 103     |
| Bright Blue    | 94      | 104     |
| Bright Magenta | 95      | 105     |
| Bright Cyan    | 96      | 106     |
| Bright White   | 97      | 107     |

To use these colors in a terminal, you use ANSI escape codes. The format for these codes is:
```
\e[<code>m or \033[<code>m
```

<img height="350" src="https://github.com/amitkr000/PyTermUtils/blob/master/res/4bit.png"/>

[Click to see more about it](https://en.wikipedia.org/wiki/ANSI_escape_code#3-bit_and_4-bit:~:text=The%20chart%20below%20shows%20a%20few%20examples%20of%20how%20VGA%20standard%20and%20modern%20terminal%20emulators%20translate%20the%204%2Dbit%20color%20codes%20into%2024%2Dbit%20color%20codes.)

### 8 bits color (256 colors)

To use 8-bit colors in a terminal, the format of the escape code is:
```
\e[38;5;<color>m for foreground colors
\e[48;5;<color>m for background colors
```


![16 bits colors img](https://user-images.githubusercontent.com/995050/47952855-ecb12480-df75-11e8-89d4-ac26c50e80b9.png)

### 24 bits color (True color) (8 bits each R-G-B)

24-bit color, also known as true color, allows for a much wider range of colors than 256-color ANSI. It uses 8 bits each for red, green, and blue components, allowing for 16,777,216 possible colors. This is particularly useful for applications requiring high color fidelity.

ANSI Code for 24-Bit Color
To use 24-bit color in ANSI, you can use the following format:

```
Foreground Color: \033[38;2;R;G;Bm
Background Color: \033[48;2;R;G;Bm
```

Where R, G, and B are the red, green, and blue color values (0-255).


> [!NOTE]
> All three(3) color mode of print have both foreground and background color.



## Available Attributes

The following text styles are supported:

- Bold
- Dim
- Italic
- Underline
- Blinking
- Reverse
- Hidden
- Strikethrough

### Example

Here is a more comprehensive example demonstrating the use of different colors and styles:


## Contributing

Contributions are welcome! Please open an issue or submit a pull request on GitHub.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

If you have any questions or suggestions, feel free to open an issue on GitHub.

## References

- [https://en.wikipedia.org/wiki/ANSI_escape_code#Fs_Escape_sequences]()
- [https://gist.github.com/fnky/458719343aabd01cfb17a3a4f7296797]()
- [https://www.lihaoyi.com/post/BuildyourownCommandLinewithANSIescapecodes.html]()
---
