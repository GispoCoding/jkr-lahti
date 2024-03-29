# jkr.v_sopimukset

## Description

Apunäkymä velvoitekyselyille. Sisältää mm. jätetyypin selitteen.

<details>
<summary><strong>Table Definition</strong></summary>

```sql
CREATE VIEW v_sopimukset AS (
 SELECT s.id AS sopimus_id,
    s.kohde_id,
    jt.selite AS jatetyyppi_selite,
    s.voimassaolo AS sopimus_voimassaolo,
    s.kimppaisanta_kohde_id
   FROM (jkr.sopimus s
     JOIN jkr_koodistot.jatetyyppi jt ON ((jt.id = s.jatetyyppi_id)))
)
```

</details>

## Referenced Tables

- [jkr.sopimus](jkr.sopimus.md)
- [jkr_koodistot.jatetyyppi](jkr_koodistot.jatetyyppi.md)

## Columns

| Name | Type | Default | Nullable | Children | Parents | Comment |
| ---- | ---- | ------- | -------- | -------- | ------- | ------- |
| sopimus_id | integer |  | true |  |  |  |
| kohde_id | integer |  | true |  |  |  |
| jatetyyppi_selite | text |  | true |  |  |  |
| sopimus_voimassaolo | daterange |  | true |  |  |  |
| kimppaisanta_kohde_id | integer |  | true |  |  |  |

## Relations

![er](jkr.v_sopimukset.svg)

---

> Generated by [tbls](https://github.com/k1LoW/tbls)
