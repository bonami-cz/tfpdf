tFPDF

Informations
Author: Ian Back
License: LGPL
Description: This class is a modified version of FPDF that adds UTF-8 support. Moreover, it embeds only the necessary parts of the fonts that are used in the document, making the file size much smaller than if the whole fonts were embedded. These features were originally developed for the mPDF project.

To use a Unicode font in your script, pass the font file name as third parameter of AddFont() and true as fourth parameter. The font may be located either in the font/unifont directory or directly in the system font folder (in case the _SYSTEM_TTFONTS constant is defined). The package ships with the DejaVu font family.

Note: this class requires the mbstring extension.

tFPDF accepts UTF-8 encoded text. It embeds font subsets allowing small PDF files.

It requires a folder 'unifont' as a subfolder of the 'font' folder.

You should make the 'unifont' folder writeable (CHMOD 755 or 644). Although this
is not essential, it allows caching of the font metrics the first time a font is used,
making subsequent uses much faster.

All tFPDF requires is a .ttf TrueType font file. The file should be placed in the
'unifont' directory. Optionally, you can also define the path to your system fonts e.g. 'C:\Windows\Font'
(see the example ex.php file) and reference TrueType fonts in this directory.

Pass a fourth parameter as true when calling AddFont(), and use utf-8 encoded text
when using Write() etc.

