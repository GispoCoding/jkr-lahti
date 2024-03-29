# jkr.jatteenkuljetusalue

## Description

Jätteenkuljetusalueet sisältävä taulu.  
Jätteenkuljetusalueiden ulkopuoliset kiinteistöt liittyvät aluejätekeräykseen.

## Columns

| Name | Type | Default | Nullable | Children | Parents | Comment |
| ---- | ---- | ------- | -------- | -------- | ------- | ------- |
| id | integer | nextval('jkr.jatteenkuljetusalue_id_seq'::regclass) | false |  |  |  |
| geom | geometry(MultiPolygon,3067) |  | true |  |  | Jätteenkuljetusalueen geometria |
| nimi | text |  | true |  |  |  |

## Constraints

| Name | Type | Definition |
| ---- | ---- | ---------- |
| jatteenkuljetusalue_pk | PRIMARY KEY | PRIMARY KEY (id) |

## Indexes

| Name | Definition |
| ---- | ---------- |
| jatteenkuljetusalue_pk | CREATE UNIQUE INDEX jatteenkuljetusalue_pk ON jkr.jatteenkuljetusalue USING btree (id) |
| idx_jatteenkuljetusalue_geom | CREATE INDEX idx_jatteenkuljetusalue_geom ON jkr.jatteenkuljetusalue USING gist (geom) |

## Relations

![er](jkr.jatteenkuljetusalue.svg)

---

> Generated by [tbls](https://github.com/k1LoW/tbls)
