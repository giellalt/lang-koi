=================================== !
The Komi-Permyak morphophonological/twolc rules file 
=================================== !

This file documents the [phonology.twolc file](http://github.com/giellalt/lang-koi/blob/main/src/fst/phonology.twolc) 

## Alphabet, Sets and Definitions


## Letters of the alphabet

* а б в г д е ё ж з и і й к л м н о ӧ п р с т у ф х ц ч ш щ ъ ы ь э ю я 
* А Б В Г Д Е Ё Ж З И І Й К Л М Н О Ӧ П Р С Т У Ф Х Ц Ч Ш Щ Ъ Ы Ь Э Ю Я 

## Archiphonemes for vowels
## Triggers
* %^1Cns:0    Plural-initial; it allows for doubling of consonant

* %^LVBound:0     boundary for LV change instead of Consonant or end of word
* %^VowRM:0       vowel syncope

## Boundary symbols

*  %>  morpheme boundary
* hash # word boundary
*  %-  
 »7      * »
 «7      * «
 %[%>%]  * > (escaped with square brackets, to avoid collision with > as morpheme boundary)
 %[%<%]  * < (escaped with square brackets, to avoid collision with < as morpheme boundary)

Diacritics




## Sets 

Vowel

Palatal Vowel
Cns-initial vowels

All non-vowels, consonants and hard and soft signs

All non-vowels with exception of soft sign

All consonants with hard A

All consonants followed by Cyrillic и
Why is т2 here 2015-10-01


Letters

Dummy


## Definitions



## Rules


**Double stem-final consonant**


**Double stem-final consonant л:в**


**%^1Cns to zero**

**э:е**



**The famous L/V**

Paragogic consonants
**mDeletion**

Paragogic consonants
**tDeletion**


**jDeletion after vowel**

**j to hard sign after consonant**
* *кывй%>а#*
* *кывъ%>я#*
* *кӧсй%>а#*
* *кӧсъ%>я#*

**l deletion**

**d deletion**

Vowel Palatalisation
**а 2 я, о 2 ё, у 2 ю**
* *вой%>ас*
* *во0%>яс*
* *озй%>ас*
* *озъ%>яс*
* *ворссь%>а#*
* *ворсс0%>я#*
картопель+Sg+Ine+PxSg3
* *картопель%>ас*
* *картопел0%>яс*
картопель+Pl+Nom
* *картопель%>ъяс*
* *картопел0%>0яс*

**%{иі%} 2 і**



**%{иі%} 2 и**
* *ворссь%>%{иі%}#*
* *ворсс0%>и#*
* *ло%>%{иі%}#*
* *ло%>и#*
* *шу%>%{иі%}с*
* *шу%>ис*
* *вай%>%{иі%}с*
* *вай%>ис*

**%{ая%} 2 а**
* *ло%>%{ая%}#*
* *ло%>а#*
* *шу%>%{ая%}с*
* *шу%>ас*



**%{ая%} 2 я**
* *ворссь%>%{ая%}#*
* *ворсс0%>я#*
* *вай%>%{ая%}с*
* *вай%>яс*


**Soft Sign Deletion**
* *нянь%>%^1Cnsэз*
* *нян0%>нез*

* *велӧдысь%>сянь*
* *велӧдыс0%>сянь*
* *велӧдысь%>сьыс*
* *велӧдыс0%>сьыс*

**Hard Sign Deletion**
* *вой%>ъяс*
* *вой%>0яс*
* *выль%>ъяс*
* *выль%>0яс*
* *коми%>ъяс*
* *коми%>0яс*
* *автобус%>ъяс*
* *автобус%>ъяс*
* ★*автобус%>0яс* (is not standard language)

**Hard Sign Palatalization**
* *виддз%>ъяс*
* *вид0з%>ьяс*

**No triple letters**
* *класс%>сянь*
* *клас0%>сянь*
* *Блатт%>тӧг*
* *Блат0%>тӧг*
* *металл%>лӧн*
* *метал0%>лӧн*

**IClitic**


* * *
<small>This (part of) documentation was generated from [../src/fst/phonology.twolc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/phonology.twolc)</small>