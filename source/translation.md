Translation for CORAL
---------------------

### Translation of ERMS CORAL

All modules of this ERMS can be translated with the tool GNU gettext to continue with the use of free software. GNU gettext use internationalization and localization to display adapted information to the language required for the user. The internationalization is how the application is made to support multiple languages and the localization is how the application is adapted to the language required for the user.

### Programming languages supported

This tool is used to translate applications in different programming languages (you can find all programming languages here).

### How it works?

We use the files .po which contains all strings to translate and the files .mo, these files are binaries which are used for the machine to translate the application, both files have all strings but in different languages, understandable for each user (human and machine). You should use a file .po for each language and located in a special folder which has the name of the language.

### Structure of languages supported

GNU gettext use the local names of the system with the structure "ll_CC" where ll is the code ISO 639 for the code of language and CC is the code ISO 3166 of the country, for example, if I live in Mexico the local name is "es_MX" where es is the code for the Spanish language and MX the code of Mexico.

Also, there are many local names which support different characters encodings today is used UTF-8 in most cases but also exist ISO-8859-1. To add a character encoding in the locale name you use the next syntax: "ll_CC.encoding" where encoding is the name of the character encoding. For example, I would use UTF-8 with the French language, the local name for this example is: "fr_FR.UTF8".

You can find all codes ISO 639 here and the codes ISO 3166 here.

You can see the complete documentation of GNU gettext here.

### Folder structure

We recommend use the next structure for all languages:

locale / ll_CC / LC_MESSAGES / file.po

The folder locale is the main folder where all languages supported for the application stay.
ll_CC is the local name of the translation, you must use this to difference between the other translations.
LC_MESSAGES is the folder for the file .po, the name of this file is for your consideration.
Example: locale / fr_FR / LC_MESSAGES / messages.po

Note: This structure must be in the root folder of the application

How to obtain the strings?

This is easy you must change the string with this structure, this exemple use PHP:

<?php echo "This is a string"; ?> to <?php echo _("This is a string");?>

The structure is not complicated only use _("string").

### Install GNU gettext in PHP

You should install the option "gettext" in your server, because for default is not found, but most of hostings have installed this option. If you use a server with Debian, you can install gettext like this:

sudo apt-get install php-gettext

Another option to install this, is rebuild PHP with the option --with-gettext[=DIR] where DIR is the gettext install directory, defaults to /usr/local. Install GNU gettext in PHP.

### How add new languages in a module?

The first step to add a new language is create a new folder in locale with the code of language where the translation will be found.
Do the translation of the strings according to the folder structure established
In the file LangCodes.php add the new language code according to the syntax set up.
For example, if I would add the Spanish language, in the method getLaunguage I must add 'es'=>'es_ES' and in getNameLang: 'es'=>_('Spanish').

These are the steps to add a new language, is really easy.

### How add new locales in the system?

If you have added all files and folders, but the translation does not work, is a small problem in the system, very simple to resolve. GNU gettext use a function named setlocale(), this function use a variable of the system named locale, which is used to recognize the language for default in the system. To know how is the language in my system I must write in a console:

locale -a

This console command lists all languages are configured in the system, for example:

C

C.UTF-8

en_US

en_US.iso88591

en_US.iso885915

en_US.utf8

POSIX

If you use a server with a distribution Debian, you can add a new locale with the next console command:

dpkg-reconfigure locales

This command displays a menu with all locales, where you must select the locales to add (with the space bar you can select a locale). After selecting the locales, you must select the locale for default.

Note: If you don't want to change the locale for default in the system, you must select Ok without changing anything in the second menu. We recommended adding the locales with utf8 because is more extensive if you will use the special characters for the translation.

The last step is verify if the locale was added in the system with the console command: locale -a

I added French and the console displays:

C

C.UTF-8

en_US

en_US.iso88591

en_US.iso885915

en_US.utf8

fr_FR.utf8

POSIX

And that's all, if you have changed the locale for default, you must reboot the system to apply the change.

Helpful links

Add locales in Debian.

Add locales in RedHat 7.

Add locales in CentOS 6.

### Implementation in CORAL

The implementation of i18n in Coral will use all those tools. Here are the steps:

Update all strings in php files to add the _(). Many patches, just containing this change everywhere will be submitted. Each patch can be merged independently. without anything else, those patches change nothing at all: the interface will still be in english
generate the .po A tool like poedit can generate them easily.
add a way to handle language selection. We propose to have it on the login page and also on each module, next to the module selection (top-right). For now French and English are supported. It's easy to add a new language. A next improvement (that we expect to do in before june) will be to retrieve langages from the list of po files.
last point to solve: messages that are retrieved through javascript/ajax: they are not detected by poedit. We're still investigating how to solve this problem, there are different options, none of them looking good and easy for now.
2 additional comments:

The default language is automatically identified by CORAL but you can change the language if you prefer.

Most modules of CORAL have the language chooser at the top-right on the page because this is visible for the user to change the language without interfering with the content of each page. For "auth" and "reports" the dropdown is at the bottom side because the top would be interfering with the dynamic content of these modules.
