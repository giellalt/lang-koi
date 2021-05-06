This is where new words are added as lexc entries before they are 
added to the xml source files.
Абъячой+N+Prop+Sem/Plc:Абъячой PROP_ "(eng) fish/(fin) /(rus)" ;


ADD NOUNS BELOW






This is where new words from kpv are initially shown








This is where new words from kpv are initially shown




Nouns
Nouns in the Komi Permyak language are things.






This is where new words from kpv are initially shown

2016-07-14







Numerals
Numerals in the KOMI-PERMYAK language are numbers.




This is where new words from kpv are initially shown



This is where new words from kpv are initially shown





These are koi verbs



Adjectives
Adjectives in Komi-Permyak language describe things.



Pronouns
Pronouns in KOMI PERMYAK language are references to things.



This is where new words from kpv are initially shown







=================================== !
The Komi-Permyak morphophonological/twolc rules file !
=================================== !


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
 »7       * »
 «7       * «
 %[%>%]   * > (escaped with square brackets, to avoid collision with > as morpheme boundary)
 %[%<%]   * < (escaped with square brackets, to avoid collision with < as morpheme boundary)

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



# Symbol affixes






# Noun morphological lexica !


 * **LEXICON Vocative**

 * **LEXICON Noun1-IS_PTC-OM** is to provide deverbal nouns with +Der/ӧм tags

 * **LEXICON Noun1-IS_PTC-AN**

 * **LEXICON Noun1-IS_PTC-YSJ**








Basic nouns.

The lexicon for basic nouns is N_ 





This should be phased out 2013-05-07









subsequent Cns vs Vow
 * LEXICON N_PARAGOGIC-V/L  ныв:ны нылыс


 * LEXICON N_PARAGOGIC-J  ав:ав авйыс

 * LEXICON N_PARAGOGIC-K  кытш:кытш кытшкыс

 * LEXICON N_PARAGOGIC-M  зон:зон зонмыс

 * LEXICON N_PARAGOGIC-T  зеп:зеп зептыс

 * LEXICON N_END-IN-J  абай:аба абайыс

 * LEXICON N_END-IN-ДДЬ  автомобиль:автомобил автомобильыс
 * +Pl:%>%^1Cnsэз CASEPOSSLEX ;  2015-09-04 change to ь%>яс after xfst rules are removed

 * LEXICON N_END-IN-ДДЗ  автомобиль:автомобил автомобильыс

 * LEXICON N_END-IN-ЛЛЬ  моль:мол молльӧ
2015-09-04 change to ь%>яс after xfst rules are removed

 * LEXICON N_END-IN-Ч/ДЗ  автомобиль:автомобил автомобильыс
 * LEXICON NMN_END-IN-Ч/ДЗ  автомобиль:автомобил автомобильыс
















## Inflectional lexica 


All nouns follow one contlex "N_"
to begin with here is simply a list of all variant
with no more variants beyond:



 * **LEXICON CASEPOSSLEX**



SG1

SG2


SG3

PL1


PL2
PL3


SG1
SG2
SG3
PL1
PL2
PL3

SG1
SG2
SG3
PL1
PL2
PL3



SG1

SG2

SG3

PL1

PL2
PL3


## Case followed by possible clitic






















## Case followed by word end




































2012-02-07 !!+Der/A+Adv:%>а K ;








# Numeral morphological lexica 











LEXICON NUM-APPR ! 2011-11-03 This will need work



## Inflectional lexica 

All nouns follow one contlex "Noun1"
to begin with here is simply a list of all variant
with no more variants beyond:
















































## Arabic numerals



 * **LEXICON ARABIC          ** 








# Adverb inflection
----
Komi adverbs inflect for direction.






















 * **LEXICON ADV-SPAT  **
these are adverbs in spatial cases
and they probably are equivalent in morphology to postpositions






























Proper noun inflection

Komi proper nouns inflect in the same cases as regular
nouns.






Russian type Surnames 

Preparing for the template urj-Cyrl
Beginning 2012-11-15





 * :2 PropSur-kal ;  These are foreign Л words



Абдеев:Абдеев

Багрий:Багр


Аморский:Аморск



PLACE NAMES FROM TEMPLATES !!




These are vowel-final stems
They have previously received +Sem/Fem tags







