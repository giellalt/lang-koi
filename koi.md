# Komi-Permyak description 

All documents in one file

# Komi-Permyak disambiguator

## Delimiters 

Sentence delimiters are: "<.>" "<!>" "<?>" "<...>" "<¶>" sent

## Tags and sets 

### Beginning and end of sentence	
BOS
EOS

### Miscellanous

CmpTest
Err
Err
вӧлі Sg3

### Parts of speech tags
N
V
A
Adv
CC
CS
Inter
Pron
Num
Pcle
Clt
Po
Dem
Qnt
Prop

### Derivation tags
Ex/A (former adj)
Ex/N
Ex/Num
Ex/V
Ex/WORD
DerTag
AspDerTag

### Verbal categories
Prs
Fut
Fut1
Imprt
Prt1
Prt2
Prf
PrfIpf
HstPrf
PluPrf
HstPluPrf
Ind
Imp
Cond
Opt

Sg1
Sg2
...

Nominal categories
Sg
Pl
Nom
Gen
Abl
Dat
Com 
Cns
...

### Verb sets
VNEG (all Neg verbs)

VFIN

ASKI (tomorrow set)

NOT-PRL (have no homograph Prolative pairs set)

## Rule section

* **NoDerIfPossible** removes all derivations

* **Dem** selects Dem if N Nom to the right

* **NoFinalCC** removes CC if competing Pcle and sentence-final
* **NoABBR** removes ABBR for competing CC

* * *
<small>This (part of) documentation was generated from [src/cg3/disambiguator.cg3](https://github.com/giellalt/lang-koi/blob/main/src/cg3/disambiguator.cg3)</small>

* Sets for POS sub-categories

* Sets for Semantic tags

* Sets for Morphosyntactic properties

* Sets for verbs

- V is all readings with a V tag in them, REAL-V should
be the ones without an N tag following the V.  
The REAL-V set thus awaits a fix to the preprocess V ... N bug.

* The set COPULAS is for predicative constructions

* NP sets defined according to their morphosyntactic features

* The PRE-NP-HEAD family of sets

These sets model noun phrases (NPs). The idea is to first define whatever can
occur in front of the head of the NP, and thereafter negate that with the
expression **WORD - premodifiers**.

The set **NOT-NPMOD** is used to find barriers between NPs.
Typical usage: ... (*1 N BARRIER NPT-NPMOD) ...
meaning: Scan to the first noun, ignoring anything that can be
part of the noun phrase of that noun (i.e., "scan to the next NP head")

* Miscellaneous sets

* Border sets and their complements

* Syntactic sets

These were the set types.

## HABITIVE MAPPING

* **hab1** 

* **hab2** 

* **hab3** (<hab> @ADVL>) for hab-actor and hab-case; if leat to the right, and Nom to the right of leat. Lots of restrictions.

* **habNomLeft** 

* **hab4** 	

* **hab6** 

* **hab7** 

* **hab8** This is not HAB
* **hab5**  This is not HAB

* **habDain** (<hab> @ADVL>) for (Pron Dem Pl Loc) if leat followed by Nom to the right

* **habGen** (<hab> @<ADVL) hab for Gen; if Gen is located in the end of the sentence and Nom is sentence initial

* **spred<obj** (@SPRED<OBJ) for Acc; the object of an SPRPED. Not to be mistaken with OPRED. If SPRED is to the left, and copulas is to the left of it. Nom or Hab are found sentence initially.

* **Hab<spred** (@<SPRED) for Nom; if copulas, goallut or jápmit is FMAINV and habitive or human Loc is found to the left. OR: if Ill or @Pron< followed by HAB are found to the left.

* **Hab>Advlcase<spred** (<ext> @<SUBJ) for Nom; it allows adverbials with Ill/Loc/Com/Ess to be found inbetween HAB and <ext>.

* **Nom>Advlcase<spred** (<ext> @<SUBJ) for Nom; it allows adverbials with Ill/Loc/Com/Ess to be found inbetween Nom and <ext> @<SUBJ.

* **<spred** (<ext> @<SUBJ) for Nom; if copulas to the left, and some kind of adverb, N Loc, time related word or Po to the left of it. OR: if Ill or @Pron< to the left, followed by copulas and the before mentioned to the left of copulas. 

* **<spred** (<ext> @<SUBJ) for Nom, but not for Pers. To the left boahtit or heaŋgát as MAINV, and futher to the left is some kind of place related word, or time related word

* **<spredQst1** (<ext> @<SUBJ) for Nom in a typically question sentence; if A) Hab, some kind of place word, Po or Nom to the left, and Qst followed by copulas to the left. B) same as a, only the Qst-pcle is attached to copulas. C) Qst to the left, with copulas to its left, but not if two Nom:s are found somewhere to the right. D) copulas to the left, and BOS to the left. E) Loc or Ill to the left, and Loc or Hab to the left of this, Qst and copulas to the left. F) Num @>N to the left, Hab, some kind of place word, Po or Nom to the left, and Qst followed by copulas to the left. NOTE) for all these rules; human, Loc or Sem/Plc not allowed to the right.

