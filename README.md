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

The **content** folder will be the main hub for the main sections of your book. If you add a section, however, be sure to update the table of contents either manually (it resides in the **data** folder) or automatically by running:

![Toc](/images/toc.png)  

To specify the order in which the sections should rank, naming the folders by the order in which they should list will do the job ("01", "02", "03"...).
#### Building/Uploading Your Book
Once your table of contents is generated and your content is well structured, you should be well-suited to _build_ your book. Building essentially allows GitHub and other services to understand and read your jupyter-book. Once you're ready, run the following:

![Build](/images/build.png)  

A new '_ build' folder should generate. Upload your book's contents to GitHub and move into the **Settings** tab to configure your "Git Pages" settings. You should find this panel towards the bottom:

![Pages](/images/pages.png)  

Choose "master" from the **Source** drop-down menu. Assuming there are no build failures, you should be provided a link to your new book in roughly a couple minutes or so.

## Editing an Existing Book
When adding content to a section,
