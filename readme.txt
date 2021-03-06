=== Plugin Name ===
Contributors: bpiwowar
Tags: formatting, bibtex
Requires at least: 2.7
Tested up to: 3.1.1
Stable tag: 0.3.14

papercite helps to format bibtex entries to display a bibliography or
cite papers.

== Description ==

papercite format bibtex entries as HTML so they can be inserted in
WordPress pages and posts. The input data is a bibtex file (either
local or remote) and entries can be formatted by default using various 
predefined styles. Bibtex source file and a link to the publication
are also available from the HTML. 

Features:

* Input data directly from the bibtex text file
* Source files can be URL (e.g., from citeulike.org and bibsonomy.org)
* Template based HTML generation
* Possibility of filtering the bibtex entries based on their type (allow, deny)
* Possibility to access the single bibtex entry source code to enable copy&paste (toggle-enabled visualization)
* Possibility of editing the bibtex file directly from the wordpress administration page
* Adds the possibility of writing a text with references to a bibtex entries, and to print the bibliography at the end.
* Auto-detection of PDF files based on the BibTeX key
* Publications can be grouped and sorted in various ways

The papercite plugin has been developed and tested under Wordpress
3.1. Versions before 0.3 were based on bib2html version 0.9.3.

**Documentation can be found from within WordPress plugin list (click on
the documentation link)**. You can see the documentation of the plugin
as installed on my site <a href="http://www.bpiwowar.net/wp-content/plugins/papercite/documentation/index.html">here</a>. 

To report bugs or request features, please navigate to 
https://github.com/bpiwowar/papercite

== Installation ==

Follow these step or use the plugin installer from WordPress to
install papercite:

1. download the zip file and extract the content of the zip file into a local folder
2. upload the folder papercite into your wp-content/plugins/ directory
3. log in the wordpress administration page and access the Plugins
menu

Then, you should activate papercite, and follow the instructions
given in the *documentation* that you can access through the plugin
list (click on the documentation link).

== Frequently Asked Questions ==

= Where is the documentation? =

The documentation is now bundled with the plug-in. Go to the plug-in
list page in the WordPress dashboard, and click on the documentation link.

= How can I edit my bibtex files? =

If your file is local to the blog installation, you have two options:

- via FTP client with text editor
- via Wordpress Admin interface: Manage->Files->Other Files

-- use wp-content/papercite-data/bib/mybibfile.bib as a path

