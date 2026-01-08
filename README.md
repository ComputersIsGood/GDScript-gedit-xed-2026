Updated GDScript Language for GTKSourceViewer-Based Text Editors (xed, gedit)
==============
I use this file in the Xed text editor (default text editor for Linux Mint), which uses GTKSourceViewer for styles.  
I don't know if it will work in other editors, but I believe it should work on any editor which uses GTKSourceViewer (gedit apparently).  
  
This is an update of @haimat and @iatenine's [*GDScript* syntax definition for the gedit text editor](https://github.com/haimat/GDScript-gedit).  
GDScript is the scripting language for the [Godot Game Engine](http://www.godotengine.org/).  

  
Installation
------------
Copy *gdscript451.lang* into your */usr/share/gtksourceview-4/language-specs* directory. (your gtksourceview-# version might differ, use most recent version you have)  

*GDScript 4.5.1* should now appear in your editor as a selectable language.  

Modification
------------
It is surprisingly simple to modify the file yourself, take a shot at changing styles or adding expressions if you want to tweak anything!  

My understanding is: 
- The text editor's style file (/usr/share/gtksourceview-4/styles) defines styles for certain \<style-ref\> in this .lang file  
- GTKSourceViewer defines "fallback" styles for some types, which is why they are colored even if the stlye file does not mention them  
    - I couldn't find a full list, but quite a few were already added in the \<styles\> section (line 30)  
  
Be careful when Editing the id in \<language\>. If you change the id at the top of the file (gdscript451), the whole file will break unless you change   every other instance of gdscript451 to the same thing.  
  
Disclaimers / Notes
------------
I am a noob at Github, GDScript, and formatting xml files;  
I couldn't find any more recent .lang file for GDScript in GTKSourceViewer, so I took a shot at making my own update;  
I simply wanted more GDScript keywords and expressions to light up nicely in the text editor that came with my linux distro, which it now seems to do correctly, but I cannot guarantee anything past that :)  

Additions to haimat's Version
------------
- Highlight Keywords in comments ([See comments section](https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/gdscript_basics.html))
- Recognition for @,&,$,^,% as markers of function shorthands
- Recognition of CONSTANTs, _functions
- Recognition of all classes
- Recognition of more keywords
- Recognition of more built-in functions
  

Hopefully someone else finds this useful!