* **<spredQst2** (@<SPRED) for Nom; in a typically question sentence; differs from <spredQst1 by not beeing as restricted to the right. Though you are not allowed to be Pers or human.

* **Nom<spredQst** (@<SPRED) for Nom; in a typically question sentence. Differs from <spredQst2 by letting Nom be found between SPRED and copulas

* **<spred** (@<SPRED) for A Nom or N Nom if; the subject Nom is on the same side of copulas as you: on the right side of copulas

* **<spredVeara** (@<SPRED) for veara + Nom; if genitive immediately to the right, and intransitive mainverb to the right of genitive

* **leftCop<spred** (@<SPRED) for Nom; if copulas is the main verb to the left, and there is no Ess found to the left of cop (note that Loc is allowed between target and cop). OR: if you are Coll or Sem/Group with copulas to your left. 

* **<spredLocEXPERIMENT** (@<SPRED) for material Loc; if you are to the right of copulas, and the Nom to the left of copulas is not a hab-actor

* **NumTime** (@<SPRED) for A Nom

* **<spredSg** (@<SPRED) for Sg Nom	

* **<spredPg** (@<SPRED) for Pl Nom	

* **<spred** (@<SPRED) for Nom; if copulas to the left, and Nom or sentence boundary to the left of copulas. First one to the right is EOS.

* **<spred** (@<SPRED) for N Ess

* **spredEss>** (@SPRED>) for N Ess; if copulas to the right of you, and if an NP with nom-case first one to your left.

* **HABSpredSg>** (@SPRED>) for Nom; if habitive first one to the left, followed by copulas.

* **GalleSpred>** (@SPRED>) for Num Nom; if sentence initial

* **spredSgMII>** (@SPRED>)

* **r492>** (@SPRED>) for Interr Gen; consisting only of negations. You are not allowed to be MII. You are not allowed to have an adjective or noun to yor right. You are not allowed to have a verb to your right; the exception beeing an aux.

* **AdjSpredSg>** (@SPRED>) for A Sg Nom; if copulas to the right, but not if A or @<SPRED are found to the right of copulas

* **SpredSg>Hab** (@SPRED>) for Nom; if you are sentence initial, copulas is located to the right, and there is a habitive to the right of copulas

* **Spred>SubjInf** (@SPRED>) for Nom; if copulas to the right, and the subject of copulas is an Inf to the right

* **spredCoord** (@<SPRED) coordination for Nom; only if there already is a SPRED to the left of CNP. Not if there is some kind of comparison involved.

* **subj>Sgnr1** (@SUBJ>) for Nom Sg, including Indef Nom if; VFIN + Sg3 or Pl3 to the right (VFIN not allowed to the left) 

* **subj>Du** (@SUBJ>) for dual nominatives, including Coll Nom. VFIN + Du3 to the right. 
* **subj>Pl** (@SUBJ>) for plural nominatives, including Coll and Sem/Group. VFIN + Pl3 to the right.

* **subj>Pl** (@SUBJ>) for plural nominatives

* **subj>Sgnr2** (@SUBJ>) for Nom Sg; if VFIN + Sg3 to the right.

