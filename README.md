# icelandic_spellcheck_markdown_quest 


A search for the best spell checking tools for the Icelandic language.

![is_ISbdic](is_bdic.png)

I frequently use markdown to document, project manage and plan things. Having a good spell checker is essential since I have no problem making spelling errors.
Of all the editors out there, [Marktext](https://www.marktext.cc/) has become a favorite. It comes with a nice English spell check but is lacking the Icelandic language.
Marktext both has a hunspell and system spell checker for Windows and macOS but the Icelandic languages package does not work. 
For way too long have I just copied the text in and out of google drive to do the spell check so I want to find another way.

## Research
I did a Quick search on the internet for hunspell, .aff, .dic and .bdic and almost everything I found was about 5 years old. Including interviews on [RÚV](https://www.ruv.is/frettir/innlent/vantar-rafraen-gogn-um-islenska-tungu) talking about the lack of data for the Icelandic language. I’m not sure if that’s because we just gave up or there is something new out there.

I found out that the markdown editor that I was using [Ghostwriter](https://ghostwriter.kde.org/) and [Typora](https://typora.io/) were using **.aff** and **.dic** for their spell checking. Below is a table of the **.aff** and **.dic** files I found online.

| name                                                                      | note                                                        |
| ------------------------------------------------------------------------- | ----------------------------------------------------------- |
| [titoBouzout/Dictionaries](https://github.com/titoBouzout/Dictionaries)   | worked fine for ghostwrited but not when converted to .bdic |
| [hunspell-is](https://github.com/nifgraup/hunspell-is)                    | Couldn't figure out how to use it                           |
| [LibreOffice](https://github.com/LibreOffice/dictionaries/tree/master/is) | Used to make the .bdic                                      |

### formats and terms

- [Hunspell](https://en.wikipedia.org/wiki/Hunspell) : Spell checker
- [Ispell](https://en.wikipedia.org/wiki/Ispell) : spell checker
- **.aff** file: grammar rule files
- **.dic** file: dictinary file with a wordlist
- **.bdic** file: binary dictinary file that also inclueds grammar rules

## The build

![bdic_gen.png](images/bdic_gen.png)

After being unsuccessful in finding a **.bdic** file for Marktext I found a generator that makes one from **.aff**, **.dic** and **.dic_delta**. I couldn't find or understand the **.dic_delta** and it generated the file even if it was missing. I had to do it using Linux and it was well documented and I didn't have any troubles.

[convert-dict-tool-from-chromium](https://github.com/jankelemen/convert-dict-tool-from-chromium)

To add it to Marktext simply add it to the dictionary folder and change the spell settings to use hunspell.
C:\Users\%user%\AppData\Roaming\marktext\dictionaries

![bdic_file.png](images/bdic_file.png)

## Conclusion

It works well now It's missing some words but I can add them over time and Marktext generates a **.json** file so it's easy to keep track of it and I might update it here from time to time. 

![add_json.png](images/add_json.png)


![spellcheck_working.png](images/spellcheck_working.png)


![spellcheck_working.png](images/is_bdic.png)
