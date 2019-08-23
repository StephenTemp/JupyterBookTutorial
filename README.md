# JupyterBookTutorial
A short, mildly comprehensive (and hopefully useful) guide on creating and displaying jupyter books

## Installing Jupyter-Book
Run the following through your command line:
![Install](/images/install.png)

## Creating and Building your Book
You can generate a new jupyter-book by running:
![Create](/images/create.png)  
You may also generate a standard example book to build off of by running:

![Demo](/images/demo.png)   
[Warning: the demo book has trouble interacting with the Git Pages service and adding onto it risks build failure; it's better to start from scratch]
#### Adding to New Books
Creating a new book from scratch should produce a folder with the following contents:

![NewBook](/images/testbook.png)  

The **content** folder will be the hub for the main sections of your book. If you add a section, however, be sure to update the table of contents either manually (it resides in the **data** folder) or automatically by running:

![Toc](/images/toc.png)  

To specify the order in which the sections should rank, naming the folders by the order in which they should list will do the job ("01", "02", "03"...).
#### Building/Uploading Your Book
Once your table of contents is generated and your content is well structured, you should be well-suited to _build_ your book. Building essentially allows GitHub and other services to understand and read your jupyter-book. Once you're ready, run the following:

![Build](/images/build.png)  

A new '_ build' folder should generate. Upload your book's contents to GitHub (see the section below) and move into the **Settings** tab to configure your "Git Pages" settings. You should find this panel towards the bottom:

![Pages](/images/pages.png)  

Choose "master" from the **Source** drop-down menu. Assuming there are no build failures, you should be provided a link to your new book in roughly a couple minutes or so.

### Using GitHub
GitHub is a service that allows multiple programmers to edit files in an efficient and collaborative manner. These projects are called _repositories_. There are multiple ways to use GitHub's services including your command line or the desktop GitHub app (which I **strongly** recommend for working with Git Pages). You can find the downloads/instructions for each **here**:
- [Create an Account (Required)](https://github.com)
- [Using the Command Line (Required)](https://help.github.com/en/articles/set-up-git)
- [Using GitHub Desktop (Recommended)](https://desktop.github.com/)

Now that your account is up and running, it's time to create a new repository. You may now use either GitHub Desktop or the command line. If you've chosen to use the command line, here's a helpful cheat sheet to aid you in following along: [Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)  
1. If you're using the command line, navigate to your Jupyter-Book and enter it. Initialize this space as a new GitHub repository with the **git init** command. Once complete, run **git add -A** to add all the files in your book to the following _commit_. Run the commit (present on the cheat sheet) and connect it to GitHub using these instructions: [GitHubTutorial](https://kbroman.org/github_tutorial/pages/init.html).
2. If you're using the desktop app, simply navigate to **add** and select **Create New Repository** as shown below:

![Desktop Repo](/images/deskrep.png)  

Fill in the title (keep it the same as your Jupyter-Book) and create the new repository. Next, select **Publish Repository** from the top of the screen:

![Publish](/images/publish.png)  

Navigate back to your repositories and you should find your Jupyter-Book with all its contents. Follow the above instructions to learn how to utilize **Git Pages** to display your hard work.

## Editing an Existing Book
When adding content to a section, it's important to keep in mind the overall structure of jupyter-books. For example, to add a notebook page "Query" to an existing heading, navigate to the **content** folder (not the build). Say it has the following sections:

![Pages](/images/content.png)  
These folders correspond to the ordered sections within the **toc.yaml** file (table of contents):

![Pages](/images/tocex1.png)  

This section of the **toc.yaml** maps to folder _02_ from the **content** folder. The top _url_ field designates the path Jupyter-Book should send a user when clicking the main heading (in this case, the file "llc90plottingexamples"). Adding a notebook/file under the heading is as easy as dropping it into the heading folder and adding the _title_ and _url_ fields to match. Adding a "Query" page for instance would require the following edit to the above **toc.yaml** file:

![Pages](/images/tocex2.png)  

[Note: You can also accomplish this by generating a **toc.yaml** from the code above, but manually describing the change is recommended]. After you're finished, be sure to rebuild your book (using the steps listed above) and push the change to GitHub. If the book builds without error (and you've specified the path correctly), it should be listed under your heading:

![Pages](/images/bookheadex.png)  