* **<subjSg** (@<SUBJ) for Nom Sg; if VFIN Sg3 or Du2 to the left (no HAB allowed to the left).

* **f<advl** (@-F<ADVL) for infinite adverbials

* **f<advl** (@-F<ADVL) for infinite adverbials

* **s-boundary=advl>** (@ADVL>) for ADVL that resemble s-booundaries. Mainverb to the right.

* **-fobj>** (@-FOBJ>) for Acc 

* **-fobj>** (@-FOBJ>) for Acc

* **advl>mainV** (@ADVL>) if; finite mainverb not found to the left, but the finite mainverb is found to the right.

* **<advl** (@<ADVL) if; finite mainverb found to the left. Not if a comma is found immediately to the left and a finite mainverb is located somewhere to the right of this comma.

* **<advlPoPr** (@<ADVL) if mainverb to the left.
* **advlPoPr>** (@<ADVL) if mainverb to the right.

* **advlEss>** (@<ADVL) for weather and time Ess, if FMAINV to the left.

* **advl>inbetween** (@ADVL>) for Adv; if inbetween two sentenceboundaries where no mainverb is present.

* **comma<advlEOS** (@<ADVL) if; comma found to the left and the finite mainverb to the left of comma. To the right is the end of the sentence.

* **advlBOS>** (@ADVL>) if; you are N Ill and found sentnece initially. First one to your right is a clause.

* **<advlPoEOS** (@<ADVL) for Po; if you are found at the very end of a sentence. A mainverb is needed to the right though.

* **cleanupILL<advl** (@<ADVL) for N Ill if; there are no boundarysymbols to your left, if you arent already @N< OR @APP-N<, and no mainverb is to yor left.

* **<opredAAcc** (@<OPRED) for A Acc; if an other accusative to the left, and a transtive verb to the left of it. OR: if a transitive verb to the left, and an accusative to the left of it.

### sma object

* **<advlEss** (@<ADVL) for ESS-ADVL if; FMAINV to the left
* **<spredEss** (@<SPRED) for N Ess if; FMAINV to the left is intransitive or bargat

## SUBJ MAPPING - leftovers

## OBJ MAPPING - leftovers

## HNOUN MAPPING

* * *
<small>This (part of) documentation was generated from [src/cg3/functions.cg3](https://github.com/giellalt/lang-koi/blob/main/src/cg3/functions.cg3)</small># Adjective inflection
----
Komi (Permyak) adjectives compare.

Continuation lexicon has been assigned according to <pos/> content

* LEXICON A_PARAGOGIC-В/Л  юмов:юмо юмолӧсь
Singular predicative 

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/adjectives.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/affixes/adjectives.lexc)</small>

---

# Postposition inflection
----

Komi postpositions inflect for direction.

Prep lexica

Russian на

Postp lexica 

This contlex allows for relational word which, otherwise, are open 
to extensive declension

* **LEXICON PO_ **

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

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/adpositions.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/affixes/adpositions.lexc)</small>

---

# Adverb inflection
----
Komi adverbs inflect for direction.

* **LEXICON ADV-SPAT  **
these are adverbs in spatial cases
and they probably are equivalent in morphology to postpositions

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/adverbs.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/affixes/adverbs.lexc)</small>

---

# Conjunctors
----
Komi conjunctors

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/conjunctors.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/affixes/conjunctors.lexc)</small>

---


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

## Case followed by possible clitic OR WORDEND

+Der/A+Adv:%>а K ;

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/nouns.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/affixes/nouns.lexc)</small>

---



# Numeral morphological lexica 

LEXICON NUM-APPR ! 2011-11-03 This will need work

## Inflectional lexica 

All nouns follow one contlex "Noun1"
to begin with here is simply a list of all variant
with no more variants beyond:

## Arabic numerals

* **LEXICON ARABIC          ** 

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/numerals.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/affixes/numerals.lexc)</small>

---

# Particles
----
Komi Particles

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/particles.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/affixes/particles.lexc)</small>

---

Prefixes
Prefixes in the Komi-Permyak language are bound to the beginning of other words.

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/prefixes.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/affixes/prefixes.lexc)</small>

