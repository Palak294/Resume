# Static Website on a Forge

Welcome! If you have been exploring the concepts in Andrew Etter's *Modern Technical Writing* and are learning the basics of Markdown, you might be interested in seeing how those principles are applied to build real-world documentation and websites here at Foomatic.

This repository contains the source code for my professional resume. Instead of writing it in a traditional word processor, I used a **Static Site Generator** (Pelican) and a **Forge** (GitHub) to publish it. 

As Etter explains in his book, keeping documentation in plain text (Markdown) and separating the content from its visual presentation allows us to write faster, easily track changes, and treat our documentation exactly like software code.

If you have a basic understanding of navigating the command line, here is how you can download this code and build this website on your own Windows computer!

## Prerequisites
Before you begin, you need to have two pieces of software installed on your Windows machine:
* **Python 3:** Needed to run the Pelican generator.
* **Git:** A version control system needed to download the files. 

## Instructions

### Phase 1: Downloading the Repository
Since you are familiar with basic command-line operations, we will use Git to copy these files from the GitHub forge to your computer.

1. **Open** your Windows Command Prompt.
2. **Navigate** to the folder where you want to save the project using the `cd` command. 
   *(Note: For example, type `cd Documents`)*.
3. **Clone** the repository by typing the following command and pressing Enter:
   `git clone [Your Repository URL]`
   *Result: Git will download a folder named "Resume" containing all the files.*
4. **Change** your directory to enter the new project folder:
   `cd Resume`

### Phase 2: Installing the Static Site Generator
Now we need to install Pelican. Pelican is a Python-based tool that will read my Markdown text and automatically wrap it in HTML and CSS to make it look like a real website.

1. **Install** Pelican and its Markdown support tool by running this command:
   `python -m pip install "pelican[markdown]"`
   *Result: Your computer will download the necessary Python packages.*

### Phase 3: Building and Viewing the Website
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

## Phase 4: Saving and Publishing Your Changes
Whenever you make changes to your Markdown files and regenerate your HTML, you need to save those updates and send them to the forge so your live website updates.

1. **Stage** your updated files by running this command:
   `git add .`
   *Result: Git prepares all your new and modified files to be saved.*
2. **Commit** (save) your snapshot by running this command:
   `git commit -m "Updated resume content"`
   *Note: You can change the message inside the quotation marks to describe what you changed.*
3. **Push** your saved snapshot to GitHub by running this command:
   `git push`
   *Result: GitHub will receive your files and automatically update your live website within a few minutes.*

## Further Resources
If you would like to dive deeper into the tools and concepts used to build this project, here are some helpful links to get you started:

* **[The Markdown Guide: Basic Syntax](https://www.markdownguide.org/basic-syntax/):** An excellent, beginner-friendly tutorial on Markdown formatting that goes beyond the basics to help you write documentation effortlessly. 
* **[Official Pelican Documentation](https://docs.getpelican.com/):** The complete guide to the static site generator powering this resume. It covers everything from basic content creation to advanced configuration.
* **[GitHub Pages Overview](https://pages.github.com/):** A straightforward explanation of how the GitHub forge takes plain text files and automatically broadcasts them as a live website.
* **[Official Git Documentation](https://git-scm.com/doc):** The definitive, official guide and reference manual for Git, covering everything from installing the software to taking your first repository snapshots.

## FAQ

1. **Why is Markdown better than writing raw HTML?**  
HTML is cluttered with complex and easily broken formatting tags while,Markdown uses simple, highly readable symbols. Following Andrew Etter's principles, it separates content from presentation. You can focus purely on writing the information in plain text, while a tool like Pelican automatically handles the design and converts it into HTML later.

2. **I changed the Markdown version of my resume, so why don't I see the changes when I refresh the website in my browser?**  
In order to save the changes completely to your website, you need to save your changes and then make sure you add and commit them to your GitHub.

## Credits & Licensing
* **Theme:** This site uses the third-party [Flex](https://github.com/alexandrevicenzi/Flex) theme created by Alexandre Vicenzi, utilized under the MIT License.
* **Lara De Leon:** Suggested changes to my README file
* **Eunice Taborlupa:** Suggested changes to my README file
* **Google's Gemini AI:** Troubleshooting and debugging assistance for Pelican setup errors, GitHub deployment issues, and theme configuration 