Should this be limited to +Sg? 2015-09-06

Вили:Вил




Андрей:Андре












Ending 2012-11-15









FEMALE NAMES FROM TEMPLATE

PLACE NAMES FROM TEMPLATES !!



 * **@U.Cap.Opt@+Sem/Plc+EOLang/KPV+Der+Der/LocMod:@U.Cap.Opt@%>са A_ ; ** This requires down-casing















# Verbal morphology               





## Closed class verbs







## Open class verbs

Some Flag diacritic lines are with regexes, other with aligned zeros. We want to migrate to
regexes < … > , for readability reasons (sic!)

 * **LEXICON V_LOKNY** One verb only, локны:лок

Begin work with TV and IV



 * **LEXICON VR_SHUNY** 

 * **LEXICON V_SHUNY** шуны:шу янӧдны, контролируйтны. Ending in -дны, -тны, -Cны, -Vны.

 * **LEXICON V_JUAYSHNY** is there ш : шт gradation

 * **LEXICON V_AMNY** амны:ам Ending in -мны, -жны, -дзны,


 * **LEXICON V_KYJNY** кыйны:кый Ending in -йны, 

 * **LEXICON V_CHILOESNY** is there s : st alternation 2018-09-01


 * **LEXICON V_KUTNY** шуны:шу янӧдны, контролируйтны. Ending in -дны, -тны, -Cны, -Vны.


 * **LEXICON V_NUAVNY** нуавны:нуа
Consonant-onset


 * **LEXICON V_ARTASJNY** артасьны:артас -Cны.

 * **LEXICON VR_LYDDJYNY** 

 * **LEXICON V_LYDDJYNY** лыддьыны:лыддьы ! ярмыны. Multiple-syllable verb ending in -ыны.


 * **LEXICON V_VOLYNY** волыны:волы ! ярмыны. Multiple-syllable verb ending in -ыны.








## Verb conjugation 

 * **LEXICON VerbConj-V**  суф б -- ы 

 * **LEXICON VerbConj** суф а

 * **LEXICON VerbConj_KYJNY** суф а

 * **LEXICON VerbConj_AMNY** суф а

 * **LEXICON VerbConj_KUTNY** суф а


 * **LEXICON Finiteforms** Gives linking vowels for 3 tenses

 * **LEXICON Finiteforms_KYJNY** Gives linking vowels for 3 tenses

 * **LEXICON Finiteforms_AMNY** Gives linking vowels for 3 tenses

 * **LEXICON Finiteforms_KUTNY** Gives linking vowels for 3 tenses













 * **@U.CONJ-MX.IMP@@U.CONJ-NX.PL@@U.CONJ-PX.2@+Imprt+Pl2:@U.CONJ-MX.IMP@@U.CONJ-NX.PL@@U.CONJ-PX.2@%>ӧ VerbEnd ;** kpv -ӧй













Differs from kpv 2016-09-15









## Derivation


 * **LEXICON Verb-nyDer** 

 * **LEXICON Verb-nyDer-ONSET-CONS** Derivation onset in consonant
verb-to-verb

This is fed by LEXICON V_SHUNY, and therefore certain corrections
must be made 2012-01-18

овсьыны
пусьыштлывлыны
босьтчыштлывлыны

 * **LEXICON Verb-nyDer-ONSET-VOW** Derivation onset	in vowel

 * **LEXICON Verb-nyDer-ONSET-Y** Derivation onset	in vowel

 * **LEXICON Verb-nyDer-ONSET-A** Derivation onset	in vowel
босьтасьны

 * **LEXICON Verb-nyDer-ONSET-JA** Derivation onset	in vowel
босьтасьны


verb-to-noun

 * **LEXICON VerbDer** 
FIX THIS 2015-09-06

 * **LEXICON VerbDer_KYJNY**
 * **:й VerbDer-ONSET_OE ;**
 * **:й VerbDer-ONSET_JA ;** 
 * **:й VerbDer-ONSET_JI ;**

 * **LEXICON VerbDer_KUTNY**
 * **VerbDer-ONSET_OE ;**
 * **VerbDer-ONSET_A ;** 
 * **VerbDer-ONSET_JI ;**

 * **LEXICON VerbDer_ARTASJNY**
 * **: VerbDer-ONSET_OE ;**
 * **: VerbDer-ONSET_JA ;** 
 * **: VerbDer-ONSET_JI ;**

 * **LEXICON VerbDer-ONSET_OE** 
 * **+Der/ісь+ActPrsPtc:%>%{иі%}сь N_ ;** kpv ысь

 * **LEXICON VerbDer-ONSET_JI** 


 * **LEXICON VerbDer-ONSET_A** 

 * **LEXICON VerbDer-ONSET_JA** 










