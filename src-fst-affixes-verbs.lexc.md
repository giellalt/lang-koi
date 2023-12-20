

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

<small>This (part of) documentation was generated from [src/fst/affixes/verbs.lexc](https://github.com/giellalt/lang-koi/blob/main/src/fst/affixes/verbs.lexc)</small>

---

