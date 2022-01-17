


















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
<small>This (part of) documentation was generated from [../src/cg3/functions.cg3](http://github.com/giellalt/lang-koi/blob/main/../src/cg3/functions.cg3)</small># Komi-Permyak disambiguator

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
<small>This (part of) documentation was generated from [../src/cg3/disambiguator.cg3](http://github.com/giellalt/lang-koi/blob/main/../src/cg3/disambiguator.cg3)</small>
INTRODUCTION TO MORPHOLOGICAL ANALYSER OF Komi-Permyak LANGUAGE.


# Definitions for Multichar_Symbols@CODE@




## Analysis symbols
The morphological analyses of wordforms for the Komi-Permyak
language are presented in this system in terms of the following symbols.
(It is highly suggested to follow existing standards when adding new tags).

The parts-of-speech tags are:
* **+Aadjective**:  adjective
* **+AdpAdposition**:  Adposition
* **+Advadverb**:  adverb
* **+CSconjunction**:  subordinating conjunction
* **+CCconjunction**:  coordinating conjunction
* **+Interjinterjection**:  interjection
* **+Nnoun**:  noun
* **+Pcleparticle**:  particle
* **+Popostposition**:  postposition
* **+Prpreposition**:  preposition
* **+Pronpronoun**:  pronoun
* **+QntQuantifier**:  Quantifier
* **+Vverb**:  verb



The parts of speech are further split up into:
Adjectives

Adverbs
These are ideophonic descriptors used to modify the verb
вырк ливтясь "**flit** and it flew off"
* **+DegAdA** Degree depricate AdA
Ad-adjective
with reference to type of adverb
spatial
temporal
multiplicative, i.e. iterations
* **+Parentheticphrase** parenthetical phrase

Interjections
  +Conative   Used for calling animals, for example

Nouns
proper
used with paired nouns **collective nouns**
* **+Relatув** relational noun: выв, ув

Postpositions

## Pronouns
* **+Demdemonstrative**:  demonstrative
* **+Indefindefinite**:  indefinite
* **+Interrinterrogative**:  interrogative
* **+Perspersonal**:  personal
* **+Reciprreciprocal**:  reciprocal
* **+Reflreflexive**:  reflexive
* **+Relrelative**:  relative

## Quantifiers (numerals)
Quantifiers and Numerals are classified under:
* **+Numnumeral**:  numeral
* **+Apprthree***:  Approximative numeral кавто-колмо, колмошка *two or three*
NB! do not confuse with Komi case +Apr
* **+AssocCollavide-**:  -ne- ; avide-
* **+Assoc+мезть**:  +мезть
* **+CardNCard**:  cardinal + NCard
* **+Collcollective**:  collective
* **+DistrDistributive**:  Distributive
* **+Iter`кыкысь`: Iterative form expressing number of times; kpv**:  `кыкысь`
* **+OrdNOrd**:  ordinal + NOrd
* **+Coordnumerals.lexc**:  Coordinates, i.e. 65˚36′8,30″ in numerals.lexc
* **+Copdepricated**:  this is for copula complement position with pl in -ӧсь Pred depricated


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
*  **+Cmplcomplement**  Postposition complement
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
* **»7»**:  Literal »
* **«7«**:  Literal «
```
  %[%>%]  - Literal >
  %[%<%]  - Literal <
```




The possession is marked as such:
ODD

The comparative forms are:
* **+Compcomparative**:  comparative
* **+Superlsuperlative**:  superlative
* **+Mdrbig'**:  moderative -моз, -кодь  'kind of, -ish' with reference to quality ыджыткодь 'rather big'
* **+Augbig'**:  augmentative, intensive -ӧв 'too X' with reference to quality ыджытӧв 'too big'
*  **+Der/AdvCompModof** Adverbial comparative modifier in моз Der/моз +MOZ  diminishing, kind of, sort of
*  **+Der/CompModof** comparative modifier in кодь Der/кодь ! diminishing, kind of, sort of

Numerals are classified under:

Verb moods are:
* **+Imprtimperative**:  imperative
* **+Indindicative**:  indicative
* **+Prs-ӧ**:  present      -ӧ
* **+Prt1-ис**:  preterite 1 -ис
* **+Prt2-ӧма**:  preterite 2 -ӧма
* **+Fut-ас**:  future      -ас
* **+PrecPrecative**:  Precative mood is a directive mood that signals that the utterance is a request. -ко on imperative forms equals Precative
Verb personal forms are:
Other verb forms are
Gerund This is used with derivations


* +Symbol© = independent symbols in the text stream, like £, €, ©
Special symbols are classified with:
The verbs are syntactically split according to transitivity:
Special multiword units are analysed with:
Non-dictionary words can be recognised with:

Question and Focus particles:


### Tags distinguishing different versions of the same lemma (before POS)
* +v1@CODE@
* +v2@CODE@
* +v3@CODE@
* +v4@CODE@
* +v5@CODE@
* +v6@CODE@
* +v7@CODE@
* +v8@CODE@
* +v9@CODE@
* +v10@CODE@
* +v11@CODE@
* +v12@CODE@
* +v13@CODE@
* +v14@CODE@
* +v15@CODE@

The Usage extents are marked using following tags:

Where do these come from source
* **+Src/F2015-09-08** foreign source apparently 2015-09-08
* **+Dimdiminutive** diminutive


* **+Sem/ActActivity** Activity
* **+Sem/AmountAmount** Amount
* **+Sem/AniAnimate** Animate
* **+Sem/AniprodProduct** Animal Product
* **+Sem/AntAntroponym** Antroponym
* **+Sem/Ant-FemAntroponym** Female Antroponym
* **+Sem/Ant-MalAntroponym** Male Antroponym
* **+Sem/BodyBodypart** Bodypart
* **+Sem/Body-abstrjierbmi** siellu, vuoig?a, jierbmi
* **+Sem/BuildBuilding** Building
* **+Sem/Build-partcloset** Part of Bulding, like the closet
* **+Sem/CatCategory** Category
* **+Sem/ClthClothes** Clothes
* **+Sem/Clth-jewlJewelery** Jewelery
* **+Sem/Clth-partsávdnji...** part of clothes, boallu, sávdnji...
* **+Sem/CtainContainer** Container
* **+Sem/Ctain-abstraccount** Abstract container like bank account
* **+Sem/Ctain-clth**@CODE@****
* **+Sem/CurrMoney** Currency like dollár, Not Money
* **+Sem/DanceDance** Dance
* **+Sem/DirGPS-kursa** Direction like GPS-kursa
* **+Sem/Domainactions)** Domain like politics, reindeerherding (a system of actions)
* **+Sem/DrinkDrink** Drink
* **+Sem/DummytagDummytag** Dummytag
* **+Sem/Eduevent** Educational event
* **+Sem/EventEvent** Event
* **+Sem/FeatÁrvu** Feature, like Árvu
* **+Sem/Feat-physfárda** Physiological feature, ivdni, fárda
* **+Sem/Feat-psychfeauture** Psychological feauture
* **+Sem/Feat-measrfeauture** Psychological feauture
* **+Sem/Femname** Female name
* **+Sem/FoodFood** Food
* **+Sem/Food-medMedicine** Medicine
* **+Sem/FurnFurniture** Furniture
* **+Sem/GameGame** Game
* **+Sem/Geomobject** Geometrical object
* **+Sem/GroupGroup** Animal or Human Group
* **+Sem/HumHuman** Human
* **+Sem/Hum-abstrabstract** Human abstract
* **+Sem/Hum-profprofessional** Human professional
* **+Sem/IdeolIdeology** Ideology
* **+Sem/LangLanguage** Language
* **+Sem/Malname** Male name
* **+Sem/Matthings** Material for producing things
* **+Sem/MeasrMeasure** Measure
* **+Sem/MoneyCurr(ency)** Has to do with money, like wages, not Curr(ency)
* **+Sem/ObjObject** Object
* **+Sem/Obj-cloCloth** Cloth
* **+Sem/Obj-cognCloth** Cloth
* **+Sem/Obj-elapparatus** (Electrical) machine or apparatus
* **+Sem/Obj-lingit** Object with something written on it
* **+Sem/Obj-ropeobject** flexible ropelike object
* **+Sem/Obj-surfcobject** Surface object
* **+Sem/OrgOrganisation** Organisation
* **+Sem/Partbealli** Feature, oassi, bealli
* **+Sem/PatrPatronymic** Patronymic
* **+Sem/Patr-FemPatronymic** Female Patronymic
* **+Sem/Patr-MalPatronymic** Male Patronymic
* **+Sem/Perc-cognperception** Cognative perception
* **+Sem/Perc-emoperception** Emotional perception
* **+Sem/Perc-physperception** Physical perception
* **+Sem/Perc-psychperception** Physical perception
* **+Sem/PlantPlant** Plant
* **+Sem/Plant-partpart** Plant part
* **+Sem/PlcPlace** Place
* **+Sem/Plc-abstrplace** Abstract place
* **+Sem/Plc-elevatePlace** Place
* **+Sem/Plc-linePlace** Place
* **+Sem/Plc-waterPlace** Place
* **+Sem/Posjob)** Position (as in social position job)
* **+Sem/ProcessProcess** Process
* **+Sem/ProdProduct** Product
* **+Sem/Prod-audioproduct** Audio product
* **+Sem/Prod-cognproduct** Cognition product
* **+Sem/Prod-lingproduct** Linguistic product
* **+Sem/Prod-visproduct** Visual product
* **+Sem/RelRelation** Relation
* **+Sem/RouteRoute** Name of a Route
* **+Sem/Ruleconvention** Rule or convention
* **+Sem/Semconconcept** Semantic concept
* **+Sem/Sign** Sign (e.g. numbers, punctuation) 
* **+Sem/SportSport** Sport
* **+Sem/State** 
* **+Sem/State-sickIllness** Illness
* **+Sem/SubstncWater** Substance, like Air and Water
* **+Sem/SurSurname** Surname
* **+Sem/Sur-FemSurname** Surname
* **+Sem/Sur-MalSurname** Surname
* **+Sem/SymbolSymbol** Symbol
* **+Sem/TimeTime** Time
* **+Sem/Toolthings** Prototypical tool for repairing things
* **+Sem/Tool-catchfish)** Tool used for catching (e.g. fish)
* **+Sem/Tool-cleancleaning** Tool used for cleaning
* **+Sem/Tool-itIT** Tool used in IT
* **+Sem/Tool-measrmeasuring** Tool used for measuring
* **+Sem/Tool-musicinstrument** Music instrument
* **+Sem/Tool-writetool** Writing tool
* **+Sem/Txtlávlla...)** Text (girji, lávlla...)
* **+Sem/VehVehicle** Vehicle
* **+Sem/WpnWeapon** Weapon
* **+Sem/Wthrground** The Weather or the state of ground





