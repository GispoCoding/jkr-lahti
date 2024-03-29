# jkr_koodistot.rakennuksenkayttotarkoitus

## Description

Taulu, joka sisältää mahdolliset rakennuksen käyttötarkoitukset

## Columns

| Name | Type | Default | Nullable | Children | Parents | Comment |
| ---- | ---- | ------- | -------- | -------- | ------- | ------- |
| koodi | text |  | false | [jkr.rakennus](jkr.rakennus.md) |  | Taulun avaimena toimiva uniikki tekstimuotoinen tunniste |
| selite | text |  | false |  |  | Kuvaus tietyn tunnisteen omaavasta rakennuksen käyttötarkoituksesta |

## Constraints

| Name | Type | Definition |
| ---- | ---- | ---------- |
| rakennuksenkayttotarkoitus_pk | PRIMARY KEY | PRIMARY KEY (koodi) |

## Indexes

| Name | Definition | Comment |
| ---- | ---------- | ------- |
| idx_rakennuksenkayttotarkoitus_selite | CREATE INDEX idx_rakennuksenkayttotarkoitus_selite ON jkr_koodistot.rakennuksenkayttotarkoitus USING btree (selite) | factassa duplikaattiselitteitä, ei voida käyttää uniikkiindeksiä |
| rakennuksenkayttotarkoitus_pk | CREATE UNIQUE INDEX rakennuksenkayttotarkoitus_pk ON jkr_koodistot.rakennuksenkayttotarkoitus USING btree (koodi) |  |

## Relations

![er](jkr_koodistot.rakennuksenkayttotarkoitus.svg)

---

> Generated by [tbls](https://github.com/k1LoW/tbls)