---

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

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/pronouns.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/affixes/pronouns.lexc)</small>

---

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

These are vowel-final stems
They have previously received +Sem/Fem tags

Should this be limited to +Sg? 2015-09-06

Вили:Вил

Андрей:Андре

Ending 2012-11-15

FEMALE NAMES FROM TEMPLATE

* **@U.Cap.Opt@+Sem/Plc+EOLang/KPV+Der+Der/LocMod:@U.Cap.Opt@%>са A_ ; ** This requires down-casing

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/propernouns.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/affixes/propernouns.lexc)</small>

---


# Symbol affixes

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/symbols.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/affixes/symbols.lexc)</small>

---



# Verbal morphology               

## Closed class verbs

## Open class verbs

Some Flag diacritic lines are with regexes, other with aligned zeros. We want to migrate to
regexes < … > , for readability reasons (sic!)

* **LEXICON V_LOKNY** One verb only, локны:лок U9 — глагол локны

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

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/verbs.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/affixes/verbs.lexc)</small>

---

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
* »
* «
* > (escaped with square brackets, to avoid collision with > as morpheme boundary)
* < (escaped with square brackets, to avoid collision with < as morpheme boundary)

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

**j to soft sign after r**

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

<small>This (part of) documentation was generated from [src/fst/morphology/phonology.twolc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/phonology.twolc)</small>

---


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
* **+Tot**:  universal кыкнан; кыкнанным

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
* **+Dim** diminutive,  words that are already -ok dimin

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

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/root.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/root.lexc)</small>

---

Adjectives
Adjectives in Komi-Permyak language describe things.

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/adjectives.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/stems/adjectives.lexc)</small>

---

This is where new words from kpv are initially shown

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/adjectives_newwords.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/stems/adjectives_newwords.lexc)</small>

---

This is where new words from kpv are initially shown

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/adverbs_newwords.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/stems/adverbs_newwords.lexc)</small>

---

This is where new words are added as lexc entries before they are 
added to the xml source files.
Абъячой+N+Prop+Sem/Plc:Абъячой PROP_ "(eng) fish/(fin) /(rus)" ;

ADD NOUNS BELOW

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/kom-rus-propernouns_newwords.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/stems/kom-rus-propernouns_newwords.lexc)</small>

---

Nouns
Nouns in the Komi Permyak language are things.

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/nouns.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/stems/nouns.lexc)</small>

---

This is where new words from kpv are initially shown

2016-07-14

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/nouns_newwords.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/stems/nouns_newwords.lexc)</small>

---

Numerals
Numerals in the KOMI-PERMYAK language are numbers.

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/numerals.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/stems/numerals.lexc)</small>

---

This is where new words from kpv are initially shown

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/numerals_newwords.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/stems/numerals_newwords.lexc)</small>

---

Pronouns
Pronouns in KOMI PERMYAK language are references to things.

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/pronouns.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/stems/pronouns.lexc)</small>

---

This is where new words from kpv are initially shown

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/pronouns_newwords.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/stems/pronouns_newwords.lexc)</small>

---

This is where new words from kpv are initially shown

These are koi verbs

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/verbs_newwords.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/morphology/stems/verbs_newwords.lexc)</small>

---



retroflex plosive, voiceless			t`  ʈ	    0288, 648 (` = ASCII 096)
retroflex plosive, voiced			d`	ɖ		0256, 598
labiodental nasal					F 	ɱ		0271, 625
retroflex nasal						n` 	ɳ		0273, 627
palatal nasal						J 	ɲ		0272, 626
velar nasal							N 	ŋ		014B, 331
uvular nasal							N\	ɴ		0274, 628
	