Alternatively, you can maintain your updated biblilography by using systems such as citeulike.org and bibsonomy.org; 
specify the bib file using as a URL (e.g., in citeulike, you should use http://www.citeulike.org/bibtex/user/username)

= How are the entries sorted? =

Entries are sorted by year by default.

= How can I personalize the HTML rendering? =

The HTML rendering is isolated in two template files, located in the
subfolders tpl (citation list rendering) and format (entry rendering).

== Screenshots ==

1. With the bibshow & bibcite commands
2. With the bibtex command

== Changelog ==

= 0.3.14 =
  * The HTML code produced has been cleaned up (valid HTML) [bug 28]
= 0.3.13 =
  * Enhancement (bug 26): several bibtex files can be given
  * New (optional) bibtex parser handles larger bibtex files (bug 23) 
  * Master thesis is now properly handled (bug 27)
= 0.3.12 =
  * Fix missing <?php (bug 24 and 25)
= 0.3.11 =
  * Fix a bug introduced in 0.3.10
= 0.3.10 =
  * Multiple authors in bibcite (enhancement #2)
  * Ignores @comment entries generated by jabref (bug 22) 
  * Updated the documentation (for the new entry formats, and the
  extensions to bib2tpl)
= 0.3.9 =
  * Adopted patch given in bug 18 (bibtex source formatting)
  * Fixed function name conflict with Simple Google Analytics plug-in
  (bug 19)
= 0.3.8 =
  * Fixed bug 14 (group_order not working)
  * Used the proposed enhancement (bug 13) of the function _e2mn
  (parsing a month)
  * Improved bibtex parsing (\&)
  * Improved the entry templates
  * Now uses OSBib for pages formatting
= 0.3.7 =
  * Improved the OSBib conversion for entry format - now close to perfect
= 0.3.6 =
  * Bug fix when there are only two authors in the entry
  * Bug fix on nested conditions in templates
= 0.3.5 =
  * Author are formatted according to the entry template converted
  from OSBib
= 0.3.4 =
  * Formats are back, translated from OSBib (not perfect, but close to
  the output in version prior to 0.3.0
  * More latex accents handled
= 0.3.3 =
  * Fixed bug 7: umlaut (still) not handled
  * Fixed bug 12: bug with remote URLs
= 0.3.2 =
  * Entry format is now in XML to ease the edition
= 0.3.1 =
  * Fixed bug 7: umlaut not handled
  * Fixed bug 9: template option does nothing for bibshow
  * Bug fix on sort options
  * Sort by author now working
= 0.3.0 = 
  * Complete code overhaul - switched to a new bibtex / template
  system
  * New options to sort & group entries
  * Preference system to set defaults
  * New template based system for entry customisation
  * Multi-site support
= 0.2.14 = 
  * Grouped by year option (patch due to S. Aiche)
  * Now generates an id which does not depend on the key (fix javascript related bugs)
= 0.2.13 = 
  * bug fix: wrong mappings from bibtex fields to arrays have been corrected, link to pdf is now working properly, polish characters
  are almost properly handled (thanks to Łukasz Radliński)
= 0.2.11 =
  * bug fix: name clash was preventing insertion of medias using the
  WP dialogs
= 0.2.10 =
  * papercite now looks in the pdf directory at two levels
    (wp-content,  and wp-content/plugins)
= 0.2.9 =
  * Small bug fix (removes a warning)
= 0.2.8 =
  * Documentation update
  * New parameter `format`
 = 0.2.5 =
  * Fixed a bug with the allow filter
= 0.2.4 =
  * Small bug fixes (if the file is an URL) and use of WP functions to
  retrieve remote data (useful when you have proxies)
= 0.2.3 =
 * Fixed a bug introduced in 0.2.2
 * Changed the default folder for data in order to avoid data loss
 when upgrading
 * Finished the encapsulation of all the code, so as to prevent name
 clash with wordpress and/or other plugins
= 0.2.2 =
 * Removed PHP 5 specific code
= 0.2.1 =
 * Added the template file
= 0.2 =
 * Added deny/allow parameters to [bibtex] so the plugin can replace bib2html
= 0.1 =
 * Adapted the plugin from bib2html 0.9.3
 * Added the bibshow and bibcite commands

== Upgrade Notice ==

= 0.3.14 =
If you have custom templates, please read. The template generation has been slightly modified - you have to
explicitely markup paragraphs and line breaks, since papercite now
removes any \n or \r in the templates to avoid clashes with WordPress.
= 0.3.13 =
Bug fixes and new experimental parser (disabled by default) to handle
bibtex files faster (useful for large bibtex files)
= 0.3.11 =
Should be the last stable release before the 0.4.0 and CoINS support
= 0.3.5 =
Compatibility with version prior to 0.3.0 is now almost completed. Users who
want to use the new grouping, sorting or template functionalities are advised
to upgrade to this version.
= 0.3.0 = 
Complete overhaul of the bibtex/template system, with a lot of new
options. Please wait until version
0.3.1 if you want to be sure of a bug free papercite (it should not
break WordPress though). Please note that there is
only one citation format (IEEE) and that is only a partial implementation.
= 0.2.9 = 
Removed a PHP warning with bibshow
= 0.2.8 =
Introduced the `format` parameter to format the entries
= 0.2.5 =
Bug fix - all users should upgrade
= 0.2.4 =
Users using remote URLs for their bibliography should upgrade
= 0.2.3 =
All users must upgrade to this version - Please read the information
about the new location of bibtex and pdfs.
= 0.2.2 =
Users using PHP 4 should upgrade
= 0.2.1 = 
All users should upgrade - plugin was broken until now
= 0.2 =
All bib2html users should at least use this version so they don't break their installation
= 0.1 =
First version

