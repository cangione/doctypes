Introduction


This readme.txt file includes various instructions, descriptions, and 
information about all aspects of a TMSS DSS.  The contents of this readme file 
will apply to all users, but the installation procedures described in Paragraph 
#2 and #3 are for JCALS users.  If you are installing this DSS on an independent 
system, please contact the TMSS office for additional information.  Below is a 
breakdown and description of the contents of this readme file.

1.0 	Contents of this zip file

2.0	JCALS Installation

	2.1	Launching the Publishing Administration Tool 
	2.2	Preparing for Installation
	2.3 	How to Import and Install a DTD, ATD, Screen Style Sheet, and
		template
	2.4	How to Import and Install a FOSI

3.0 JCALS configuration

	3.1	Creating Links for all DSSs

4.0 OmniMark
	
	4.1	Use of OmniMark scripts
		4.1.1		JCALS users
		4.1.2		Non-JCALS users
		4.1.2.1	Directory Structure 
		4.1.2.2 Create a Library File
		4.1.2.3 Modify Scripts 
	4.2 Running an OmniMark program

5.0 ISO Entities
	5.1	Contents of the zip file 
	5.2	Installation 

*****    *****     *****     *****     *****     *****

1.0	Content of the Zip File

Each zip file contains the following pieces of the DSS.



1) resolved DTD (with entity calls removed)

	2)	FOSI for DataLogics DLComposer

	3)	screen FOSI for Adept Editor Version 8.0

	4)	screen FOSI for Adept Editor (for any version below 8.0)

	5)	Auxillary Tag Description

	6)	Tag Description Table

	7) Instance containing a minimal tag set to serve as an outline

	8) Sample instance containing a more robust example of the DSS

	9) OmniMark zip file

	10) ISO Entities zip file

	11)	this README file



*****    *****     *****     *****     *****     *****



2.0	JCALS INSTALLATION

For any user currently publishing on the JCALS system, most of the installation 
described below will in most cases be handled by your system administrator.  In 
any case, the instructions will lead you through the full installation of the 
attached DSS on to the JCALS system.  Paragraph 3 will complete the installation 
procedure by defining the configuration management needed to complete the 
installation onto JCALS.



2.1	Launching the Publishing Administration Tool



This tool is used to install the DSSs.  Before installing anything, this tool
needs to be opened to rebuild the maps before making modifications to them.  



Perform the following Steps:



STEP 1:	Log onto the system as JADMIN. Using the left mouse button, double-
click on the Tools icon.  The Desktop Toolbox is displayed.  Double-click on the 
Publishing Administration icon in the Toolbox.  An information dialogue box is 
displayed informing you that the Publishing Tool is being started, followed by 
the Select a Publishing Tool Window.



STEP 2:	Click on Manage DTDs and FOSIs in the Type field of the Select a 
Publishing Tool Window.  A list of subtypes is displayed in the Subtype field.



STEP 3:	Click on Manage DTDs and FOSIs in the Subtype field, then select the 
OK button.  The Pub Admin. Tool Control Panel is displayed.



STEP 4:	Click on the Rebuild Map button.  Wait for the "Maps have been 
rebuilt" message.  This may take a few minutes.  This rebuilds the entity.map 
and entities.xlr files from the system.map file.



STEP 5:	Select the Exit button to close the Control Panel and return to the 
JCALS Toolbox.  Continue on to 2.2





2.2	Preparing for Installation



Now that the map files have been rebuilt.  Perform the following:


STEP 1:	Go to /jcals/wss_data/sgml_applications directory and make a backup 
copy of the original system.map file.



STEP 2:	Go to /home/afcpo-scripts directory and locate the system.map file 
from PDSM PO.  Copy that system.map file into the 
jcals/wss_data/sgml_applications directory under the same name.



STEP 3:	Go to the /jcals/wss_data/sgml_applications directory from the 
command line and make a directory called services.  Just type: mkdir services.  
The directory must be lowercase and make sure there are write permissions on the 
services directory for the owner and group.



STEP 4:	Build the maps again by executing steps 1-4 of section 2.1 again.  
Once maps have been rebuilt, you are ready to start installing the DSSs.  Keep 
the Pub Admin Control Panel up because you will	be using it for installation.



STEP 5:	Go into the /jcals/wss_data/sgml_applications directory and open 
system.map.  Scroll down to Class=services.  Then scroll to Family=airforce.  
This is where the names of the DSSs to install to JCALS are located.  Write the 
names of the DSSs down because the exact name is required when installing.  



		For example, use 38784STD-BV3 DSS.  
		This is the new naming convention for the MIL-STD-38784B DSS. 
		
		This is how they would look:



		DTD 		38784STD-BV3.dtd
		Screen Fosi	38784STD-BV3.fos

		ATD		38784STD-BV3.atd

		Template	38784STD-BV3_test.sgml

		FOSI		38784STD-BV3.fosi