Semantics are classified with
* **+Sem/InanimInanimate,**  Inanimate,
* **+Sem/NonHumNonhuman,**  Nonhuman,


Derivations are classified under the morphophonetic form of the suffix, the
source and target part-of-speech.



* **+Der/ісьDer/ысь** Der/ысь







*  **+Der/PrivModAbeMod** privative or abessive modifier -тӧм AbeMod
*  **+Der/LocModIneMod** locative modifier са - IneMod
*  **+Der/ProprietiveModDer/а** habeo modifier HabObjMod Der/а
*  **+Der/TempMod-** temporal modifier ся -



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
|  @P.NeedNoun.ON@nominalised | (Dis)allow compounds with verbs unless nominalised
|  @D.NeedNoun.ON@nominalised | (Dis)allow compounds with verbs unless nominalised
|  @C.NeedNoun@nominalised | (Dis)allow compounds with verbs unless nominalised

For languages that allow compounding, the following flag diacritics are needed
to control position-based compounding restrictions for nominals. Their use is
handled automatically if combined with +CmpN/xxx tags. If not used, they will
do no harm.
|  @P.CmpFrst.FALSE@first | Require that words tagged as such only appear first
|  @D.CmpPref.TRUE@ENDLEX | Block such words from entering ENDLEX
|  @P.CmpPref.FALSE@compounds | Block these words from making further compounds
|  @D.CmpLast.TRUE@R | Block such words from entering R
|  @D.CmpNone.TRUE@compounding | Combines with the next tag to prohibit compounding
|  @U.CmpNone.FALSE@compounding | Combines with the prev tag to prohibit compounding
|  @P.CmpOnly.TRUE@R | Sets a flag to indicate that the word has passed R
|  @D.CmpOnly.FALSE@root. | Disallow words coming directly from root.

