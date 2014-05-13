TinyMCE4XOOPS 2.0 - 2014/03/28
by Alain01

TinyMCE4

1 - copy both directories "class" + "uploads" to the root path web of XOOPS.
2 - Update the system module
3 - Go to "control panel" / "Preferences" / "System Module Settings"
4 - Modify the "Editor Settings" for "blocks" / "comments" / "all modules" as you want
5 - For somes modules, then go to the preferences option and choose the editor

If your web site is not in the root path (like http://myxoops/mywebsite.com), please modify 2 files : 

- (...)/uploads/filemanager/templates/liste-templates.js (url lines)
- (...)/uploads/filemanager/templates/template-video/video.html (src lines)

If you change the language to another language than english (en) or french (fr), e.g. to german (de), than you have to do following:
1) create language file "german.php" in \tinymce4\language\ 
a) the file name must be the same as language in xoops settings
b) in this file you must define the language code: define("_XOOPS_EDITOR_TINYMCE4_LANGUAGE","de");
c) this language code must be the same as the name of the language files himself, e.g. "de" -> de.js

2) check, whether your language files are existing:
a) \tinymce4\tinymce\js\tinymce\langs\de.js
b) \tinymce4\external_plugins\codemirror\langs\de.js
c) \tinymce4\external_plugins\youtube\langs\de.js

Enjoy !

To DO : 
- Add class name to images
- Add XOOPS Imagesmanager
- Add XOOPS emoticon


Changelog :

Changes in TinyMCE4XOOPS 2.0 (2014/03/28)
- Updated TinyMCE V4.0.11 to V4.0.20
- Updated Responsivefilemanager 9.3.0 to 9.4.0
- Add index.html files in all directories
- Bugfixes : path in XOOPSQuote, XOOPSCode, and QRcode
- Add plugin Codemirror (thanks to andrey3761)
- Add many languages
- blue colorisation for XOOPSQuote, XOOPSCode and ExtGallery


Changes in TinyMCE4XOOPS 1.14 (2013/12/11)
- Updated TinyMCE V4.0.10 to V4.0.11
- Updated Responsivefilemanager 9.2.0 to 9.3.0
- Modify the toolbars (moved right the format and paragraph button)
- Bug $chemin_array['path'] in tinymce.php and /external_plugins/filemanager/config/config.php
- Bug session in /external_plugins/filemanager/config/config.php