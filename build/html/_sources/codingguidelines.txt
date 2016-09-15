Coding Guidelines
-----------------

This page lists the CORAL coding guidelines. It's shared between all modules, so these rules apply for all of them.

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