bilabial trill						B\ 	ʙ		0299, 665
uvular trill							R\ 	ʀ		0280, 640
alveolar tap							4	ɾ		027E, 638
retroflex flap						r` 	ɽ		027D, 637
bilabial fricative, voiceless		p\ 	ɸ		0278, 632
bilabial fricative, voiced			B 	β		03B2, 946
dental fricative, voiceless			T 	θ		03B8, 952
dental fricative, voiced				D 	ð		00F0, 240
postalveolar fricative, voiceless	S	ʃ		0283, 643
postalveolar fricative, voiced		Z 	ʒ		0292, 658
retroflex fricative, voiceless		s` 	ʂ		0282, 642
retroflex fricative, voiced			z` 	ʐ		0290, 656
palatal fricative, voiceless			C 	ç		00E7, 231
palatal fricative, voiced			j\ 	ʝ		029D, 669
velar fricative, voiced	        	G 	ɣ		0263, 611
uvular fricative, voiceless			X	χ		03C7, 967
uvular fricative, voiced				R 	ʁ		0281, 641
pharyngeal fricative, voiceless		X\ 	ħ		0127, 295
pharyngeal fricative, voiced			?\ 	ʕ		0295, 661
glottal fricative, voiced			h\	ɦ		0266, 614

alveolar lateral fricative, vl.		K 
alveolar lateral fricative, vd.		K\

labiodental approximant				P (or v\) 
alveolar approximant					r\ 
retroflex approximant				r\` 
velar approximant					M\

retroflex lateral approximant		l` 
palatal lateral approximant			L 
velar lateral approximant			L\
Clicks

bilabial								O\	(O = capital letter) 
dental								|\
(post)alveolar						!\ 
palatoalveolar						=\ 
alveolar lateral						|\|\
Ejectives, implosives

ejective								_>	e.g. ejective p		p_>
implosive							_<	e.g. implosive b	b_<
Vowels

close back unrounded					M
close central unrounded 				1 
close central rounded				} 
lax i								I 
lax y								Y 
lax u								U

close-mid front rounded				2 
close-mid central unrounded			@\ 
close-mid central rounded			8 
close-mid back unrounded				7

schwa	ə							@

open-mid front unrounded				E 
open-mid front rounded				9
open-mid central unrounded			3 
open-mid central rounded				3\ 
open-mid back unrounded				V 
open-mid back rounded				O

