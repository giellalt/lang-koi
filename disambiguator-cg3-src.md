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
<small>This (part of) documentation was generated from [../src/cg3/disambiguator.cg3](http://github.com/giellalt/lang-koi/blob/main/../src/cg3/disambiguator.cg3)</small>