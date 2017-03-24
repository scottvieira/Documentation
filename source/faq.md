FAQ
---

### General

**Restarting Workflows**

**Question:** My intention was to set up a workflow for renewals that could be completed and then restarted the next year. We’ve been able to set up and successfully use a workflow for this, but I don’t see any way to begin it again in subsequent years. Am I missing something or are the workflows only set up to be once and done?

**Answer:** This is a known difference between how the system was designed and how many people are using it.

Two workarounds:

First, there is the technical way: “If you have access to the databases, using mysql you can change the statusID number.
update Resource set statusID = '1' where resourceID=NNN;
I believe "1" is not complete and "2" is complete. You'd need to use the resourceID of your resource. You can find that in the url of the resource page. ” (from an email Kelly Drake sent on May 19, 2014)

Second, there is the non-technical way: Until the last step in your workflow has been marked as complete, you can click “restart workflow.” People simply leave the last step incomplete until the next year, then click “restart workflow.”

### Installation

**Question:** Why am I getting the following series of "Notice" messages or warnings when I install CORAL?  

For example:

> -- Notice: Undefined index: orderBy in C:\xampp\htdocs\coral\resources\admin\classes\domain\Resource.php on line 805
> 
> -- Notice: Undefined index: page in C:\xampp\htdocs\coral\resources\admin\classes\domain\Resource.php on line 805
> 
> -- Notice: Undefined index: recordsPerPage in C:\xampp\htdocs\coral\resources\admin\classes\domain\Resource.php on line 805
> 
> -- Notice: Undefined variable: currentPage in C:\xampp\htdocs\coral\resources\index.php on line 32


**Answer:** The messages are low level warnings from PHP and usually do not signify anything serious. Generally, best practices for PHP dictates variable are defined. The CORAL Steering Committee is aware of this and has this issue listed for correction. However, if you are seeing these messages in your CORAL pages, you should be concerned that your server is configured to show all server error messages on the page that is being loaded, which could allow malicious users to gain insight into your vulnerabilities. You should change your PHP settings in php.ini to disable that display for any production instances. Change display_errors = On to display_errors = Off and restart Apache. 

### Technical



