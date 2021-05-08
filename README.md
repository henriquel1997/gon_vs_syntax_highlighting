# gon_vs_syntax_highlighting
Visual Studio syntax highlighting plugin for GON (Glaiel Object Notation) https://github.com/TylerGlaiel/GON

# About
The Visual Studio project for the plugin is in the folder "VSLanguageHighlight". To build it, just open the solution and build as any other project.
The compiled plugin can be found in the "bin/Debug" folder and can be installed by running the "VSLanguageHighlight.vsix" file located there.

For more information on how to use this project, refer to this tutorial: https://www.youtube.com/watch?v=5LaVcOP2X4g

# Structure
The plugin is compiled based on the "Language.plist" file, located in the "Syntaxes" folder, it is Textmate Grammar especification generated using Iro (https://eeyo.io/iro/), which is a grammar editor for syntax highlighting.

The source Iro source code is located in the root of this project in a file named "gon_grammar.iro". To open it in the Iro editor, copy its text contents and paste it in the Iro editor.
Iro can be used as an editor and a debugger for the syntax highlighting. 
You can find an introduction to it here: https://medium.com/@model_train/creating-universal-syntax-highlighters-with-iro-549501698fd2
And the documentation here: https://eeyo.io/iro/documentation/

# Modifying
In the Iro code, you can find two main sections, Styles and Context. Styles defines what each token looks like, and Context is the grammar.
Let's say you want to modify what an object field name looks like. You can find "object_field" in the styles and change it's textmate_scope value. There is also a color value in each style, but it is only used for the Iro preview, it has no effect in the final Textmate Grammar.

There's a set of valid values that can be used for the textmate_scope, they are listed both in the Iro documentation https://eeyo.io/iro/documentation/#TextmateAtomAceScopes and also in the Textmate Documentation (Section 12.4): https://macromates.com/manual/en/language_grammars
