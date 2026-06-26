# Lemma-tests for *verbs* in ...`verbs.lexc`


**айда** failures:

* `айда+V+Inf` does not generate!
* `айда` has following analyses:
  * `айда+V+WORK`

**жагыт** failures:

* `жагыт+V+Inf` does not generate!
* `жагыт` has following analyses:
  * `жагыт+Hom2`
  * `жаг+A+Der+Der/MWN+N+Sg+Nom+PxSg2`
  * `жагыт+Hom2+Der+Der/MWN+N+Sg+Nom`

**шонтіcьыштлыны** failures:

* `шонтіcьыштлыны+V+Inf` => `шонтіcьышвыны`
* `шонтіcьыштлыны` has no analyses either

**шонтіcьлыны** failures:

* `шонтіcьлыны+V+Inf` => `шонтіcьвыны`
* `шонтіcьлыны` has no analyses either

**быръялны** failures:

* `быръялны+V+Inf` does not generate!
* `быръялны` has no analyses either

**тӧждіcьлывлыны** failures:

* `тӧждіcьлывлыны+V+Inf` => `тӧждіcьвыввыны`
* `тӧждіcьлывлыны` has no analyses either

**поздіcьлыны** failures:

* `поздіcьлыны+V+Inf` => `поздіcьвыны`
* `поздіcьлыны` has no analyses either

**ны** failures:

* `ны+V+Inf` does not generate!
* `ны` has following analyses:
  * `ны+Hom2+Interj`
  * `сія+Pron+Pers+Pl3`
  * `ны+Imprt+Sg2`
  * `ны+ConNeg`

**бырлывлыны** failures:

* `бырлывлыны+V+Inf` => `бырлыллыны`
* `бырлывлыны+V+Inf` => `бырвыввыны`
* `бырлывлыны` has no analyses either

**ылӧcмывлыны** failures:

* `ылӧcмывлыны+V+Inf` => `ывӧcмыввыны`
* `ылӧcмывлыны` has no analyses either

**садіcьлыны** failures:

* `садіcьлыны+V+Inf` => `садіcьвыны`
* `садіcьлыны` has no analyses either

**на** failures:

* `на+V+Inf` does not generate!
* `на` has following analyses:
  * `на+Adp+Pr`
  * `на+Hom1+Adv`
  * `на+Hom2+Adv`
  * `на+Adv`
  * `на+V+WORK`

## Lemma statistics
* 7649 lemmas
* 99.77774872532356 % success

## Settings used

```json
{
    "adjectives": {
        "lemmatags": [
            "+A+Sg+Nom"
        ],
        "lexcfile": ".../adjectives.lexc"
    },
    "analyser": ".../analyser-gt-norm.hfstol",
    "generator": ".../generator-gt-norm.hfstol",
    "nouns": {
        "lemmatags": [
            "+N+Sg+Nom",
            "+N+Pl+Nom"
        ],
        "lexcfile": ".../nouns.lexc"
    },
    "propernouns": {
        "lemmatags": [
            "+N+Prop+Sg+Nom"
        ],
        "lexcfile": ".../propernouns.lexc"
    },
    "verbs": {
        "lemmatags": [
            "+V+Inf"
        ],
        "lexcfile": ".../verbs.lexc"
    }
}
```
