CORAL Licensing User Guide
---------------------------
 
### About CORAL Licensing ###

A component of Hesburgh Libraries locally developed ERM, CORAL
Licensing provides a way to store and access digital copies of current
and expired license agreements and related documents as well as
associated agreement metadata. The licensing module helps make library
license agreements more accessible to personnel through select
searchable metadata fields and assists institutions in tracking and
using specific pieces of information included in legal agreements.
CORAL Licensing is a flexible document management system, useful in
anticipating a variety of agreements and institutional goals for
managing agreements. The module allows users to identify license
clauses most important to record and track from an institutional point
of view. With related features like a clause comparison function, and
ILL and course pack terms tools that can be implemented to deliver
terms through other systems such as SFX, the CORAL Licensing module
provides a way to make better use of permissions included in the
license agreement.

*Please note that screenshots and text in this document are just
examples and do not necessarily reflect terms for a particular
resource.*

### Component Overview

CORAL Licensing has seven major components in the primary navigation at
the top of each page.

- Home
- New License
- Licenses in Progress
- Expression Comparison
- Calendar
- ONIX-PL File Import
- Admin

### Home

![image of home screen for Licensing modules.  Search features are on the left and a table of licenses on the right.](img/licensing/licensingHome.png)

Search has been placed on the *Home* page as the primary point of
entry into the license records. The search runs against the fields
license name, document name, and publisher/provider. The fields are
defined in the next section as we look at creating a new license
record.

### New License

Select *New License* from the main navigation to begin adding new
license records. The link will present the window shown below.

![screenshot of Add License form. There are three fields.](img/licensing/licensingAddNewLicense.png)

- **License Name:** Name of the license record. A license record can group  together all licenses that are either related to each other or related to the same resource. If you have licensed a package of electronic journals from Springer and have over the years collected several licenses and amendments for that package. You can place all of those documents on the same license record and then you need to give the license record a name which gives some indication as to the documents found on that record. In this example ‘Springer Online Journals’ may be a valid license name. If you have a license record that contains license documents for Springer eBooks, you can rename the license to something like 'Springer Online Products'

- **Publisher/Provider:** Name of the licensing organization. In this
 example Springer would be the publisher/provider.
 
- **Consortium:** Consortium through which a licensed resource is obtained. The consortiums dropdown is populated with any organization assigned a consortium organization type in the Organizations module.

*Interoperability note:* The publisher/provider field has an auto-fill
feature which is populated from the organizations listed in CORAL
Organizations. 

### Adding / Editing New License Record

![screenshot of the License Record.](img/licensing/licensingLicenseRecord.png)
Here is a new license record which has just been created for
*Cambridge University Press Online Journals*. To the right of the
license name are the options to remove the license or to edit the
name, publisher/provider and consortia. Selecting 'Edit Organization' next to the publisher/provider name takes you to the Cambridge University Press record within CORAL Organizations. To the far right is the 'License Status' field where you can also select a license record status.  CORAL Licensing includes the following default statuses.

- Awaiting Document: license record created but scanned license not yet added

- Complete: license record is complete, no additional work required
 
- Document Only: document loaded with expressions not identified or loaded

- Editing Expressions: document loaded and currently adding license terms/expressions

- NLR: no license required

