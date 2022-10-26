Coding Standards
**********************
The following set of guideline items should be followed when coding the new banking product. 

Indentation
--------------------
Indentation should be used to: 

Four (4) spaces shall be used to indent. Tabs shall not be used for indentation purposes. 

Example

//Indentation used in a loop construct. Four spaces are used for indentation.

for ( int i = 0 ; i < count ; i++ ) 

{

     //some work   

} 

Inline Comments
---------------------

Inline comments explaining the functioning of the subroutine or key aspects of the algorithm shall be frequently used.

Classes, Methods and Namespaces
--------------------------------------

Classes, methods and namespaces shall be reasonably sized. We shall as much as possible try to constrain each method to limited action(s).

The names of the classes, methods and namespaces shall have verbs in them. That is the names

shall specify an action e.g "GetAccount", "GetUser".

We will use PascalCasing for class names and method names, camelCasing for method arguments and local variables this is because its consistent with the Microsoft's .NET Framework and easy to read.

Abbreviations will be avoided when possible

Bad : CustomerAccount custmrAccnt 

Good : CustomerAccount customerAccount

When not avoidable use PascalCasing for abbreviations 3 characters or more 

e.g. CustomerAccount custAccount 

Avoid use of Underscores in identifiers

Use predefined type names instead of system type names

Bad : String userName; 

Good : string userName; 

Bad : Boolean isActive; 

Good : bool isActive; 

Organize namespaces with a clearly defined structure

Declare all member variables at the top of a class, with static variables at the very top

Methods shall be invoked using POST only.

Source Files and Folders
-------------------------------
The name of the source file or script shall represent its function 

e.g. Identitymaintenance.cshtml 

The name of the folders shall represent the general functionality of source files within 

e.g. Folder : Identity > File : Identitymaintenance.cshtml

Variable Names, Parameters/Arguments and Constants
-------------------------------------------------------------
Variables, Parameters and Constants shall have meaningful names that show its intended use.  These shall be initialized prior to their first use.  – both local and private

Leading and Trailing spaces in all holders shall be trimmed prior to transmission from both Application and API 

Member & Static variable declaration
-------------------------------------------
Static variables must be declared at the top of the class. All member variables must be declared at the top of the class after the static variables are declared. No variables should be 

declared in between method definitions or in the middle of the file. 

Enum variable naming

*With an exemption of bit field enums, all enums must be named as singular nouns.

Variable Conversion
------------------------------
When converting variables from one data type to another, always use the convention below.

GOOD CONVERSION

String myvar = “”;

myvar = Convert.ToString(myothervariable);

BAD CONVERSION

String myvar = “”;

myvar = myothervariable.ToString();

Using the Convert.ToString() conversion handles null values/invalid keys and other exceptions and returns an empty string (“”) compared to the .ToString() which would throw an error if 

the variable being converted is an empty string (“”)

Use of Braces
---------------------
We shall use the Allman bracing style:

::
    for (int j = 0 ; j < max_count ; ++j) 

    {     
        // Some work here.
    } 

  
     
Braces shall be used even when there is only one statement in the block;