STEP 6:	Go back to the Pub Admin Tool Control Panel that should still be 
open and execute section 2.1 step 4 again.  Continue on to 2.3





2.3	How to Import and Install a DTD, ATD, Screen Style Sheet, and Template



		NOTE



	It is good practice to import a DTD, ATD, screen style sheet,
	and template.  This insures consistency among the various files 
	and document versions.  The SGML declaration is automatically 
	imported.  You should still be at the control panel after rebuilding
	maps.  For example, we will use 38784STD-BV3 DSS.
	This should be the first that gets installed anyway.  After 
	that follow the order you see in the system.map file.





STEP 1:	Select the New button from the Control Panel.  The New Panel is 
displayed. 



STEP 2:	In the New Panel, type a DTD name (38784STD-BV3) in the Name field, 
and select the DTD button. Do not put the extension on the name, the system will 
automatically attach it.  The Edit Panel is now displayed.



STEP 3:	Select the Import... button.  The Import Panel is displayed.



	· Installed - Installation area; contains JCALS DTDs and FOSIs.

	· Working - Publishing Administration Tool filing area; contains
			publishing administration files on which work is
			being performed.

	· Filing - Filing Service area for Jadmin; this is where the DSSs 
			was installed from the tape.  To look at these 
			go to ~jadmin/filing directory.



STEP 4:	Click on the filing button for the DTD, ATD, Screen Style Sheet, and 
Template.  When you click on each you will get a list of what is in the 
jadmin/filing directory.  Do not click on SGML Declaration.  For example, use 
38784STD-BV3.  When clicked, the system automatically puts the extension on the 
file and displays it under file field in the Import panel.



STEP 5:	Once the DTD, ATD, Screen Style Sheet, and Template are selected, 
select the OK button.  The edit panel will be displayed again.


STEP 6:	Select the Compile button.  This will compile the DTD and the Screen 
Fosi.  There will be a message saying the DTD is compiling and then the Screen 
Fosi is compiling.  Once they are both compiled successfully, select the Install 
button.  



STEP 7:	The Installed DTD list is displayed.  Select the arrow key for each 
option.  For example,  for Class select services, for Family select airforce, 
for Group select 38784STD-B, and for Version select V3.  Then select OK.



STEP 8:	The Select Root Element Window is displayed.  For example for 
38784STD-BV3 the root element is "doc".  Select "doc" and click OK.  Then the 
Public identifier window is displayed.  Make sure the public identifiers are the 
same and click OK.  



STEP 9:	An information dialog box, "DTD 38784STD-BV3 installed" is 
displayed.  Then an information box is displayed asking whether to delete the 
DTD from the Admin WIP area.  Always select the YES button.



STEP 10:	Select the Control Panel button to go back to the Pub Admin Control 
Panel.  Continue...








2.4	How to Import and Install a FOSI



Once the DTD, ATD, Screen Fosi, and Template are installed, go back to the
Pub Admin Control Panel.  Now install the FOSI for that DSS.  
Follow these steps:



STEP 1:	Select the New button from the Control Panel.  The New Panel is 
displayed.



STEP 2:	In the New Panel, type a FOSI name in the Name field (38784STD-BV3) 
and select the FOSI button.  The Edit Panel is displayed.



STEP 3:	Select the Import ... button on the Edit Panel.  The Import FOSI 
Panel is displayed.



STEP 4:	Select the Filing button.  A list of FOSIs is displayed.



STEP 5:	Select a FOSI (38784STD-BV3).  The selected FOSI is displayed in the 
File field of the Import Panel.  Click OK.



STEP 6:	The Edit Panel is displayed again.  Select the Compile button.  
There will be a message saying its compiling the FOSI.  Once the FOSI is 
compiled successfully, select the Install button.  



STEP 7:	The Install FOSI Panel window is displayed.  The Class, Family, 
Group, Version, and Name should be filled in and already associating this FOSI 
with the correct DSS (i.e., 38784STD-BV3).  Then Select OK. 



STEP 8:	An Information dialog box,  "FOSI Installed," is displayed. Then an 
information box is displayed asking whether to delete the FOSI from the Admin 
WIP area.  Always select the Yes button.



STEP 9:	Select the Control Panel button to go back to the Pub Admin Control 
Panel.   Click on Rebuild maps.  Now your first DSS is installed.  Repeat 
sections 2.3 - 2.4 until all DSSs are installed.