Use the following flag diacritics to control downcasing of derived proper
nouns (e.g. Finnish Pariisi -> pariisilainen). See e.g. North Sámi for how to use
these flags. There exists a ready-made regex that will do the actual down-casing
given the proper use of these flags.
|  @U.Cap.Obl@deatnulasj. | Allowing downcasing of derived names: deatnulasj.
|  @U.Cap.Opt@deatnulasj. | Allowing downcasing of derived names: deatnulasj.









FLAGS USED WITH COLLECTIVE NOUNS








Removal

|  @U.Cap.Obl@deatnulasj | Allowing downcasing of derived names: deatnulasj
|  @U.Cap.Opt@deatnulasj | Allowing downcasing of derived names: deatnulasj


The word forms in the KOMI-PERMYAK language start from the lexeme roots of basic

word classes, or optionally from prefixes:


Incoming from akusanat
Pron_koi2x ;


Incoming for conversion from kpv





























* * *
<small>This (part of) documentation was generated from [../src/fst/root.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/root.lexc)</small>
# Symbol affixes





* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/symbols.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/affixes/symbols.lexc)</small># Conjunctors
----
Komi conjunctors










* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/conjunctors.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/affixes/conjunctors.lexc)</small>Prefixes
Prefixes in the Komi-Permyak language are bound to the beginning of other words.



* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/prefixes.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/affixes/prefixes.lexc)</small># Particles
----
Komi Particles











* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/particles.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/affixes/particles.lexc)</small>
# Noun morphological lexica !


* **LEXICON Vocative**@CODE@****

* **LEXICON Noun1-IS_PTC-OMtags** is to provide deverbal nouns with +Der/ӧм tags

* **LEXICON Noun1-IS_PTC-AN**@CODE@****

* **LEXICON Noun1-IS_PTC-YSJ**@CODE@****








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



* **LEXICON CASEPOSSLEX**@CODE@****



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




































+Der/A+Adv:%>а K ;






* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/nouns.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/affixes/nouns.lexc)</small># Adjective inflection
----
Komi (Permyak) adjectives compare.

Continuation lexicon has been assigned according to <pos/> content























 * LEXICON A_PARAGOGIC-В/Л  юмов:юмо юмолӧсь
Singular predicative 





* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/adjectives.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/affixes/adjectives.lexc)</small># Pronominal morphology                           

## Closed class personal pronouns

* **LEXICON PERS** 
* **ме+Pron+Pers+Sg1:ме perssg1decl ;...** ...

* **ачым+Pron+Refl+Sg1:а REFLSG1DECL ;...** ...




* **LEXICON perssg1decl** 


* **LEXICON perspl1decl**@CODE@****


* **LEXICON perssg2decl**@CODE@****

* **LEXICON perspl2decl** 




* **LEXICON perssg3decl** 


ми мийӧ The 1st and 2nd persons have Oblique case stem strategies
that differ from the 3rd person: 
ті тійӧ nämä ovat aivan eri asioita?
сы сійӧ tosin joskus 

* **LEXICON perspl3decl**@CODE@****


* **LEXICON perssg**@CODE@****



* **LEXICON persplobl**@CODE@****


























































































































































Tagged in the src/morphology/stems/pronouns.xml file













* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/pronouns.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/affixes/pronouns.lexc)</small>

# Verbal morphology               





## Closed class verbs







## Open class verbs

Some Flag diacritic lines are with regexes, other with aligned zeros. We want to migrate to
regexes < … > , for readability reasons (sic!)

* **LEXICON V_LOKNYлокны:лок** One verb only, локны:лок

Begin work with TV and IV



* **LEXICON VR_SHUNY** 

* **LEXICON V_SHUNY-Vны.** шуны:шу янӧдны, контролируйтны. Ending in -дны, -тны, -Cны, -Vны.