ash (ae digraph)						{ 
open schwa (turned a)				6

open front rounded					& 
open back unrounded	        		A 
open back rounded					Q
Other symbols

voiceless labial-velar fricative		W 
voiced labial-palatal approx.		H 
voiceless epiglottal fricative		H\ 
voiced epiglottal fricative			<\ 
epiglottal plosive					>\

alveolo-palatal fricative, vl. 		s\ 
alveolo-palatal fricative, voiced	z\ 
alveolar lateral flap				l\ 
simultaneous S and x					x\ 
tie bar								_
Suprasegmentals

primary stress						" 
secondary stress						% 
long									: 
half-long							:\ 
extra-short							_X 
linking mark							-\
Tones and word accents

level extra high						_T 
level high							_H
level mid							_M 
level low							_L 
level extra low						_B
downstep								! 
upstep								^	(caret, circumflex)

contour, rising						 
contour, falling						_F 
contour, high rising					_H_T 
contour, low rising					_B_L 

contour, rising-falling				_R_F 
(NB Instead of being written as diacritics with _, all prosodic 
marks can alternatively be placed in a separate tier, set off 
by < >, as recommended for the next two symbols.)
global rise						<R> 
global fall						<F>
Diacritics						
									
voiceless						_0	(0 = figure), e.g. n_0
voiced							_v 
aspirated						_h 
more rounded						_O	(O = letter) 
less rounded						_c 
advanced							_+
retracted						_-
centralized						_" 
syllabic							=	(or _=) e.g. n= (or n_=) 
non-syllabic						_^ 
rhoticity						`
									
breathy voiced					_t 
creaky voiced					_k
linguolabial						_N 
labialized						_w 
palatalized						'	(or _j) e.g. t' (or t_j) 
velarized						_G 
pharyngealized					_?\
									
dental							_d 
apical							_a 
laminal							_m
nasalized						~	(or _~) e.g. A~ (or A_~) 
nasal release					_n
lateral release					_l 
no audible release				_}

velarized or pharyngealized		_e 
velarized l, alternatively		5 
raised							_r 
lowered							_o 
advanced tongue root				_A 
retracted tongue root			_q

* * *

<small>This (part of) documentation was generated from [src/fst/phonetics/txt2ipa.xfscript](https://github.com/giellalt/lang-koi/blob/main/src/fst/phonetics/txt2ipa.xfscript)</small>

---



We describe here how abbreviations are in Komi-Permyak are read out, e.g.
for text-to-speech systems.

For example:

* s.:syntynyt # ;  
* os.:omaa% sukua # ;  
* v.:vuosi # ;  
* v.:vuonna # ;  
* esim.:esimerkki # ; 
* esim.:esimerkiksi # ; 

* * *

<small>This (part of) documentation was generated from [src/fst/transcriptions/transcriptor-abbrevs2text.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/transcriptions/transcriptor-abbrevs2text.lexc)</small>

---


[ L A N G U A G E ]  G R A M M A R   C H E C K E R

# DELIMITERS

# TAGS AND SETS

## Tags

This section lists all the tags inherited from the fst, and used as tags
in the syntactic analysis. The next section, **Sets**, contains sets defined
on the basis of the tags listed here, those set names are not visible in the output.

### Beginning and end of sentence
BOS
EOS

### Parts of speech tags

N
A
Adv
V
Pron
CS
CC
CC-CS
Po
Pr
Pcle
Num
Interj
ABBR
ACR
CLB
LEFT
RIGHT
WEB
PPUNCT
PUNCT

COMMA
¶

### Tags for POS sub-categories

Pers
Dem
Interr
Indef
Recipr
Refl
Rel
Coll
NomAg
Prop
Allegro
Arab
Romertall

### Tags for morphosyntactic properties

Nom
Acc
Gen
Ill
Loc
Com
Ess
Ess
Sg
Du
Pl
Cmp/SplitR
Cmp/SgNom Cmp/SgGen
Cmp/SgGen
PxSg1
PxSg2
PxSg3
PxDu1
PxDu2
PxDu3
PxPl1
PxPl2
PxPl3
Px

Comp
Superl
Attr
Ord
Qst
IV
TV
Prt
Prs
Ind
Pot
Cond
Imprt
ImprtII
Sg1
Sg2
Sg3
Du1
Du2
Du3
Pl1
Pl2
Pl3
Inf
ConNeg
Neg
PrfPrc
VGen
PrsPrc
Ger
Sup
Actio
VAbess

Err/Orth

### Semantic tags

Sem/Act
Sem/Ani
Sem/Atr
Sem/Body
Sem/Clth
Sem/Domain
Sem/Feat-phys
Sem/Fem
Sem/Group
Sem/Lang
Sem/Mal
Sem/Measr
Sem/Money
Sem/Obj
Sem/Obj-el
Sem/Org
Sem/Perc-emo
Sem/Plc
Sem/Sign
Sem/State-sick
Sem/Sur
Sem/Time
Sem/Txt

HUMAN

PROP-ATTR
PROP-SUR

TIME-N-SET

###  Syntactic tags

@+FAUXV
@+FMAINV
@-FAUXV
@-FMAINV
@-FSUBJ>
@-F<OBJ
@-FOBJ>
@-FSPRED<OBJ
@-F<ADVL
@-FADVL>
@-F<SPRED
@-F<OPRED
@-FSPRED>
@-FOPRED>
@>ADVL
@ADVL<
@<ADVL
@ADVL>
@ADVL
@HAB>
@<HAB
@>N
@Interj
@N<
@>A
@P<
@>P
@HNOUN
@INTERJ
@>Num
@Pron<
@>Pron
@Num<
@OBJ
@<OBJ
@OBJ>
@OPRED
@<OPRED
@OPRED>
@PCLE
@COMP-CS<
@SPRED
@<SPRED
@SPRED>
@SUBJ
@<SUBJ
@SUBJ>
SUBJ
SPRED
OPRED
@PPRED
@APP
@APP-N<
@APP-Pron<
@APP>Pron
@APP-Num<
@APP-ADVL<
@VOC
@CVP
@CNP
OBJ
<OBJ
OBJ>
<OBJ-OTHERS
OBJ>-OTHERS
SYN-V
@X

## Sets containing sets of lists and tags

This part of the file lists a large number of sets based partly upon the tags defined above, and
partly upon lexemes drawn from the lexicon.
See the sourcefile itself to inspect the sets, what follows here is an overview of the set types.

### Sets for Single-word sets

INITIAL

### Sets for word or not

WORD
NOT-COMMA

### Case sets

ADLVCASE

CASE-AGREEMENT
CASE

NOT-NOM
NOT-GEN
NOT-ACC

### Verb sets

NOT-V

### Sets for finiteness and mood

REAL-NEG

MOOD-V

NOT-PRFPRC

### Sets for person

SG1-V
SG2-V
SG3-V
DU1-V
DU2-V
DU3-V
PL1-V
PL2-V
PL3-V

### Pronoun sets

### Adjectival sets and their complements

### Adverbial sets and their complements

### Sets of elements with common syntactic behaviour

### NP sets defined according to their morphosyntactic features

### The PRE-NP-HEAD family of sets

These sets model noun phrases (NPs). The idea is to first define whatever can
occur in front of the head of the NP, and thereafter negate that with the
expression **WORD - premodifiers**.

### Border sets and their complements

### Grammarchecker sets

* * *
<small>This (part of) documentation was generated from [tools/grammarcheckers/grammarchecker.cg3](https://github.com/giellalt/lang-koi/blob/main/tools/grammarcheckers/grammarchecker.cg3)</small># Tokeniser for koi

Usage:
```
$ make
$ echo "ja, ja" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "Juos gorreválggain lea (dárbbašlaš) deavdit gáibádusa boasttu olmmoš, man mielde lahtuid." | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "(gáfe) 'ja' ja 3. ja? ц jaja ukjend \"ukjend\"" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "márffibiillagáffe" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

Pmatch documentation:
<https://github.com/hfst/hfst/wiki/HfstPmatch>

Characters which have analyses in the lexicon, but can appear without spaces
before/after, that is, with no context conditions, and adjacent to words:
* Punct contains ASCII punctuation marks
* The symbol after m-dash is soft-hyphen `U+00AD`
* The symbol following {•} is byte-order-mark / zero-width no-break space
`U+FEFF`.

Whitespace contains ASCII white space and
the List contains some unicode white space characters
* En Quad U+2000 to Zero-Width Joiner U+200d'
* Narrow No-Break Space U+202F
* Medium Mathematical Space U+205F
* Word joiner U+2060

Apart from what's in our morphology, there are
1. unknown word-like forms, and
2. unmatched strings
We want to give 1) a match, but let 2) be treated specially by
`hfst-tokenise -a`
Unknowns are made of:
* lower-case ASCII
* upper-case ASCII
* lower-case cyrillic
* upper-case cyrillic
* select extended latin symbols
* extended cyrillic
ASCII digits
* select symbols
* Combining diacritics as individual symbols,
* various symbols from Private area (probably Microsoft),
so far:
* U+F0B7 for "x in box"

