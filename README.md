```markdown
# WPM Counter: A C-Based Typing Speed Test

![Language](https://img.shields.io/badge/Language-C-A8B9CC?style=for-the-badge&logo=c)

A simple but effective console application written entirely in C that tests your typing speed in Words Per Minute (WPM). It calculates your WPM, accuracy, and time taken based on your performance on a randomly selected paragraph.

## Demo

Here is a quick demo of the application flow:

```

select level(easy/med/hard): med

press any key to start the test\!

your timer has started...

enter the paragraph mentioned below:

The dog chased the ball across the yard while the kids watched.The dog was fast and energetic, enjoying the game.
The dog chased the ball across the yard while the kids watched.The dog was fast and energetic, enjoying the game.

YOUR RESULT:
WPM: 42
Time taken: 20.00 seconds
accuracy: 100.00%

You want to test again?(yes/no): no
Thanks for joining :)

````

## 🚀 Features

* **Three Difficulty Levels:** Choose from `easy`, `med` (medium), or `hard` difficulty.
* **Random Paragraphs:** Each level has a bank of 10 unique paragraphs to ensure a different test every time.
* **Accurate WPM Calculation:** Calculates your Words Per Minute based on correctly typed words.
* **Performance Metrics:** Displays your total time taken (in seconds) and your typing accuracy (as a percentage).
* **Replayable:** Instantly test yourself again with a simple "yes" prompt.

## 🛠️ How It Works

1.  **Level Selection:** The user selects a difficulty level.
2.  **Paragraph Generation:** The program randomly selects a string from the corresponding array (`easy_paragraphs`, `medium_paragraphs`, or `hard_paragraphs`).
3.  **Timer:** The test starts a timer as soon as the user presses a key. The timer stops when the user hits "Enter".
4.  **Input:** The user's typed input is read as a single string.
5.  **Comparison:**
    * The program tokenizes (splits by space) both the original paragraph and the user's input.
    * It compares each word to calculate the total number of correct words.
    * It compares each character to calculate a percentage for accuracy.
6.  **Results:** The program uses the correct word count and the total time elapsed to calculate and display the final WPM and other stats.

## 🔧 Technologies Used

* **C**
* **Standard Libraries:**
    * `stdio.h` (Standard Input/Output)
    * `stdlib.h` (Standard Library)
    * `string.h` (For `strcmp`, `strlen`, `strtok`, `strdup`)
    * `time.h` (For timing the user with `time()`, `difftime()`)
    * `conio.h` (For `getch()` - specific to Windows compilers)

## ⚙️ How to Compile and Run

This project uses the `conio.h` library, which is specific to Windows. It can be compiled using a compiler like `gcc` (via MinGW) or the Visual Studio C compiler (`cl`).

**Using `gcc` (on Windows):**

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/dhruv-jani-0808/WPM-counter.git](https://github.com/dhruv-jani-0808/WPM-counter.git)
    cd WPM-counter
    ```

2.  **Compile the program** (assuming your file is named `main.c`):
    ```sh
    gcc main.c -o wpm_test.exe
    ```

3.  **Run the executable:**
    ```sh
    ./wpm_test.exe
    ```

> **Note:** This code will not compile on Linux or macOS without modifications (i.e., removing `conio.h` and finding an alternative for `getch()`).
````
