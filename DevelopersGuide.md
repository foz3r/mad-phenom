# Download Atmel AVR Studio #

Development of this firmware is done in the Atmel AVR Studio IDE.  In order to download the free IDE you must register.  Registration is free and available at the following location: [Atmel Studio Download](http://www.atmel.com/tools/atmelstudio.aspx)

# Download Git #

Git is used to store the source code for the firmware.  Download and install Git from the following location:

[Git Download](http://git-scm.com/)

# Download Source Code #

Once Git has been installed, open a command prompt or terminal window in your machine and execute the following command within the folder where you would like the project to be located on your harddrive:

`git clone https://github.com/mikedehaan/mad-phenom.git`

Once this command completes, navigate to the folder and double click on the mad-phenom.atsln file.  This should open Atmel AVR Studio and load the mad-phenom project.

# Tagging in Git #

Tag the version
<pre>
git tag -a v0.9.2<br>
</pre>

Share the tags with the main repository
<pre>
git push origin --tags<br>
</pre>