вевттьысьыны

бертласьны
















# Conjunctors
----
Komi conjunctors










# Postposition inflection
----

Komi postpositions inflect for direction.

Prep lexica

Russian на


Postp lexica 







This contlex allows for relational word which, otherwise, are open 
to extensive declension


 * **LEXICON POSTP1  **
these are: 

аддза, бӧрті, бокиті, боксянь, дырйи, йитӧдын, 
кузя, ног, ньылыд, паныдӧн, пӧлӧн, пыдди, пыр, понда, 
ради, уліті, выліті, вывті, вомас, вомӧн
пӧвст














 * **LEXICON PO-SPAT_  **
these are: 

аддза, бӧрті, бокиті, боксянь, дырйи, йитӧдын, 
кузя, ног, ньылыд, паныдӧн, пӧлӧн, пыдди, пыр, понда, 
ради, уліті, выліті, вывті, вомас, вомӧн
пӧвст





















Prefixes
Prefixes in the Komi-Permyak language are bound to the beginning of other words.



# Adjective inflection
----
Komi (Permyak) adjectives compare.

Continuation lexicon has been assigned according to <pos/> content























 * LEXICON A_PARAGOGIC-В/Л  юмов:юмо юмолӧсь
Singular predicative 





# Pronominal morphology                           

## Closed class personal pronouns

 * **LEXICON PERS** 
 * **ме+Pron+Pers+Sg1:ме perssg1decl ;** ...

 * **ачым+Pron+Refl+Sg1:а REFLSG1DECL ;** ...




 * **LEXICON perssg1decl** 


 * **LEXICON perspl1decl**


 * **LEXICON perssg2decl**

 * **LEXICON perspl2decl** 




 * **LEXICON perssg3decl** 


ми мийӧ The 1st and 2nd persons have Oblique case stem strategies
that differ from the 3rd person: 
ті тійӧ nämä ovat aivan eri asioita?
сы сійӧ tosin joskus 

 * **LEXICON perspl3decl**


 * **LEXICON perssg**



 * **LEXICON persplobl**


























































































































































Tagged in the src/morphology/stems/pronouns.xml file













# Particles
----
Komi Particles












INTRODUCTION TO MORPHOLOGICAL ANALYSER OF Komi-Permyak LANGUAGE.


 # Definitions for Multichar_Symbols




## Analysis symbols
The morphological analyses of wordforms for the Komi-Permyak
language are presented in this system in terms of the following symbols.
(It is highly suggested to follow existing standards when adding new tags).

The parts-of-speech tags are:
 * **+A**:  adjective
 * **+Adp**:  Adposition
 * **+Adv**:  adverb
 * **+CS**:  subordinating conjunction
 * **+CC**:  coordinating conjunction
 * **+Interj**:  interjection
 * **+N**:  noun
 * **+Pcle**:  particle
 * **+Po**:  postposition
 * **+Pr**:  preposition
 * **+Pron**:  pronoun
 * **+Qnt**:  Quantifier
 * **+V**:  verb



The parts of speech are further split up into:
Adjectives

Adverbs
These are ideophonic descriptors used to modify the verb
вырк ливтясь "**flit** and it flew off"
 * **+Deg** Degree depricate AdA
Ad-adjective
with reference to type of adverb
spatial
temporal
multiplicative, i.e. iterations
 * **+Parenthetic** parenthetical phrase

Interjections
  +Conative   Used for calling animals, for example

Nouns
proper
used with paired nouns **collective nouns**
 * **+Relat** relational noun: выв, ув

Postpositions

## Pronouns
 * **+Dem**:  demonstrative
 * **+Indef**:  indefinite
 * **+Interr**:  interrogative
 * **+Pers**:  personal
 * **+Recipr**:  reciprocal
 * **+Refl**:  reflexive
 * **+Rel**:  relative