* **LEXICON V_JUAYSHNYgradation** is there ш : шт gradation

* **LEXICON V_AMNY-дзны,** амны:ам Ending in -мны, -жны, -дзны,


* **LEXICON V_KYJNY** кыйны:кый Ending in -йны, 

* **LEXICON V_CHILOESNY2018-09-01** is there s : st alternation 2018-09-01


* **LEXICON V_KUTNY-Vны.** шуны:шу янӧдны, контролируйтны. Ending in -дны, -тны, -Cны, -Vны.


* **LEXICON V_NUAVNYнуавны:нуа** нуавны:нуа
Consonant-onset


* **LEXICON V_ARTASJNY-Cны.** артасьны:артас -Cны.

* **LEXICON VR_LYDDJYNY** 

* **LEXICON V_LYDDJYNY-ыны.** лыддьыны:лыддьы ! ярмыны. Multiple-syllable verb ending in -ыны.


* **LEXICON V_VOLYNY-ыны.** волыны:волы ! ярмыны. Multiple-syllable verb ending in -ыны.








## Verb conjugation 

* **LEXICON VerbConj-V**  суф б -- ы 

* **LEXICON VerbConjа** суф а

* **LEXICON VerbConj_KYJNYа** суф а

* **LEXICON VerbConj_AMNYа** суф а

* **LEXICON VerbConj_KUTNYа** суф а


* **LEXICON Finiteformstenses** Gives linking vowels for 3 tenses

* **LEXICON Finiteforms_KYJNYtenses** Gives linking vowels for 3 tenses

* **LEXICON Finiteforms_AMNYtenses** Gives linking vowels for 3 tenses

* **LEXICON Finiteforms_KUTNYtenses** Gives linking vowels for 3 tenses













* **@U.CONJ-MX.IMP@@U.CONJ-NX.PL@@U.CONJ-PX.2@+Imprt+Pl2:@U.CONJ-MX.IMP@@U.CONJ-NX.PL@@U.CONJ-PX.2@%>ӧ VerbEnd ;-ӧй** kpv -ӧй













Differs from kpv 2016-09-15









## Derivation


* **LEXICON Verb-nyDer** 

* **LEXICON Verb-nyDer-ONSET-CONSconsonant** Derivation onset in consonant
verb-to-verb

This is fed by LEXICON V_SHUNY, and therefore certain corrections
must be made 2012-01-18

овсьыны
пусьыштлывлыны
босьтчыштлывлыны

* **LEXICON Verb-nyDer-ONSET-VOWvowel** Derivation onset	in vowel

* **LEXICON Verb-nyDer-ONSET-Yvowel** Derivation onset	in vowel

* **LEXICON Verb-nyDer-ONSET-Avowel** Derivation onset	in vowel
босьтасьны

* **LEXICON Verb-nyDer-ONSET-JAvowel** Derivation onset	in vowel
босьтасьны


verb-to-noun

* **LEXICON VerbDer** 
FIX THIS 2015-09-06

* **LEXICON VerbDer_KYJNY**@CODE@****
* **:й VerbDer-ONSET_OE ;**@CODE@****
* **:й VerbDer-ONSET_JA ;** 
* **:й VerbDer-ONSET_JI ;**@CODE@****

* **LEXICON VerbDer_KUTNY**@CODE@****
* **VerbDer-ONSET_OE ;**@CODE@****
* **VerbDer-ONSET_A ;** 
* **VerbDer-ONSET_JI ;**@CODE@****

* **LEXICON VerbDer_ARTASJNY**@CODE@****
* **: VerbDer-ONSET_OE ;**@CODE@****
* **: VerbDer-ONSET_JA ;** 
* **: VerbDer-ONSET_JI ;**@CODE@****

* **LEXICON VerbDer-ONSET_OE** 
* **+Der/ісь+ActPrsPtc:%>%{иі%}сь N_ ;ысь** kpv ысь

* **LEXICON VerbDer-ONSET_JI** 


* **LEXICON VerbDer-ONSET_A** 

* **LEXICON VerbDer-ONSET_JA** 










