# Navigating RStudio

*This lesson is partially derived from Software Carpentry teaching materials available under the [CC BY 4.0 license](https://creativecommons.org/licenses/by/4.0/legalcode):*

http://swcarpentry.github.io/r-novice-gapminder/

#### 1. Introduction to RStudio

R is a programming language for handling, analysing and visualizing data. It is freely downloadable and works on all major platforms, including Windows, macOS and Linux. At its core, R code is made of text-based commands that can be run from a command prompt and without a graphical user interface. R can also be run via an open-source interface such as RStudio (see [rstudio.com](http://www.rstudio.com)). RStudio provides a built in-editor and offers many advantages including ease of use, integration with version control and project management. 

During this workshop we will be using RStudio Server, which lets us access a remote instance of R via a web browser.

#### 2. Accessing RStudio Server on notebooks.csc.fi

To launch your own instance of R:

- Go to [notebooks.csc.fi](https://notebooks.csc.fi) and log in using the Haka authentication service. If you do not have a Haka account and password, please let us know!
- Find "R Data Analysis" in the dashboard and click on "Launch new".  
- Wait for the virtual machine to start and click on "Open in browser" once the link appears.
- Your browser will open a new window with login and password details. Press "Click to copy password & proceed".
- This will open a new tab where you can enter a username ("rstudio") and paste your password to open up a new RStudio session.

**Note:** each RStudio session on notebooks.csc.fi lasts for 10 hours, after which it is automatically erased. We will cover ways to save your code and data for later work during this workshop!

#### 3. Basic layout

When you first open RStudio, you will be greeted by three panels:

- The interactive R console (entire left)
- Environment / History (tabbed in upper right)
- Files / Plots / Packages / Help / Viewer (tabbed in lower right)

Your screen will look similar to this:

![](Images/01-rstudio.png?raw=true)

Once you open files, such as R scripts, an editor panel will also open in the top left.

![](Images/01-rstudio-script.png?raw=true)

#### 4. Executing code in RStudio

There are two main ways one can work within RStudio:

1. Test and play within the interactive R console
   - This works well when doing small tests
   - Quickly becomes laborious
2. Write using the script editor
   - Makes it possible to save your code for later (as an .R file)
   - Far easier to keep track of long segments of code

RStudio offers you great flexibility in running code from within the editor window. There are buttons, menu choices, and keyboard shortcuts. To run the current line, you can:

1. Click on the `Run` button above the editor panel, or
2. Select `Run Selected Lines` from the `Code` menu, or
3. Hit `Ctrl + Return` in Windows or Linux or `⌘ + Return` on OS X. 

If you have modified a block of code and wish to re-run it, you can either highlight it and run the code again (using one of the options above) or use the button `Re-run the previous region`. This will run the previous code block including the changes you have made.

#### 5. Projects in RStudio

Many data analysis projects might be organised like this:

![](Images/bad_layout.png?raw=true)

There are many reasons why we should *always* avoid this:

1. It is hard to tell which version of your data is the original
2. It gets really messy because it mixes files with various extensions together
3. It probably takes a lot of time to actually find things, and relate the correct figures to the exact code that has been used to generate it

A good project layout will ultimately make your life easier:

- It will help ensure the integrity of your data
- It makes it simpler to share your code with someone else (a lab mate, collaborator, or supervisor)
- It allows you to easily upload your code with your manuscript submission
- It makes it easier to pick the project back up after a break

**Hands-on: creating a self-contained RStudio project**

We’re going to create a new project in RStudio:

1. Click the “File” menu button, then “New Project”
2. Click “New Directory”
3. Click “New Project”
4. Type in the name of the directory to store your project, e.g. “RIntro”.
5. Click the “Create Project” button

Now when we start R in this project directory, or open this project with RStudio, all of our work on this project will be entirely self-contained in this directory.

Switching between projects can be done from the "File" menu ("Open Project").

##### Best practices for project organisation

Although there is no single best way to lay out a project, there are general principles to adhere to that will make project management easier:

- **Treat data as read-only**
  
  - This is probably the most important goal of setting up a project. Data are typically time-consuming and / or expensive to collect. Working with them interactively where they can be modified means you are never sure of where the data came from, or how they have been modified.

- **Separate raw and tidied data**
  
  - In many cases your data will be “messy”: it will need significant preprocessing to get into a format R (or any other programming language) will find useful. Storing these files in a separate folder, and creating a second “read-only” data folder to hold the “cleaned” data sets can prevent confusion between the two sets.

- **Treat the generated output as disposable**
  
  - Anything generated by your scripts should be treated as disposable: it should all be possible to regenerate from your scripts.

Some general recommendations for organising a project:

1. Keep all project files under the directory that was automatically created when you named the project.
2. Put text documents associated with the project in a directory called `doc` .
3. Put raw data and metadata in the `data` directory, and files generated during cleanup and analysis in the `results` directory.
4. Name all files to reflect their content or function.

We will cover topics including data import and export later during this workshop!