## Quantifiers (numerals)
Quantifiers and Numerals are classified under:
 * **+Num**:  numeral
 * **+Appr**:  Approximative numeral кавто-колмо, колмошка *two or three*
          NB! do not confuse with Komi case +Apr
 * **+AssocColl**:  -ne- ; avide-
 * **+Assoc**:  +мезть
 * **+Card**:  cardinal + NCard
 * **+Coll**:  collective
 * **+Distr**:  Distributive
 * **+Iter: Iterative form expressing number of times; kpv**:  `кыкысь`
 * **+Ord**:  ordinal + NOrd
 * **+Coord**:  Coordinates, i.e. 65˚36′8,30″ in numerals.lexc
 * **+Cop**:  this is for copula complement position with pl in -ӧсь Pred depricated


## Nominals are inflected for Number and Case
## Number
singular
plural
## Case
accusative -ӧс
ablative case -лісь
approximative -лань
approximative egressive -ланьсянь
approximative elative -ланьысь
approximative illative -ланьӧ
approximative inessive -ланьын
approximative prolative -ланьӧт
approximative terminative -ланьӧдз
approximative terminative -ланьви
carative -тӧг
consecultative -ла
Comitative -кӧт
Comparative case form -ся
 *  **+Cmpl**  Postposition complement
dative case -лӧ
egressive -сянь
elative -ысь
genitive case -лӧн
illative -ӧ
inessive -ын
instrumental -ӧн
nominative case
prolative -ӧт
Terminative -ви
Terminative -ӧдз
Vocative


transitive THIS should be removed 2019-11-01

used when possessive marking occurs before case
used when case occurs before possessive marking




this will be used for marking complement forms such as кыкнан in collective numerals, сы , which can only appear with a following NP. DO WE NEED THIS 2019-10-22? jaska Niko


## Symbols that need to be escaped on the lower side (towards twolc):
 * **»7**:  Literal »
 * **«7**:  Literal «
```
  %[%>%]  - Literal >
  %[%<%]  - Literal <
```




The possession is marked as such:
ODD

The comparative forms are:
 * **+Comp**:  comparative
 * **+Superl**:  superlative
 * **+Mdr**:  moderative -моз, -кодь  'kind of, -ish' with reference to quality ыджыткодь 'rather big'
 * **+Aug**:  augmentative, intensive -ӧв 'too X' with reference to quality ыджытӧв 'too big'
 *  **+Der/AdvCompMod** Adverbial comparative modifier in моз Der/моз +MOZ  diminishing, kind of, sort of
 *  **+Der/CompMod** comparative modifier in кодь Der/кодь ! diminishing, kind of, sort of

Numerals are classified under:

Verb moods are:
 * **+Imprt**:  imperative
 * **+Ind**:  indicative
 * **+Prs**:  present      -ӧ
 * **+Prt1**:  preterite 1 -ис
 * **+Prt2**:  preterite 2 -ӧма
 * **+Fut**:  future      -ас
 * **+Prec**:  Precative mood is a directive mood that signals that the utterance is a request. -ко on imperative forms equals Precative
Verb personal forms are:
Other verb forms are
Gerund This is used with derivations


 * +Symbol = independent symbols in the text stream, like £, €, ©
Special symbols are classified with:
The verbs are syntactically split according to transitivity:
Special multiword units are analysed with:
Non-dictionary words can be recognised with:

Question and Focus particles:


### Tags distinguishing different versions of the same lemma (before POS)
 * +v1
 * +v2
 * +v3
 * +v4
 * +v5
 * +v6
 * +v7
 * +v8
 * +v9
 * +v10
 * +v11
 * +v12
 * +v13
 * +v14
 * +v15

The Usage extents are marked using following tags:

Where do these come from source
 * **+Src/F** foreign source apparently 2015-09-08
 * **+Dim** diminutive


 * **+Sem/Act** Activity
 * **+Sem/Amount** Amount
 * **+Sem/Ani** Animate
 * **+Sem/Aniprod** Animal Product
 * **+Sem/Ant** Antroponym
 * **+Sem/Ant-Fem** Female Antroponym
 * **+Sem/Ant-Mal** Male Antroponym
 * **+Sem/Body** Bodypart
 * **+Sem/Body-abstr** siellu, vuoig?a, jierbmi
 * **+Sem/Build** Building
 * **+Sem/Build-part** Part of Bulding, like the closet
 * **+Sem/Cat** Category
 * **+Sem/Clth** Clothes
 * **+Sem/Clth-jewl** Jewelery
 * **+Sem/Clth-part** part of clothes, boallu, sávdnji...
 * **+Sem/Ctain** Container
 * **+Sem/Ctain-abstr** Abstract container like bank account
 * **+Sem/Ctain-clth**
 * **+Sem/Curr** Currency like dollár, Not Money
 * **+Sem/Dance** Dance
 * **+Sem/Dir** Direction like GPS-kursa
 * **+Sem/Domain** Domain like politics, reindeerherding (a system of actions)
 * **+Sem/Drink** Drink
 * **+Sem/Dummytag** Dummytag
 * **+Sem/Edu** Educational event
 * **+Sem/Event** Event
 * **+Sem/Feat** Feature, like Árvu
 * **+Sem/Feat-phys** Physiological feature, ivdni, fárda
 * **+Sem/Feat-psych** Psychological feauture
 * **+Sem/Feat-measr** Psychological feauture
 * **+Sem/Fem** Female name
 * **+Sem/Food** Food
 * **+Sem/Food-med** Medicine
 * **+Sem/Furn** Furniture
 * **+Sem/Game** Game
 * **+Sem/Geom** Geometrical object
 * **+Sem/Group** Animal or Human Group
 * **+Sem/Hum** Human
 * **+Sem/Hum-abstr** Human abstract
 * **+Sem/Hum-prof** Human professional
 * **+Sem/Ideol** Ideology
 * **+Sem/Lang** Language
 * **+Sem/Mal** Male name
 * **+Sem/Mat** Material for producing things
 * **+Sem/Measr** Measure
 * **+Sem/Money** Has to do with money, like wages, not Curr(ency)
 * **+Sem/Obj** Object
 * **+Sem/Obj-clo** Cloth
 * **+Sem/Obj-cogn** Cloth
 * **+Sem/Obj-el** (Electrical) machine or apparatus
 * **+Sem/Obj-ling** Object with something written on it
 * **+Sem/Obj-rope** flexible ropelike object
 * **+Sem/Obj-surfc** Surface object
 * **+Sem/Org** Organisation
 * **+Sem/Part** Feature, oassi, bealli
 * **+Sem/Patr** Patronymic
 * **+Sem/Patr-Fem** Female Patronymic
 * **+Sem/Patr-Mal** Male Patronymic
 * **+Sem/Perc-cogn** Cognative perception
 * **+Sem/Perc-emo** Emotional perception
 * **+Sem/Perc-phys** Physical perception
 * **+Sem/Perc-psych** Physical perception
 * **+Sem/Plant** Plant
 * **+Sem/Plant-part** Plant part
 * **+Sem/Plc** Place
 * **+Sem/Plc-abstr** Abstract place
 * **+Sem/Plc-elevate** Place
 * **+Sem/Plc-line** Place
 * **+Sem/Plc-water** Place
 * **+Sem/Pos** Position (as in social position job)
 * **+Sem/Process** Process
 * **+Sem/Prod** Product
 * **+Sem/Prod-audio** Audio product
 * **+Sem/Prod-cogn** Cognition product
 * **+Sem/Prod-ling** Linguistic product
 * **+Sem/Prod-vis** Visual product
 * **+Sem/Rel** Relation
 * **+Sem/Route** Name of a Route
 * **+Sem/Rule** Rule or convention
 * **+Sem/Semcon** Semantic concept
 * **+Sem/Sign** Sign (e.g. numbers, punctuation) 
 * **+Sem/Sport** Sport
 * **+Sem/State** 
 * **+Sem/State-sick** Illness
 * **+Sem/Substnc** Substance, like Air and Water
 * **+Sem/Sur** Surname
 * **+Sem/Sur-Fem** Surname
 * **+Sem/Sur-Mal** Surname
 * **+Sem/Symbol** Symbol
 * **+Sem/Time** Time
 * **+Sem/Tool** Prototypical tool for repairing things
 * **+Sem/Tool-catch** Tool used for catching (e.g. fish)
 * **+Sem/Tool-clean** Tool used for cleaning
 * **+Sem/Tool-it** Tool used in IT
 * **+Sem/Tool-measr** Tool used for measuring
 * **+Sem/Tool-music** Music instrument
 * **+Sem/Tool-write** Writing tool
 * **+Sem/Txt** Text (girji, lávlla...)
 * **+Sem/Veh** Vehicle
 * **+Sem/Wpn** Weapon
 * **+Sem/Wthr** The Weather or the state of ground