## Unknown handling
Unknowns are tagged ?? and treated specially with `hfst-tokenise`
hfst-tokenise --giella-cg will treat such empty analyses as unknowns, and
remove empty analyses from other readings. Empty readings are also
legal in CG, they get a default baseform equal to the wordform, but
no tag to check, so it's safer to let hfst-tokenise handle them.

Finally we mark as a token any sequence making up a:
* known word in context
* unknown (OOV) token in context
* sequence of word and punctuation
* URL in context

* * *

<small>This (part of) documentation was generated from [tools/tokenisers/tokeniser-disamb-gt-desc.pmscript](https://github.com/giellalt/lang-koi/blob/main/tools/tokenisers/tokeniser-disamb-gt-desc.pmscript)</small>

---

# Grammar checker tokenisation for koi

Requires a recent version of HFST (3.10.0 / git revision>=3aecdbc)
Then just:
```
$ make
$ echo "ja, ja" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

More usage examples:
```
$ echo "Juos gorreválggain lea (dárbbašlaš) deavdit gáibádusa boasttu olmmoš, man mielde lahtuid." | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "(gáfe) 'ja' ja 3. ja? ц jaja ukjend \"ukjend\"" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "márffibiillagáffe" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

Pmatch documentation:
<https://github.com/hfst/hfst/wiki/HfstPmatch>

Characters which have analyses in the lexicon, but can appear without spaces
before/after, that is, with no context conditions, and adjacent to words:
* Punct contains ASCII punctuation marks
* The symbol after m-dash is soft-hyphen `U+00AD`
* The symbol following {•} is byte-order-mark / zero-width no-break space
`U+FEFF`.

Whitespace contains ASCII white space and
the List contains some unicode white space characters
* En Quad U+2000 to Zero-Width Joiner U+200d'
* Narrow No-Break Space U+202F
* Medium Mathematical Space U+205F
* Word joiner U+2060

Apart from what's in our morphology, there are
1) unknown word-like forms, and
2) unmatched strings
We want to give 1) a match, but let 2) be treated specially by hfst-tokenise -a
* select extended latin symbols
* select symbols
* various symbols from Private area (probably Microsoft),
so far:
* U+F0B7 for "x in box"

