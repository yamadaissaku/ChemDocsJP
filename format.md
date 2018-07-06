# ファイル形式

* .smi
    * SMILESを格納、複数行にSMILESを記載することで一つのファイルに複数の化学構造を記述することができる。

```
CO
CCO
OCCC
C1CCCCC1
C2=CC=CC=C2
```

[![Image from Gyazo](https://i.gyazo.com/3dba74f046db054537dd620752484de1.png)](https://gyazo.com/3dba74f046db054537dd620752484de1)

---

* .mol

```
887
  -OEChem-07031813262D

  6  5  0     0  0  0  0  0  0999 V2000
    2.5369   -0.2500    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
    3.4030    0.2500    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    3.7130   -0.2869    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
    3.9399    0.5600    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
    3.0930    0.7869    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
    2.0000    0.0600    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
  1  2  1  0  0  0  0
  1  6  1  0  0  0  0
  2  3  1  0  0  0  0
  2  4  1  0  0  0  0
  2  5  1  0  0  0  0
M  END
```

[![Image from Gyazo](https://i.gyazo.com/80b795c3979bead01535bde52d9c863b.png)](https://gyazo.com/80b795c3979bead01535bde52d9c863b)

---

* .sdf

```
887
  -OEChem-07031813262D

  6  5  0     0  0  0  0  0  0999 V2000
    2.5369   -0.2500    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
    3.4030    0.2500    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    3.7130   -0.2869    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
    3.9399    0.5600    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
    3.0930    0.7869    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
    2.0000    0.0600    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
  1  2  1  0  0  0  0
  1  6  1  0  0  0  0
  2  3  1  0  0  0  0
  2  4  1  0  0  0  0
  2  5  1  0  0  0  0
M  END
> <PUBCHEM_COMPOUND_CID>
887

> <PUBCHEM_IUPAC_INCHI>
InChI=1S/CH4O/c1-2/h2H,1H3

> <PUBCHEM_IUPAC_INCHIKEY>
OKKJLVBELUTLKV-UHFFFAOYSA-N

$$$$
888
  -OEChem-07031813262D

  6  5  0     0  0  0  0  0  0999 V2000
    2.5369   -0.2500    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
    ...
    ...
$$$$
```


[![Image from Gyazo](https://i.gyazo.com/4eecaa26d46c6eb4840f829507578677.png)](https://gyazo.com/4eecaa26d46c6eb4840f829507578677)

* [他の形式例](http://openbabel.org/docs/2.3.0/FileFormats/Overview.html)