Semantics are classified with
 * **+Sem/Inanim**  Inanimate,
 * **+Sem/NonHum**  Nonhuman,


Derivations are classified under the morphophonetic form of the suffix, the
source and target part-of-speech.



 * **+Der/ісь** Der/ысь







 *  **+Der/PrivMod** privative or abessive modifier -тӧм AbeMod
 *  **+Der/LocMod** locative modifier са - IneMod
 *  **+Der/ProprietiveMod** habeo modifier HabObjMod Der/а
 *  **+Der/TempMod** temporal modifier ся -



2012-09-11 Perhaps this is only syntactic





Tags for Ethymological Origin marking. This has initially used used with proper nouns




Morphophonology
To represent phonologic variations in word forms we use the following
symbols in the lexicon files:


And following triggers to control variation
 * %^1Cns    Plural-initial; it allows for doubling of consonant
 * %^LVBound     boundary for LV change instead of Consonant or end of word
 * %^VowRM       vowel syncope

* »
* «
* > (escaped with square brackets, to avoid collision with > as morpheme boundary)
* < (escaped with square brackets, to avoid collision with < as morpheme boundary)

## Flag diacritics
We have manually optimised the structure of our lexicon using following
flag diacritics to restrict morhpological combinatorics - only allow compounds
with verbs if the verb is further derived into a noun again:
 |  @P.NeedNoun.ON@ | (Dis)allow compounds with verbs unless nominalised
 |  @D.NeedNoun.ON@ | (Dis)allow compounds with verbs unless nominalised
 |  @C.NeedNoun@ | (Dis)allow compounds with verbs unless nominalised

For languages that allow compounding, the following flag diacritics are needed
to control position-based compounding restrictions for nominals. Their use is
handled automatically if combined with +CmpN/xxx tags. If not used, they will
do no harm.
 |  @P.CmpFrst.FALSE@ | Require that words tagged as such only appear first
 |  @D.CmpPref.TRUE@ | Block such words from entering ENDLEX
 |  @P.CmpPref.FALSE@ | Block these words from making further compounds
 |  @D.CmpLast.TRUE@ | Block such words from entering R
 |  @D.CmpNone.TRUE@ | Combines with the next tag to prohibit compounding
 |  @U.CmpNone.FALSE@ | Combines with the prev tag to prohibit compounding
 |  @P.CmpOnly.TRUE@ | Sets a flag to indicate that the word has passed R
 |  @D.CmpOnly.FALSE@ | Disallow words coming directly from root.

Use the following flag diacritics to control downcasing of derived proper
nouns (e.g. Finnish Pariisi -> pariisilainen). See e.g. North Sámi for how to use
these flags. There exists a ready-made regex that will do the actual down-casing
given the proper use of these flags.
 |  @U.Cap.Obl@ | Allowing downcasing of derived names: deatnulasj.
 |  @U.Cap.Opt@ | Allowing downcasing of derived names: deatnulasj.









FLAGS USED WITH COLLECTIVE NOUNS








Removal

 |  @U.Cap.Obl@ | Allowing downcasing of derived names: deatnulasj
 |  @U.Cap.Opt@ | Allowing downcasing of derived names: deatnulasj


The word forms in the KOMI-PERMYAK language start from the lexeme roots of basic

word classes, or optionally from prefixes:


Incoming from akusanat
  Pron_koi2x ;


Incoming for conversion from kpv
































We describe here how abbreviations are in Komi-Permyak are read out, e.g.
for text-to-speech systems.

For example:

 * s.:syntynyt # ;  
 * os.:omaa% sukua # ;  
 * v.:vuosi # ;  
 * v.:vuonna # ;  
 * esim.:esimerkki # ; 
 * esim.:esimerkiksi # ; 


