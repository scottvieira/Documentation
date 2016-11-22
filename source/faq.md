FAQ
---

### General

**Restarting Workflows**

Question: My intention was to set up a workflow for renewals that could be completed and then restarted the next year. We’ve been able to set up and successfully use a workflow for this, but I don’t see any way to begin it again in subsequent years. Am I missing something or are the workflows only set up to be once and done?

Answer: This is a known difference between how the system was designed and how many people are using it.

Two workarounds:

First, there is the technical way: “If you have access to the databases, using mysql you can change the statusID number.
update Resource set statusID = '1' where resourceID=NNN;
I believe "1" is not complete and "2" is complete. You'd need to use the resourceID of your resource. You can find that in the url of the resource page. ” (from an email Kelly Drake sent on May 19, 2014)

Second, there is the non-technical way: Until the last step in your workflow has been marked as complete, you can click “restart workflow.” People simply leave the last step incomplete until the next year, then click “restart workflow.”

### Installation

### Technical