вевттьысьыны

бертласьны
















* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/verbs.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/affixes/verbs.lexc)</small>

# Numeral morphological lexica 











LEXICON NUM-APPR ! 2011-11-03 This will need work



## Inflectional lexica 

All nouns follow one contlex "Noun1"
to begin with here is simply a list of all variant
with no more variants beyond:
















































## Arabic numerals



 * **LEXICON ARABIC          ** 








* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/numerals.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/affixes/numerals.lexc)</small># Adverb inflection
----
Komi adverbs inflect for direction.






















 * **LEXICON ADV-SPAT  **
these are adverbs in spatial cases
and they probably are equivalent in morphology to postpositions






























* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/adverbs.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/affixes/adverbs.lexc)</small># Postposition inflection
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





















* * *
<small>This (part of) documentation was generated from [../src/fst/affixes/adpositions.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/affixes/adpositions.lexc)</small>Proper noun inflection

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
<small>This (part of) documentation was generated from [../src/fst/affixes/propernouns.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/affixes/propernouns.lexc)</small>=================================== !
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


* * *
<small>This (part of) documentation was generated from [../src/fst/phonology.twolc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/phonology.twolc)</small>This is where new words from kpv are initially shown





These are koi verbs



* * *
<small>This (part of) documentation was generated from [../src/fst/stems/verbs_newwords.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/stems/verbs_newwords.lexc)</small>This is where new words from kpv are initially shown

2016-07-14







* * *
<small>This (part of) documentation was generated from [../src/fst/stems/nouns_newwords.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/stems/nouns_newwords.lexc)</small>Nouns
Nouns in the Komi Permyak language are things.






* * *
<small>This (part of) documentation was generated from [../src/fst/stems/nouns.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/stems/nouns.lexc)</small>Adjectives
Adjectives in Komi-Permyak language describe things.



* * *
<small>This (part of) documentation was generated from [../src/fst/stems/adjectives.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/stems/adjectives.lexc)</small>Pronouns
Pronouns in KOMI PERMYAK language are references to things.



* * *
<small>This (part of) documentation was generated from [../src/fst/stems/pronouns.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/stems/pronouns.lexc)</small>This is where new words are added as lexc entries before they are 
added to the xml source files.
Абъячой+N+Prop+Sem/Plc:Абъячой PROP_ "(eng) fish/(fin) /(rus)" ;


ADD NOUNS BELOW






* * *
<small>This (part of) documentation was generated from [../src/fst/stems/kom-rus-propernouns_newwords.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/stems/kom-rus-propernouns_newwords.lexc)</small>This is where new words from kpv are initially shown







* * *
<small>This (part of) documentation was generated from [../src/fst/stems/adjectives_newwords.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/stems/adjectives_newwords.lexc)</small>This is where new words from kpv are initially shown








* * *
<small>This (part of) documentation was generated from [../src/fst/stems/adverbs_newwords.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/stems/adverbs_newwords.lexc)</small>This is where new words from kpv are initially shown



* * *
<small>This (part of) documentation was generated from [../src/fst/stems/numerals_newwords.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/stems/numerals_newwords.lexc)</small>Numerals
Numerals in the KOMI-PERMYAK language are numbers.




* * *
<small>This (part of) documentation was generated from [../src/fst/stems/numerals.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/stems/numerals.lexc)</small>This is where new words from kpv are initially shown




* * *
<small>This (part of) documentation was generated from [../src/fst/stems/pronouns_newwords.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/fst/stems/pronouns_newwords.lexc)</small>


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
<small>This (part of) documentation was generated from [../src/transcriptions/transcriptor-abbrevs2text.lexc](http://github.com/giellalt/lang-koi/blob/main/../src/transcriptions/transcriptor-abbrevs2text.lexc)</small>
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
QMARK
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

HAB-ACTOR
HAB-ACTOR-NOT-HUMAN


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
REAL-WORD
REAL-WORD-NOT-ABBR
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
<small>This (part of) documentation was generated from [../tools/grammarcheckers/grammarchecker.cg3](http://github.com/giellalt/lang-koi/blob/main/../tools/grammarcheckers/grammarchecker.cg3)</small>