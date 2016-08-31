### **Organizations User Guide**

### About CORAL Organizations

A component of Hesburgh Libraries locally developed ERM, CORAL Organizations provides a way to store and manage names, contacts and account information for the many publishers, providers, vendors, etc that libraries interact with on a daily basis all within a single searchable location.

### Component Overview

CORAL Organizations has three major components in the primary navigation at the top of each page.

• Home

• New Organization

• Admin

#### Home

image of main home screen

Search has been placed on the Home page as the primary point of entry into the organization records. There are two keyword searches available. The first keyword search 'Name (contains)' searches against organization name and organization alias. For example, AIP could be retrieved by searching for any or all of the words in American Institute of Physics or by the alias AIP. The second keyword search available is ‘Contact Name (contains)’. This allows the user to search for the name of a known contact (ex. Jane Smith) instead of searching for the name of the organization.

Users also have the ability to search by an organization's role (ex. Publisher, provider, library, etc). And the last search option is more of an AZ browse for the retrieval of organizations by the first letter of the name.

#### New Organization

The purpose of the 'Parent' field is to relate multiple organizations together and to create an organization hierarchy. The field includes an auto-fill populated by existing organization records. The parent organization must already have an existing organization record in order for it to be assigned. Each organization may have only one parent assigned but multiple organizations may have the same parent thereby creating a useful parent-child hierarchy.

image of Add New Organization screen

Select New Organization from the main navigation to begin adding new organization records. The link will present the window on the right.

'Name' is the name of the organization (i.e. MetaPress, Sage Publications, etc). This is the only required field.

'Parent' is the name of the parent organization (i.e. Proquest as parent of Chadwyck-Healey).

'Company URL' is meant to be the url of the organization’s homepage.

'Role(s)' is the organization’s role. The values for this field can be customized through the Admin page.

'Account Details' is meant for account numbers and general descriptive info about a library’s account with the organization. The ‘Notes’ field is for general notes.

#### The Organization Record

image of main Organization Record

Here is an organization record for Cambridge Scientific Abstracts. The information on the record is split among five tabs. The sixth tab labeled Licenses is an interoperability feature with CORAL Licensing.

The Organization Record

* Organization: This tab displays the information found on the New Organizations screen explained on the previous page.

* Aliases: This tab is for adding alternate names and acronyms so that the record can be retrieved using various names.

* Contacts: This tab includes contact information for the organization (ex. Email, phone numbers for sales reps).

* Accounts: This tab is for managing administrator accounts (ex. Username/password logins for usage statistics collection).

* Issues: This tab is intended for recording major incidents with the organization and/or its resources (ex. Publisher changed servers and access was lost for several days).

* Licenses: This tab will display links to the records in CORAL Licensing for all licenses from the organization. This is an interoperability feature which can be activated when both CORAL Licensing and CORAL Organizations are installed.

##### Organization

The figure above shows the organization tab for Cambridge Scientific Abstracts. Notice that this screenshot does not display the 'Account Details', ‘Notes’ or ‘Company URL’ fields that were found on the New Organization window on the previous page. These three fields are not displayed because no data was entered into those fields when the record was added. This was done in order to save space and to create a cleaner design. The ‘edit organization details’ link will open the same window as seen on the previous page so that the user can further edit the organization name, role, etc.

In this example Cambridge Scientific Abstracts has been assigned ProQuest as the parent organization. The 'view' link next to ProQuest LLC will open the ProQuest organization record.

##### Aliases

image of example Alias CSA- Cambridge Scientific Abstracts

The Aliases tab allows the user to add multiple aliases for the organization. In this example, the acronym CSA has been added. Each alias is assigned an alias type. The default values for the 'Alias Type' field are Alternate Name, Name Change and Acronym. These field values can be customized using the Admin page discussed later in this document.

##### Contacts

image of example

The Contacts tab allows the user to add contact information such as phone numbers and email addresses for specific personnel as well as general support. There are two options for adding new contact information; 'add named contact' and ‘add unnamed contact’. These two links open the windows shown on the next page.

Add Named Contact Add Unnamed Contact

side by side images exmaples

The 'add named contact' and ‘add unnamed contact’ links open the two windows above. The only difference between the two is that the unnamed contact has no Name or Title field. Generic contact numbers such as a technical support 1-800 number would be added as an unnamed contact. Specific personnel such as a license manager or sales representative would be added as a named contact.

The values for the 'Role(s)' field can be customized through the Admin page discussed later in this document. Named and unnamed contacts use the same role values. The ‘Archived’ field is likely the only field that needs further explanation. Contacts can either be deleted or archived when the information is no longer accurate. Contacts that have the ‘Archived’ box checked are kept in the system but are collapsed beneath a ‘show archived contacts’ link so that all users know that the contact information is out of date. This was done for historical tracking purposes so that a library can record who their license managers, etc have been over the years. The ability to delete a contact has been restricted to users with admin privileges because of the chance that a contact might be deleted when it should only be archived.

##### Accounts

The Accounts tab is used for storing login information that library personnel use for site administration, gathering usage statistics, etc. Account login information can be entered in either CORAL Organizations or CORAL Resources. Account login information which is resource specific may be entered in CORAL Resources. Account login information that is not resource specific (ex. A single administrator login for all Gale databases) should be entered here in CORAL Organizations. Information stored at the organization level will be inherited by individual resources within CORAL Resources. The resource vs organization specific account information may be confusing but it will make more sense when CORAL Resources is installed along with CORAL Organizations.

The 'add new external login' link opens the following window.

##### Add New External Login

image of Add Login form

'Login Type' values can be customized. Default values are Admin, FTP, Marc, Statistics, Support, Other.

'URL', ‘Username’ and ‘Password’ are self-explanatory.

'Local Account Email' is the address of the library personnel registered on the account.

Once again there is an extra notes field for additional information.

##### Issues

image of Issues tab

The Issues tab is meant for recording general information about an organization that may be valuable over time. This could include anything but one example would be recording when an organization has frequent breaks in access or significant server downtimes. Another example would be having an organization that is often slow when it comes to sending out renewal invoices. The 'add new issue' link opens a new window which includes a date and notes field. It is a simple field but it may come in handy for recording the institutional knowledge that exists among various personnel.

image of the License tab with example

##### Licenses

The Licenses tab is only available when CORAL Licensing has been installed and the interoperability enabled. This tab will provide links to the license records within CORAL Licensing for all licenses where the organization has been identified as the Publisher/Provider. The hyperlinked license name will open the license record in a new window.

#### Admin

The Admin page is where you can manage user privileges as well as edit the values for organization role, contact role, alias type and external login type. As with the other modules, CORAL Organizations is designed to work with your campus authentication system (see the technical documentation for details). All valid users are given view only access when logged into CORAL Organizations unless they have specifically been granted additional privileges. You only need to add specific user accounts for personnel that need more than view only privileges. The available privileges are 'view only', ‘add/edit’ and ‘admin’. The ‘add new user’ link on the Admin page opens the following window where ‘Login ID’ is the user’s campus ID.

Privileges

* Admin : provides full add/edit rights including access to the Admin page and the ability to delete contacts.

* Add/edit : provides ability to add/edit organization records and all available fields but does not grant access to Admin page and does not give permission to delete contacts.

* View only : provides only the ability to view existing organization records.

side image with Add New User form