*****     *****     *****     *****     *****     *****



3.0 CONFIGURATION


As stated, this paragraph will provide instructions to complete the installation 
process onto JCALS.  Again, please contact your system administrator if they are 
in charge of installing this DSS.

3.1	Creating Links for all DSSs



After the DSSs have been installed onto the JCALS System, links must be created 
before composition.  These links are named to a specific public identifier for 
each DTD.  Without these links, the parser/composer will not be able to find 
other DTDs using the entity declaration's within the DTDs that are being 
composed.  The basic.setup file contains the mapping to the links directory.  

The mapping to the links directory is done in the basic.setup file.  Do not 
chang ehte names for the DSS and links because the external and internal IDs are 
linked to these specific names.  Follow these steps:



STEP 1:	As Jadmin, from the command line, go to the
		/jcals/wss_data/sgml_applications/modules/links directory.  



STEP 2:	To Link type: 


		ln -s path to the file/filename filename you're saving it to 



	Hint:	The filename linked with must be exactly the same as the public 
identifier.



		For example, 38784STD-BV3 would look like this:

		
			ln -s 
/jcals/wss_data/sgml_applications/services/airforce/38784STD-B/V3/38784STd-
BV3.dtd 38784STD-BV3
		
	NOTE

		

	This procedure must be done for every DTD that is installed on JCALS.  To 
find the path for each DTD you can reference the system.map file located in the 
jcals/wss_data/sgml_applications/ directory.  The directory path for any DSS 
will always start with /jcals/wss_data/sgml_applications.  The system.map file 
can give you the remaining DTD pathname. 
	
	For all DTDs, all paths will have services/airforce.  The name used for 
the link is always going to be the name of the DSS without any extension (i.e., 
38784STD-BV3).  This is the public identifier for this DTD, the link makes it 
possible to find the DTD in JCALS by seeing it anywhere within a DTD that makes 
a call to it.   



*****     *****     *****     *****     *****     *****



4.0	OmniMark

OmniMark is a text processing language that is used by the TMSS group to allow 
authors to auto-generate redundant material that may be difficult to tag 
manually.  Every DSS released by the Air Force TMSS will have an OmniMark zip 
file that contains, at a minimum, the scripts needed to complete tagging for 
38784STD-B requirements.

The OmniMark zip file contains all programs, the script to run these program and 
a readme.txt file specific to that individual program.  Also included are two 
files that may be necessary for NON-JCALS users.  The first is a sample library 
file and the second is a copy of the 28001B Concrete Syntax.

4.1	Use of OmniMark scripts



The OmniMark scripts must be customized to meet the requirements of your system.  
If you are an existing JCALS user, you will not have to perform any of these 
customizations (instead see paragraph 4.1.1).  All OmniMark scripts operate from 
the Unix command line and utilize a library file, a concrete syntax, and 
OmniMark programs.
 
There are four basic elements of a script identified by a special delimiter on 
the script command line.

-s identifies the source program, concrete syntax and the input file for this 
particular program, as well as their locations on your system.  When a $1 is 
used within a -s parameter, it means the name will be input from the command 
line.  

-of identifies the output file of the program  

-library identifies the library file and its location on your system

-define identifies any special files needed by OmniMark as input into the 
program.  In most cases, the -define parameter is used to gather files created 
by OmniMark during processing.  At the end of most scripts, all files created 
during the processing of an instance are deleted from your directory.

Below is an example of a very basic script:

********************************************************************************
OmniMark -s /mydirectory/OmniMark/myprogram.xom 
/mydirectory/OmniMark/28001con.syn input.file -of output.fil -library 
library.file 

********************************************************************************

OmniMark uses the ";" character to indicate a comment so if this character 
precedes any line in a file, OmniMark will not recognize it.  This character may 
be helpful if our example a file uses ISO entities not currently available on 
your system.  Also, if you need to comment our programs for any reason, use of 
this ";" character will allow you insert comments without harming the 
functionality of the program.


4.1.1	JCALS users  



The following lines of code should be added to your basic.setup file located

in /home/afcpo-scripts/

	setenv LM_LICENSE_FILE $OMNIMARK_DIR/license.dat
	setenv JCALS_CONFIG "/jcals/wss_data/sgml_applicatios/services/omniscripts/v6/configuration.sh"

	set path = ($path /jcals/wss_data/sgml_applications/services/omniscripts/v6)
	set path = ($path /jcals/wss_data/sgml_applications/services/omniscripts/)



The scripts should be copied into the directory:



	/jcals/wss_data/sgml_applications/services/omniscripts/v6



All programs should be copied into:



	/jcals/wss_data/sgml_applications/services/omniprograms/v6



