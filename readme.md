# apmuthu fork notes
Differences with upstream master codebasewhich exclusively includes the following files apart from mods needed for them:
1. si_cron script used for recurring invoice generation in linux
2. [PHPCAPTCHA](http://www.phpcaptcha.org) and hooks for it for login (set in config/defines.php)
3. Fully RDBMS compliant with no need for si_index table
4. include/sql_patches.php has all needed patches enabled
5. Releases of this fork do not contain the [Zend](https://github.com/dmelo/Zend-1.11/archive/27d7f1b3f45a436a9c795881db1d41689b8f9224.zip) library which must be separately downloaded and extracted into the library/Zend folder.
6. If CAPTCHA feature is to be enabled, then follow instructions in the [securimage-readme.txt file](https://github.com/apmuthu/simpleinvoices/blob/master/library/securimage/securimage-readme.txt) in the <b>library/securimage</b> folder.
# Simple Invoices
Making invoicing rock since '05.

## Cloning
SimpleInvoices using gitsubmodules to load the Zend Framework.  
When cloning the repository use the `--recursive` option to ensure that Zend is retrieved.  
Upstream: `git clone --recursive git@github.com:simpleinvoices/simpleinvoices.git`
This fork: `git clone --recursive git@github.com:apmuthu/simpleinvoices.git`

## Downloads
* Bleeding Edge Code: [SI Git Master](http://github.com/simpleinvoices/simpleinvoices/archive/master.zip) (.zip)
* Latest Beta Release: [2013.1 beta 7](http://download.simpleinvoices.org/simpleinvoices/downloads/simpleinvoices.2013.1.beta.7.zip) (.zip)
* Latest Stable Release: [2011.1](http://download.simpleinvoices.org/simpleinvoices/downloads/simpleinvoices.2011.1.zip) (.zip)

## Documentation
* Installation: http://simpleinvoices.org/install
* Frequently Asked Questions: http://simpleinvoices.org/wiki/faqs
* Help: http://simpleinvoices.org/help

## Schema
* The Entity Relationship Diagram for SI is available in the <b>databases/mysql folder</b>
* [ERD Schema with Primary and Foreign Keys](https://github.com/apmuthu/simpleinvoices/raw/master/databases/mysql/SI_Schema_2013.1.beta.5.1_PKFK.png)

## About
* Simple Invoices is released under the GPL v3 license - refer license.txt for details
* For installation instructions refer: http://simpleinvoices.org/install
* For any other help or comments jump on our website or post on the forum at http://simpleinvoices.org/forum

## Get Involved
* Developer Discussion: [Simple Invoices Google+ Community](https://plus.google.com/communities/102476804981627142204)
* Developer Mailing List: [Simple Invoices Google Groups](https://groups.google.com/forum/#!forum/simpleinvoices)

We also have a mailing list for tracking commit activity. This is hosted on Google Groups. You can find it here: https://groups.google.com/forum/?fromgroups#!forum/simpleinvoices-trac


## Translations
We are proud that SimpleInvoices is currently available in 25 different languages but we would love for that number to be even bigger!  

If you would like to help translate SimpleInvoices into your language check out our [translation project](https://www.transifex.com/projects/p/SimpleInvoices/).

For more information refer: [simpleinvoices.org/translate](http://www.simpleinvoices.org/translate)


## Reporting Bugs
Please use the issue tracker on GitHub when reporting bugs.
https://github.com/simpleinvoices/simpleinvoices/issues

**Developers**: There are still a number of open issues on the old Google Code issue tracker if you are looking for something to fix. http://code.google.com/p/simpleinvoices/issues/list

## Known Issues
* **Heart Internet Users** -- There is currently an issue with exporting invoices to PDF. Images are not currently being rendered in the PDF. We are working on resolving this issue but unfortunately we do not yet have a fix. We recommend that you use a different hosting service if you need to export PDF invoices.
