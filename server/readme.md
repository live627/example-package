SMF Server Reference
====================

This documentation, intended for people who wish to create a package server, is only a quick run down of package lists. More thorough and advanced information can always be found on Simple Machines' [mod site documentation pages](http://mods.simplemachines.org/docs/). It should also be noted that sometimes, it's better to put your packages on the mod site.  

For more information, you can always post on [the forum](http://www.simplemachines.org/community/index.php) asking questions, exchanging ideas and comments, or just plain bragging about how much better your package server is than anyone else's.

What's available in this kit?
-----------------------------

You should notice a few files that came with this readme. They are examples to help give you a better understanding of how to create package lists. They are as follows:

    packages.xml

A simple example of a package listing, to get started with.

    packages\_advanced.xml

A more advanced example of a package listing, using some more powerful features.

    readme.html

This file, describing the use of the above files and what you can do with them.

All of these files, with the exception of the one you are currently viewing, are best viewed and edited with the text editor of your choice. If you can, try to read through them all and get a feel for what they are doing.

Creating a package list
-----------------------

To allow people to download packages from your server, you need a package list. This is a listing of packages on your server, with information about them.  
  
For the most basic use, you'll need a list title, and some packages to offer ;). Assuming you have that, take a look at packages.xml. You'll see a section for the package list's title, like so:  

      <list-title>My Package Server</list-title>

In your package server list, you'll want to use a different title. For example, you might use Mike's Mods - this is the title of this package listing. Next, you have 'sections', which are usually groupings of types of packages, or versions. One example would be to have a section for New Features, another for Themes, another for Odds and Ends. For the purposes of this tutorial, let's just keep it to one section.  
  
Each section is enclosed in a <section> element. Inside the section should be one title element. After that, you can have one or more modification, language, theme, avatar-pack, or smiley-set (there are a few others.) Let's assume you have a modification package. For it, you might have the following data:  

```
<!-- Remember, these have to be the same as those in the package itself! -->  
<id>username:testing123</id>  
<name>Testing - 123!</name>  
<version>1.0</version>  
  
<!-- Where is the file itself? (must be relative to the current URL for security reasons!) -->  
<filename>testing123\_1-0.tar.gz</filename>  
  
<!-- A description for this mod! (required) The CDATA makes it so you can type html in here. -->  
<description><!\[CDATA\[  
      This is a really <b>awesome</b> modification ;).  
\]\]></description>
```

The id, name, and version here (for modifications) **must** be the same as the mod itself. By the way, for upgrade purposes, you should keep the same id for different versions of the same mod. As for the filename, it may include a path, but the actual filename part will be used to save the package - so try to use something unique/descriptive. Remember, also, that the description is required.  
  
Once you have the package list file sorted out, you need to actually put it somewhere. Read on!

Putting the packages and list up
--------------------------------

Now that you have your package list set up, you should upload it somewhere. A good place is your website ;). You can put them anywhere, for example mine should be at [http://www.unknownbrackets.com/smf](http://www.unknownbrackets.com/smf/).  
  
It's also a good idea to put an index.php in that directory, just in case people are using a safe mode server. If they are, they will not be able to download packages directly, and will be sent to your url/index.php?package-list&language=blah&ref=their forum  
  
It's important to note that the packages should be under the same directory as the package list, or in a directory inside that directory. Don't put them in a different directory. (this means, don't put the list in /list and the packages in /packages.)

Accessing your server
---------------------

Now that you have all your files ready, you want to be able to access it, don't you? More importantly... you want other people to be able to access it!  
  
To access it, go to your package manager. Inside the package manager, click [\[ Download New Packages \]](javascript:void(0);), and look under the Add server section. Under that, type your package server's name and URL - for example, _\[Unknown\]'s Packages_ and [http://www.unknownbrackets.com/smf](http://www.unknownbrackets.com/smf/). After you click Add server, you'll see your package server in the list. Just click [\[ Browse \]](javascript:void(0);) next to it, and you're ready to download your own packages!  
  
Thanks for contributing,  
Simple Machines
