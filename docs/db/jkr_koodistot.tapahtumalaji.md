# jkr_koodistot.tapahtumalaji

## Description

## Columns

| Name | Type | Default | Nullable | Children | Parents | Comment |
| ---- | ---- | ------- | -------- | -------- | ------- | ------- |
| koodi | text |  | false |  |  |  |
| selite | text |  | true |  |  |  |

## Constraints

| Name | Type | Definition |
| ---- | ---- | ---------- |
| tapahtumalaji_pk | PRIMARY KEY | PRIMARY KEY (koodi) |

## Indexes

| Name | Definition |
| ---- | ---------- |
| tapahtumalaji_pk | CREATE UNIQUE INDEX tapahtumalaji_pk ON jkr_koodistot.tapahtumalaji USING btree (koodi) |

## Relations

![er](jkr_koodistot.tapahtumalaji.svg)

---

> Generated by [tbls](https://github.com/k1LoW/tbls)