TODO: Could use something like this, but built-in's don't include šžđčŋ:

Simply give an empty reading when something is unknown:
hfst-tokenise --giella-cg will treat such empty analyses as unknowns, and
remove empty analyses from other readings. Empty readings are also
legal in CG, they get a default baseform equal to the wordform, but
no tag to check, so it's safer to let hfst-tokenise handle them.

Finally we mark as a token any sequence making up a:
* known word in context
* unknown (OOV) token in context
* sequence of word and punctuation
* URL in context

* * *

<small>This (part of) documentation was generated from [tools/tokenisers/tokeniser-gramcheck-gt-desc.pmscript](https://github.com/giellalt/lang-koi/blob/main/tools/tokenisers/tokeniser-gramcheck-gt-desc.pmscript)</small>

---

# TTS tokenisation for smj

Requires a recent version of HFST (3.10.0 / git revision>=3aecdbc)
Then just:
```sh
make
echo "ja, ja" \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

More usage examples:
```sh
echo "Juos gorreválggain lea (dárbbašlaš) deavdit gáibádusa \
boasttu olmmoš, man mielde lahtuid." \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
echo "(gáfe) 'ja' ja 3. ja? ц jaja ukjend \"ukjend\"" \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
echo "márffibiillagáffe" \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

Pmatch documentation:
<https://kitwiki.csc.fi/twiki/bin/view/KitWiki/HfstPmatch>

Characters which have analyses in the lexicon, but can appear without spaces
before/after, that is, with no context conditions, and adjacent to words:
* Punct contains ASCII punctuation marks
* The symbol after m-dash is soft-hyphen `U+00AD`
* The symbol following {•} is byte-order-mark / zero-width no-break space
`U+FEFF`.

Whitespace contains ASCII white space and
the List contains some unicode white space characters
* En Quad U+2000 to Zero-Width Joiner U+200d'
* Narrow No-Break Space U+202F
* Medium Mathematical Space U+205F
* Word joiner U+2060

Apart from what's in our morphology, there are
1) unknown word-like forms, and
2) unmatched strings
We want to give 1) a match, but let 2) be treated specially by hfst-tokenise -a
* select extended latin symbols
* select symbols
* various symbols from Private area (probably Microsoft),
so far:
* U+F0B7 for "x in box"

TODO: Could use something like this, but built-in's don't include šžđčŋ:

Simply give an empty reading when something is unknown:
hfst-tokenise --giella-cg will treat such empty analyses as unknowns, and
remove empty analyses from other readings. Empty readings are also
legal in CG, they get a default baseform equal to the wordform, but
no tag to check, so it's safer to let hfst-tokenise handle them.

Needs hfst-tokenise to output things differently depending on the tag they get

* * *

<small>This (part of) documentation was generated from [tools/tokenisers/tokeniser-tts-cggt-desc.pmscript](https://github.com/giellalt/lang-koi/blob/main/tools/tokenisers/tokeniser-tts-cggt-desc.pmscript)</small>

---