By installing into these directories - the scripts can be used and

executed with no further modifications.





Below is an example of an existing script used on the JCALS system:



*************************************************************************


LM_LICENSE_FILE=$OMNIMARK_DIR/license.dat

export LM_LICENSE_FILE

#Above two lines needed for OMNIMARK to run on JCALS

#For some reason these need to be at the top of the file????



omnimark -s /jcals/wss_data/sgml_applications/services/omniprograms/87929B-
I/remove_dash1V1.xom $1 -of $1.dash -library 
/jcals/wss_data/sgml_applications/services/library/wndlibrary.txt



omnimark -s 
/jcals/wss_data/sgml_applications/services/omniprograms/87929B/remove_contentsV1
.xom  /jcals/wss_data/sgml_applications/services/library/28001con.syn $1.dash -
of $1.out -library 
/jcals/wss_data/sgml_applications/services/library/wndlibrary.txt -define 
inputfile $1


**************************************************************************




4.1.2	Non-JCALS users


For those users who do not use the JCALS environment, you will have to perform 
three steps. 
1. Define the directory structure
2. Create a library file (sample file is provided in this zip file)
3. Copy the concrete syntax file into your system
4. Modify your scripts to point to the directory location of the programs, the 
concrete syntax, and a library file.  

4.1.2.1	Directory Structure

OmniMark does not really concern itself with a particular directory structure.  
You only need to develop a structure that you can understand and maintain.  As 
with the JCALS setup described above, you may want to keep your scripts and 
programs in a central location, but it is not necessary.  You can model the 
JCALS setup with a root directory and several sub-directories with a unique 
subdirectory for programs, scripts, etc.  Or, if you prefer, you can put the 
scripts, programs, library files, and concrete syntax in one directory.

4.1.2.2	Create a Library File 

The library file is merely a map for OmniMark to navigate your system.  You need 
to identify the ISO Entities and any DTD that OmniMark will reference.  At 
runtime, an OmniMark script will go out and search the system based on your 
library file and locate the ISO Entities and the particular DTD needed to parse 
your input file.  The JCALS library file is title:  wndlibrary.txt and was named 
to match an element on the JCALS system.  Your particular library file can have 
any name you desire.  This file contains a sample library file that you can 
reference or modify to suit your system.

In addition, any DTD that will be referenced by an OmniMark script or program 
must be declared in the library file.  It is not necessary to include a DTD 
declaration for every DTD loaded onto your system, since you may not run 
OmniMark on every DTD.  BUT, it is a wise practice to add any new DTD since at 
some point, it may become necessary to execute an OmniMark script on an instance 
that calls that DTD.  In addition, every DSS will, in all likelihood, utilize 
the OmniMark programs developed for 38784STD-B.

4.1.2.3	Modify Scripts

The scripts provided in this zip file were developed to match the JCALS 
structure, but very minor modifications can make the script compliant with your 
directory structure.  For example, the script:

*************************************************************************


LM_LICENSE_FILE=$OMNIMARK_DIR/license.dat

export LM_LICENSE_FILE

#Above two lines needed for OMNIMARK to run on JCALS

#For some reason these need to be at the top of the file????



omnimark -s /jcals/wss_data/sgml_applications/services/omniprograms/87929B-
I/remove_dash1V1.xom $1 -of $1.dash -library 
/jcals/wss_data/sgml_applications/services/library/wndlibrary.txt



omnimark -s 
/jcals/wss_data/sgml_applications/services/omniprograms/87929B/remove_contentsV1
.xom  /jcals/wss_data/sgml_applications/services/library/28001con.syn $1.dash -
of $1.out -library 
/jcals/wss_data/sgml_applications/services/library/wndlibrary.txt -define 
inputfile $1


**************************************************************************

could be modified to read:

*************************************************************************


LM_LICENSE_FILE=$OMNIMARK_DIR/license.dat

export LM_LICENSE_FILE

#Above two lines needed for OMNIMARK to run on JCALS

#For some reason these need to be at the top of the file????



omnimark -s /omnimark/87929B-IV3D1P0_remove_dash1.xom $1 -of $1.dash -library 
/omnimark/wndlibrary.txt



omnimark -s /omnimark/87929B-IV3D1P0_remove_contents1.xom  
/omnimark/28001con.syn $1.dash -of $1.out -library /omnimark/wndlibrary.txt -
define inputfile $1


**************************************************************************



4.2	Running an OmniMark program

There are many different types of scripts released with the TMSS DSSs.  They 
range in spectrum from executing one program to several complete compositions 
coupled with numerous OmniMark programs throughout.  Not only will some of these 
scripts execute an OmniMark program, they will also invoke DataLogics composer 
and possibly some command line executions like parsing your DTD.

