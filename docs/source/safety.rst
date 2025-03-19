Safety
======

When it comes to programmatically dealing with financial accounts **safety and data protection should be a 
number one priority**. There are a couple things we can do to prevent and/or minimize bad situations.

Securing Your tokens
--------------------
If anyone is able to get their grubby little hands on your Akahu tokens they will be able to do **EVERYTHING**
you can do with the Akahu API. To stop this from happening we can implement a secure way to use tokens in our
programs. Check out `this Data Camp article <https://www.datacamp.com/tutorial/python-environment-variables>`_ 
on how to get started with environment variables. 

.. warning:: 
    If you are using a version control like git, make sure you add the file that these tokens are stored in
    to the gitignore file. If you do accidentally leak these tokens, you can reset them in the 
    `my Akahu <https://my.akahu.nz/developers>`_ dashboard and clicking "Regenerate" at the bottom of the page.

Restricting Permissions
-----------------------
If you plan to only use your program to read any financial data connected to your Akahu account you should remove all
permissions that aren't needed. You can do this by going to the `my Akahu <https://my.akahu.nz/developers>`_ dashboard,
then to developers tab and scrolling down to "Permissions" and removing any unnecessary permissions.

Restricting IP Access
---------------------
If you plan to host your program on a dedicated server that has a static IP, you can restrict access to that IP address.
To do this go to the `my Akahu <https://my.akahu.nz/developers>`_ dashboard, then the developers tab and scrolling down to
"IP Address Ranges".

Restricting Account Access
--------------------------
If you have many accounts connected to Akahu but only want to access one with your program you can remove your personal app's
access to any unnecessary accounts. To do this go to the `my Akahu <https://my.akahu.nz/developers>`_ dashboard, then the developers tab,
scroll to the "accounts" section and edit the permissions accordingly. 

**Be safe!**



