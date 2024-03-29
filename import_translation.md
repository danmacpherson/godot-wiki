## Importing Translations

#### Games and Internationalization

The world is full of different markets and cultures and, to maximize profits(tm), nowadays games are released in several languages. To solve this, internationalized text must be supported in any modern game engine.

In regular desktop or mobile applications, internationalized text is usually located in resource files (or .po files for GNU stuff). Games, however, can use several orders of magnitude more text than applications, so they must support efficient methods for dealing with loads of multi-language text.

There are two approaches to generate multi language games and applications. Both are based on a key:value system. The first is to use one of the languages as key (usually english), the second is to use a specific identifier. The first approach is probably easier for development if a game is released first in english, later in other languages, but a complete nightmare if working with many languages at the same time.

In general, games use the second approach and a unique ID is used for each string. This allows to revise the text while it's being translated to others. the unique ID can be a number, a string, or a string with a number (it's just a unique string anyway). 

Translators also, most of the time prefer to work with spreadsheets (either as a Microsoft Excel file or a shared Google Spreadsheet).

#### Translation Format

To complete the picture and allow efficient support for translations, Godot has a special importer that can read .csv files. Both Microsoft Excel and Google Spreadsheet can export to this format, so the only requirement is that the files have a special format. The csv files must be saved in utf-8 encoding and the format is as follows:

|     | <lang1> | <lang2> | <langN> | 
| ---- | ----------- | ----------- | ----------- | 
| KEY1 | string | string |string |
| KEY2 | string | string |string |
| KEYN | string | string |string |

The "lang" tags must represent a language, it must be one of the [valid locales](locales) supported by the engine. The "KEY" tags must be unique and represent a string universally (they are usually in uppercase, to differentiate from other strings). Here's an example:


|  en | es | ja | 
| --- | --- | --- | --- | 
| GREET | Hello, friend! | Hola, Amigo! | こんにちは |
| ASK | How are you?| Cómo esta?| 元気ですか |      
| BYE | Good Bye| Adiós | さようなら |               

#### Import Dialog

The import dialog takes a .csv file in the previously described format and generates several compressed translation resource files inside the project.

Selecting a .csv file autodetects the languages from the first row. and determines which column represents which language. It is possible to change that manually, by selecting the language for each column.

<p align="center"><img src="images/trans.png"></p>

The import dialog also can add the translation to the list of translations to load when the game runs, specified in engine.cfg (or the project properties). Godot allows to load and remove translations at runtime, too.

 --- //[Juan Linietsky](reduzio@gmail.com) 2013/11/10 21:42//
 