License Status values can be edited, added or deleted through the
[Admin](#bookmark=id.26in1rg)[ ](#bookmark=id.26in1rg) section detailed later in this document. The default values
are simply suggestions for how an institution might consider tracking
agreements and to indicate the purpose of the field.

The license record has four sections located on the left-hand column:
- Documents
- Expressions
- Terms Tool
- Attachments

### Documents

The Documents tab contains all the documents for each license record.
Any document may be uploaded to the system including licenses,
amendments, order forms, purchase requests, or any other important
document. Select ‘Upload New Document’ to begin.

### Adding New Documents

The ‘Upload New Document’ link opens the window in the below screenshot. Here you can fill out the initial details of the document and upload the actual file. Document Name is the only required field.

![screenshot of Document Upload form.  There are 6 fields.](img/licensing/licensingUploadNewDocument.png)

- **Effective date:**  The effective date of the agreement, if identified and available.
 
- **Document Type:** Identifies what type of document this is. This is a customizable field which allows each library to set their own terminology. The software comes with the following types included: Agreement, Amendment, Countersigned Agreement, Internal Acknowledgment, Order Form, and SERU. Select the 'Add Document Type' link to add new document types.

- **Parent**: Identifies any parent document (ex. A parent document would be assigned when uploading an amendment).

- **Name:** The title of the document, usually taken directly from the license document (ex. Cambridge University Press Site License Agreement).
 
- **File:** Browse and upload a scanned copy of the actual document.

- **Archived:** Used to identify documents which are no longer current
or have been superseded by another agreement. Archived documents are
sorted separate from current documents and are collapsed beneath a
show/hide link to save screen space. Archiving a document does not
delete it from the system. It also does not delete any expressions
attached to that document.



### Editing Documents

Once added the documents will display on the Documents tab sorted
first by Document Type and then by signature date with most recent first.
Multiple signatures for both licensee and licensor can be added using
the ‘Add Signatures’ link. On the right side of the table are links to
view, edit, and delete each document. Now that the documents are
loaded, the next step is to begin adding Expressions. Please note that
Expressions are not required. You should however assign an appropriate
License Status to the record that indicates it is a document only
record.

### Adding Expressions

The Expressions tab is where the expressions or clauses of the license
are entered. You may enter any expression type that you wish. The
software comes with the following expression types already defined but
again the field is customizable and allows you to specify which expressions are internal and which expressions can be used for display.  

 Expression Types

- Authorized Users
- Confidentiality Clause
- Course Packs
- eReserves
- General Notes
- Interlibrary Loan
- Jurisdiction
- Multi-year Term
- Post Cancellation Access
- Third Party Archiving

### Adding Expressions


The ‘Add New Expression’ link opens the window below.  From this
window you can add expressions for the documents that have been
previously loaded.
![screenshot of the Expressions form.  There are 3 fields.](img/licensing/licensingAddNewExpression.png)

- **Document:** The document name for which you want to add a new expression. The drop-down is pre-populated from the existing document
names in the specific license record. This is a required field.
 
- **Expression Type:** The type of expression you wish to add
(interlibrary loan terms, course pack rights, etc). This is a required
field.  This is a customizable field.  You can add types by clicking on Add Expression Type or going to Admin.  
 
- **Qualifier:** This field will not be available if the selected expression type does not have a qualifier.  This is a customization field which can be used to qualify particular expressions. For example, a qualifier of 'Permitted' or 'Prohibited' may be appropriate for an interlibrary loan expression. You may choose to ignore this field as it may not be appropriate for certain expression types or choose to use it in a different fashion for other expression types.  The software comes with qualifiers added for Coursepacks and Interlibrary Loan.  


- **Document Text:** The actual text of the license clause. An
 interlibrary loan expression has been added in the following figure.


![screenshot of the ILL expression: document text, qualifier, and edit/remove links.](img/licensing/licensingAddILLExpression.png)

In this example, an Interlibrary Loan expression has been added along
with a snippet of the license text and a qualifier of *Permitted* has
been added noting that the item does allow for ILL. 

Actual legal text can be quite confusing so the next step is to add a
'Display Note' which can hold an interpretation of the text of the
clause that can be used for public display.

### Adding Display / Internal Notes

The ‘add/view display notes’ link opens a window which allows you to
enter multiple display notes. It also displays the Document Text on
that same window so that you can refer back to it while adding the
notes. The sort order of multiple display notes can also be adjusted
through this same window. The following figure shows a completed
Display Notes window.  **#  DISPLAY NOTES WINDOW IS FUNKY.  TAKE SCREENSHOT AFTER IT HAS BEEN FIXED!
 #**


There are two types of expression notes in CORAL Licensing: Display
Notes and Internal Notes. You can set the note type to either Internal
or Display for each expression type on the [ADD LINK]‘Admin’ page detailed later
in this document. The two note types (internal and display) were added
so that a distinction could be made between expressions and notes that
were intended to be displayed outside the module, for instance in one
of the Terms Tool, and those that were for internal use only. The
Display Notes which are intended to be shared have additional
functionality built in that the Internal Notes lack. In the following figure you will see the completed interlibrary loan expression.

![alt text](img/licensing/licensingInternalversusDisplayNote.png)

In this example the Interlibrary Loan expression type has been set to use Display Notes and as such the expression is presented with an
additional checkbox to the left of the Document Text. Internal Notes
do not receive this checkbox. When the licensing librarian or other
appropriate personnel has finished editing the expression
he/she can check this box which indicates that the expression is
finished and it makes the expression available through the [ADD LINK]*Terms Tool* Report* page. An email is then generated by the system indicating that a new expression has been completed and is ready for display. You can
edit the recipients of this email in the [LINK]*Admin* page.

If you choose not to use the *Terms Tool Report* page you may turn it
off as explained in the technical documentation guide. This will also
remove the display note checkbox and email functionality. It will also
remove the 'Terms Tool' tab which is explained next.


### Terms Tool

Once the expressions or terms of the license are known, the next
question to ask is ‘Which journals are covered by these terms?’.
That’s where the Terms Tool tab comes into play. The Terms Tool currently works only with the SFX link resolver.  It is true that not every institution uses SFX.  The SFX Links tab could be renamed and/or repurposed for use with  other openurl resolvers or journal management systems. 

Using this tab it is possible to relate a specific license to the covered journals in a specific SFX target or package. 

![alt text](img/licensing/licensingTermsTool.png)

In this example the Cambridge
University Press License Agreement is being associated with the
Cambridge Journals Online target in SFX (Cambridge Journals Online is
the SFX target public name). This SFX – License connection allows for
the delivery of license terms through the SFX menu as detailed in the
Terms Tool User Guide. This tab is meant to be used in conjunction with the Terms Tool and can be disabled along with the *Terms Tool Report* page for those who do not wish to use it.

### Attachments

For any resource there may be documents in addition to the actual
license that are important to retain. Title lists and email
correspondence are two that may be the most common. The Attachments
tab allows you to upload these additional documents to the license
record. 

The above figure shows an email that has been uploaded with
the date and a description of the file. In this case the attachment is
an email from the publisher detailing additional restrictions on the
resource. The date field is not automatically entered by the system so
it does not have to be the date the file was loaded into CORAL
Licensing. The intention of the date field was to be the date the
attached document was received but since the date is manually chosen
it can be any date of your choice. The ‘view attachment 1’ link will
open the uploaded file.

### Licenses in Progress

![alt text](img/licensing/licensingLicensesinProgress.png)

The *Licenses in Progress* page will show the licenses that are not
yet complete. It is intended to be used by the licensing staff as a
queue of outstanding licenses. It has been coded to show licenses of
status 'Awaiting Document' or 'Editing Expressions' and will also show new
licenses which have not yet been given any status. The hyperlinked
License Name will take you into the license record.

### Expression Comparison

*Expression Comparison* allows the user to see all the instances of a
specific expression type across all documents in a single screen or
view. The 'Limit by Expression Type' dropdown allows the user to
select from among all defined expression types. In the figure above
the display notes and document text have been removed for reasons of
confidentiality. In place of &lt; Display Notes removed &gt; and &lt;
Document Text removed &gt; users would see the actual notes and
document text that were entered. This allows licensing or relevant
personnel to compare language for each expression type across all
documents. It could be an immensely powerful tool when attempting to
come up with recommended language during negotiations. The user may
also add new display notes, open the license record and open the
actual document from this page.

*Expression Comparison* is intended for personnel that need quick
access to all expressions in the system. Other library staff however,
may only need access to specific types of expressions and this
particular page may be information overload. The *Terms Tool Report*
page was developed for these other users.

### Terms Tool Report

Once again the notes and document text have been removed from the
screenshot. *Terms Tool Report* provides access to only the
expressions using display notes and which have been identified as
being complete by the licensing librarian using the terms tool
checkbox mentioned earlier. As such it will not display unfinished
expressions which the licensing librarian may still be working on.
Another difference between *Terms Tool Report* and *Expression
Comparison* is that this page does not offer any links for editing the
record. While similar in function to *Expression Comparison* this page
was added in order to serve a user group which does not need the full
access provided by the *Expression Comparison* page.

The main points to remember for this page are that it displays
expressions which use display notes but only those that have been
approved for display. It is possible to turn off *Terms Tool Report*
and hide it from display if you do not wish to use it. Turning off the
*Terms Tool Report* will also disable the SFX Links tab on the license
record as well as the terms tool checkbox used to indicate that a
Display Note has been completed and approved for display. Please see
the Terms Tool User Guide for more information on how *Terms Tool
Report* can be used and on how it can be used to push out license
terms to other systems.

### Admin

The *Admin* page is where you will edit Document Types, Expression Types, Qualifiers, Signature Types, Licenses Statuses, and Calendar Settings.
Each of these fields can have as many values as needed so that the system can better meet local needs. 

*Admin* is also where you will edit and manage user permissions. CORAL Licensing has been built with the ability to limit access to select individuals given the confidential nature of license agreements. Users may not access CORAL Licensing until they are first set up with an account by an administrator. The following figure shows the ‘add new user’ window available from the *Admin* page.

![alt text](img/licensing/licensingAddNewUser.png)

**Login ID:**  The user’s unique ID.  If you're using your local campus's authentication system, the ID must match what is in there.  See the technical documentation for more
details on authentication.

**Privilege:** The user’s level of access.  

- Admin users have complete add/edit rights and can remove licenses and associated fields.  They also have access to the *Admin* page, the Terms Tool tab on the license record and the terms tool checkbox. 
 
- Add/Edit users can remove licenses and associated fields, but not have access to the Admin page and the Terms Tool.  

- View Only users can view all license information and are allowed access to the uploaded documents.

- Restricted users can view all license information but are not allowed access to the uploaded documents nor access the actual license agreements that have been uploaded to the system.  
  

**Terms Tool Email:** Enter email address if you wish the user to
receive email notification when the terms tool box is checked for a
given expression. Leave this blank for all others.

