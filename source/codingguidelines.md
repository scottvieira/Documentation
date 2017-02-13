Coding Guidelines
-----------------

This page lists the CORAL coding guidelines. It's shared between all modules, so these rules apply for all of them.

### Naming standards 
If you would like to contribute code / database changes to the project it is recommended that you stay
within the following naming conventions. 

#### Database Naming:
 
* Attribute and entity names in singular form and using present tense 
* Entity names are uppercased with no spaces or underscores between words (camel case) 
* Attribute names have first word lower cased, subsequent words have first letter upper case 
    * e.g. documentID, sentDate, documentText 
* Primary keys are always Auto Incrementing Integers beginning with the table name and ‘ID’ 
suffix 
    * e.g. for the “Document” table, “documentID” is the name of the primary key 
    * (note that the generic database object expects this naming convention – if you do not use this name, you must override the primary key name in the class) 
* When possible, attribute names are suffixed with class words 
    * Code - Has a list of possible values e.g. INV, ENC 
    * ShortName - Name 
    * Identifier (ID)  - Unique Identifier, generally surrogate key 
    * Number - Numeric value 
    * Indicator (Ind) - A Boolean value (0/1)
    * Date - Date 
    * DateTime - Date and time stamp 

#### Code: 
* Refer to previous sections for directory structure, script locations and script naming. 
* Variable, class and attribute names mimic the database standards with camel case. 
* Method names are prefixed with:  
    * Is – Answers a question, returns true/false, e.g. for User class `isAdmin()` method 
    * Get – retrieves a value 
    * Set – sets a value

### Issues & Pull requests

Any pull request must be related to an issue. In the 1st line of the commit message, please add "(issue #nnn)" at the beginning of the message. For example : "(issue #23) Fixes this and that". Ideally, the message is the same as the title of the issue.

### Database update

When a patch is submitted that requires a DB change, the changes must be provided in a separate SQL file.
When merged into the master repository, the DB change file is appended to the update_NEXT.sql file by the merger.
before releasing a new version, the update_NEXT.sql file will be renamed to update_.sql
Translating

For the translation you must think to use the next syntax to help the translation will be more easy:

For the code PHP: _("string PHP to traslate")

If you want translate the string "Hello", you can do this: <?php echo _("Hello"); ?>

For the code JavaScript: _("string JavaScript to translate")

Example: alert(_("There are some errors"));