To execute a script, from your working directory type in:

	scriptname.sh filename
	
where	scriptname.sh is the script you wish to run and 
	filename is the name of the file you wish to use as input
	
You may decide that you have no need for any of the OmniMark scripts that we 
provide as part of a release.  In most cases, these scripts just facilitate 
tagging that can be performed manually.  But, the scripts will save authoring 
time.  

All DSS's that rely on MIL-STD-38784 Version 3 will be able to utilize 38784STD-
BV3 scripts to generate acronym lists, alphabetical indicies, or assist in the 
composition of the verification status page.  MIL-STD-38784 will also include 
scripts and programs to generate a numerical index or reference designator index 
when developing a combined manual.

Every DSS released by the TMSS office will contain these standard 38784 scripts 
and associated programs within a zip file. In addition, your particular DSS may 
have its own set of unique OmniMark scripts and programs.  Contained within each 
zip file will be the scripts, programs, and a readme file that will outline the 
purpose of the OmniMark for your DSS and provide a list of the scripts and 
programs provided for your DSS.




*****     *****     *****     *****     *****     *****


5.0 ISO Entities

The ISO entities are needed to properly parse and compose instances using the AF 
TMSS DTD and FOSI.  These files are included as a zip within the zip file for 
your DSS.  Please keep in mind that any users currently running in a JCALS 
environment should not have to install the ISO Entities.  They should already be 
available on your system.  These instructions should be relevant to any users 
who are running on a NON-JCALS system or any users that utilize ArborText Text 
Editor Version 8 or above.

5.1 Contents of the zip file

Small EPS Symbols - V1	 - contains the public identifiers for every small eps 
symbol
Small EPS Symbols - 1 (tar file)	- contains the actual graphic files for 
small eps symbols
Small EPS Symbols - 2 (tar file)	- contains the actual graphic files for 
small eps symbols
Big EPS Symbols - V1	 - contains the public identifiers for every big eps 
symbol
Big EPS Symbols (Tar File)	- contains the actual graphic files for big eps 
symbols
JCALS supported ISO-ENTITIES V1
icons.zip	- contains all standard AF icon eps files


5.2 Installation

The first step to properly installing the ISO components of this zip file is to 
copy all of the entity and graphic files onto your system.  Again, this step is 
not necessary if you are running on a JCALS system.  These files and entities 
should already be in place, contact your System Administrator if you have any 
error messages that reference ISO Entities or EPS Symbols.

We would suggest that you create a directory on your system to house all the 
entity and graphic files.  Once you have loaded the files onto your system 
and/or identified their directory, you must modify all declarations.  

Simply stated, the first file provided - SMALL EPS SYMBOLS - V1 is a file that 
contains nothing but entity declarations for each of the small eps symbols 
contained in the tar files (small eps symbols 1 tar and small eps symbols 2 
tar).  This file must be called by your DTD.  The DTD calls the SMALL EPS 
SYMBOLS using its public identifier and that file in turn, will call all the 
small eps symbols by their individual public identifiers.

The declarations for all of these files must be modified to point to the 
location of these files on your system.  For example, the DTD declaration for 
SMALL EPS Symbols on the JCALS system is:

<!ENTITY % local-small-symbols "INCLUDE" >
<!ENTITY % eps-sml PUBLIC "-//JCALS//ENTITIES small EPS symbols v1//EN">
%eps-sml;

These three lines contain a marked section set to INLCUDE (line 1), the 
declaration (line2) and the entity call (line3).

You will have to modify your DTD to point to the correct location of these files 
on your system.  For instance, if your files are located on your system in a 
directory called isoentities, the above declaration would be modified to read:

<!ENTITY % local-small-symbols "INCLUDE" >
<!ENTITY % eps-sml PUBLIC "-//JCALS//ENTITIES small EPS symbols v1//EN"
"/isoentities/ENTITIES_small_EPS_symbols_v1">
%eps-sml;


In addition, each line of the SMALL EPS SYMBOLS V1 file must be modified in a 
text editor to reflect the location of the graphic files on your system.  Below 
is an example of the file with this modification.

<!ENTITY adown SYSTEM "/isoentities/adown.eps" NDATA EPS>
<!ENTITY ai SYSTEM "/isoentities/ai.eps" NDATA EPS>


Finally, the sample catalog file is included for any users that rely on 
ArborText V8 for authoring.  The catalog file on your system should be modified 
to correctly point to the location of the ISO declarations on your system.  The 
sample catalog file is provided as a reference to complete this modification.  
