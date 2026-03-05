# Assignment 2 Website

Hi Marvin! I noticed you have been reading Andrew Etter's *Modern Technical Writing* in the lunchroom. Since you have been learning Markdown, I thought you might be interested in seeing how we use it to build documentation and websites here at Foomatic.

This repository contains the source code for my professional resume. Instead of writing it in a word processor, I used a **Static Site Generator** (Pelican) and a **Forge** (GitHub) to publish it. 

As Etter explains in his book, keeping documentation in plain text (Markdown) and separating the content from the formatting allows us to write faster and treat our documentation exactly like software code.

Here is how you can download my code and build this website on your own Windows computer!

## Prerequisites
Before you begin, you need to have two pieces of software installed on your Windows machine:
* **Python 3:** Needed to run the Pelican generator.
* **Git:** A version control system needed to download the files. 

## Phase 1: Downloading the Repository
Since you are familiar with basic command-line operations, we will use Git to copy these files from the GitHub forge to your computer.

1. **Open** your Windows Command Prompt.
2. **Navigate** to the folder where you want to save the project using the `cd` command. 
   *(Note: For example, type `cd Documents`)*.
3. **Clone** the repository by typing the following command and pressing Enter:
   `git clone https://github.com/Palak294/Resume.git`
   *Result: Git will download a folder named "Resume" containing all the files.*
4. **Change** your directory to enter the new project folder:
   `cd Resume`

## Phase 2: Installing the Static Site Generator
Now we need to install Pelican. Pelican is a Python-based tool that will read my Markdown text and automatically wrap it in HTML and CSS to make it look like a real website.

1. **Install** Pelican and its Markdown support tool by running this command:
   `python -m pip install "pelican[markdown]"`
   *Result: Your computer will download the necessary Python packages.*

## Phase 3: Building and Viewing the Website
With Pelican installed, we can now generate the website and view it locally on your computer before it ever goes on the live internet.

1. **Generate** the HTML website by running this command:
   `pelican content`
   *Result: Pelican will process the Markdown files and create the website pages.*
2. **Start** a local preview server by running this command:
   `pelican --listen`
   *Result: The terminal will say "Serving site at: http://127.0.0.1:8000".*
3. **Open** your favorite web browser.
4. **Type** `http://127.0.0.1:8000` into the address bar and press Enter.

You should now see the fully styled resume! When you are done looking around, you can go back to your Command Prompt and press **Ctrl + C** to turn off the local server.

## Credits & Licensing
* **Theme:** This site uses the third-party [Flex](https://github.com/alexandrevicenzi/Flex) theme created by Alexandre Vicenzi, utilized under the MIT License.