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

**Question:** How do I install CORAL 2.0.x on Ubuntu 14?

**Answer:** Check out the [State of Libraria blog](http://stateoflibraria.com/2017/02/23/coral-2-on-ubuntu-14/), which has written up a nice post on installing CORAL 2 on Ubuntu 14.


**Question:** I subscribe to ERM through SirsiDynix and was wondering if there is a way to change the settings so that the database doesn’t “time out” so frequently?  

**Answer:** There is a way to help fix the problem via a timeout variable in the configuration.ini for the Auth module. An example of the file is copied and pasted below. The variable is highlighted in bold red. The installation process for CORAL will prompt you to change the default, but there is no end user way to update the value after the installation process is complete, unless you or IT support (or SirsiDynix?) can manually access and edit the file. The value is in seconds.

> [settings]

> timeout=3600

> [database]

> type = "mysql"

> host = "localhost"

> name = "coral_auth_prod"

> username = "root"

> password = "mysql"

### Technical

<<<iiii

