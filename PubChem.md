# PubChemの使い方

# PubChem

* PubChemとは？



    * 統合TVを見てみましょう
        * [2017-12-08 PubChemを利用して化学物質やアッセイの結果を調べる 2017]( http://togotv.dbcls.jp/20171208.html)
            * http://togotv.dbcls.jp/20171208.html
[![Image from Gyazo](https://i.gyazo.com/dd9616fac93a903519ba6e8e7cca85fc.png)](https://gyazo.com/dd9616fac93a903519ba6e8e7cca85fc)

* [Compound, Substance, BioAssay](https://pubchemdocs.ncbi.nlm.nih.gov/about)

    * Substance   SID (SubstanceID)
    * Compound    CID (CompoundID)
    * BioAssay    AID (AssayID)

        [![Image from Gyazo](https://i.gyazo.com/1be913ae900eaca8772cdfde5bca42c2.png)](https://gyazo.com/1be913ae900eaca8772cdfde5bca42c2)

* [Data Sources](https://pubchem.ncbi.nlm.nih.gov/sources)

* [Chemical structure representation in PubChem](https://www.slideshare.net/NextMoveSoftware/chemical-structure-representation-in-pubchem?from_action=save)

---

## ブラウザからの利用

### 化合物のページ

* [ゲフィチニブ（Gefitinib)](https://pubchem.ncbi.nlm.nih.gov/compound/123631#section=Top)

* [beta-D-Glucopyranose](https://pubchem.ncbi.nlm.nih.gov/compound/beta-D-glucose#section=Top)

---

### データの取得方法

## [PubChem’s PUG (Power User Gateway)](http://pubchemdocs.ncbi.nlm.nih.gov/programmatic-access)

* [PUG-REST](https://pubchemdocs.ncbi.nlm.nih.gov/pug-rest)

    * URL

    `https://pubchem.ncbi.nlm.nih.gov/rest/pug/<input specification>/<operation specification>/[<output specification>][?<operation_options>]`

    * レコード検索

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sourceid/DTP.NCI/747285/SDF

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sourceid/DTP.NCI/747285/PNG

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/SDF

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/PNG

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/SDF?record_type=3d

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/PNG?record_type=3d&image_size=small

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/name/aspirin/SDF

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/inchikey/BPGDAMSIGCZZLK-UHFFFAOYSA-N/SDF

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/1000/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/1000/CSV?sid=26736081,26736082,26736083

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/1000/concise/CSV

    * Compound Property Tables

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1,2,3,4,5/property/MolecularFormula,MolecularWeight,InChIKey/CSV

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1,2,3,4,5/property/MolecularFormula,MolecularWeight,InChIKey/JSON

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1,2,3,4,5/property/IsomericSMILES,XLogP,TPSA,HBondDonorCount,HBondAcceptorCount,RotatableBondCount,AtomStereoCount,BondStereoCount/JSON

    * Synonyms

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/name/aspirin/synonyms/JSON

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/smiles/CCCC/synonyms/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sid/53789435/synonyms/TXT

    * Description

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1983/description/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1983/description/JSON


    * SIDS / CIDS / AIDS

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/name/glucose/sids/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/name/glucose/sids/XML?list_return=listkey

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/name/glucose/cids/XML?list_return=grouped

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/name/glucose/cids/XML?list_return=flat

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sourceall/MLSMR/sids/JSON?list_return=listkey

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sourceall/R%26D%20Chemicals/sids/XML?list_return=listkey

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sid/123061,123079/cids/XML?cids_type=all

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/sids/JSON

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/192180/cids/TXT?cids_type=component

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/aids/JSON?aids_type=active

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/sids/JSON?sids_type=component

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/cids/TXT?cids_type=same_connectivity

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/21145249/cids/XML?cids_type=parent

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/1000/sids/XML?sids_type=inactive

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/504526/sids/JSON?sids_type=doseresponse

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/type/doseresponse/aids/JSON

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/sourceall/DTP.NCI/aids/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/xref/PatentID/EP0711162A1/sids/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/name/myxalamid/cids/XML?name_type=word

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/name/myxalamid/cids/XML?name_type=complete

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/target/genesymbol/USP2/aids/TXT

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/target/gi/116516899/aids/JSON

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/activity/EC50/aids/TXT

    * Assay Description

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/490/description/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/490/description/JSON

    * Assay Targets

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/490,1000/targets/ProteinGI,ProteinName,GeneID,GeneSymbol/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/490,1000/targets/ProteinGI,ProteinName,GeneID,GeneSymbol/JSON

    * Assay Summary

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1000,1001/assaysummary/CSV

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sid/104234342/assaysummary/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sid/104234342/assaysummary/JSON

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/1000/summary/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/1000/summary/JSON

    * Assay Dose-Response

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/504526/doseresponse/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/504526/doseresponse/CSV?sid=104169547,109967232

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/602332/sids/XML?sids_type=doseresponse&list_return=listkey

    * Classification

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sid/1917/classification/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1983/classification/JSON?classification_type=original

    * XRefs

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sid/127378063/xrefs/PatentID/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/name/vioxx/xrefs/RegistryID,RN,PubMedID/JSONP

    * Example Scripts

        * [pug_rest_scripts_nar_2018.zip](https://pubchemdocs.ncbi.nlm.nih.gov/pug-rest$example_scripts)

---

* [PUG-SOAP](https://pubchemdocs.ncbi.nlm.nih.gov/pug-soap)

    * web service definition language (WSDL)
        * https://pubchem.ncbi.nlm.nih.gov/pug_soap/pug_soap.cgi?wsdl
    * PUG SOAP Client Help
        * https://pubchem.ncbi.nlm.nih.gov/pug_soap/client_help.html

        [![Image from Gyazo](https://i.gyazo.com/48e67fd5c2f87368065df64cc65a417d.png)](https://gyazo.com/48e67fd5c2f87368065df64cc65a417d)

---


## [PubChemRDF](http://pubchemdocs.ncbi.nlm.nih.gov/rdf)

*  RESTful Interface

    `curl -L -H "Accept: text/rdf" -o CID2244.rdf http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244`

    http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244.rdf

    http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244.html

    http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244.turtle

    http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244.json

    http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244.jsonld

    http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244.ntriples

* Query RESTful Interface

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=synonym&name=aspirin

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=synonym&name=aspirin&contain=true

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=synonym&name=aspirin&return=compound

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=synonym&name=aspirin&format=json

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=substance&predicate=rdf:type&offset=10000

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=synonym&pred=rdf:type&obj=sio:CHEMINF_000561

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=synonym&pred=rdf:type&object=sio:CHEMINF_000446,sio:CHEMINF_000447&offset=1275000

---

* [Classification Browser](https://pubchem.ncbi.nlm.nih.gov/classification/#hid=1)

        * オントロジーや分類法から、化合物のデータセットを絞り込み、絞り込んだデータセットをダウンロードすることができます。
    
    1. 右の`Classification`をクリック
    [![Image from Gyazo](https://i.gyazo.com/02deb07e9c325c38e1a845427a839e2f.png)](https://gyazo.com/02deb07e9c325c38e1a845427a839e2f)

    2. `Select classification`から、データセットを選ぶ。
    [![Image from Gyazo](https://i.gyazo.com/8171df0099bdaaebae99420f83521439.png)](https://gyazo.com/8171df0099bdaaebae99420f83521439)

    3. 今回はChEBIを選択してみます。
    [![Image from Gyazo](https://i.gyazo.com/c3db102bfc7449a9266358e1c293a5e2.png)](https://gyazo.com/c3db102bfc7449a9266358e1c293a5e2)

    4. `Data type counts to display`で、`Substance`と`Compound`を切り替えると、下のカウントの数値が変わります。

    5. Treeの ▶ をクリックして、目的のセットを探します。
    [![Image from Gyazo](https://i.gyazo.com/af8d4ddf8e5f2a03bd0cdbcc24104e41.png)](https://gyazo.com/af8d4ddf8e5f2a03bd0cdbcc24104e41)

    6. 5.以外の方法として、`Search selected classification by`で、`Keyword`を選択（デフォルト）で、キーワード（ここでは、`glycolipid`）を入力し`Search`します。
    [![Image from Gyazo](https://i.gyazo.com/ec239987348227ce88abf784c43a002d.png)](https://gyazo.com/ec239987348227ce88abf784c43a002d)

    7. `Classification`の左のプラスのアイコンをクリックします。
    [![Image from Gyazo](https://i.gyazo.com/b512fa324124aade67907f5c7bf4ef5f.png)](https://gyazo.com/b512fa324124aade67907f5c7bf4ef5f)

    8. 展開された状態で、ブラウザの検索機能で`glycolipid`を検索します。
    [![Image from Gyazo](https://i.gyazo.com/1ee1f5b22e78d8e17aaddc6b4f87147b.png)](https://gyazo.com/1ee1f5b22e78d8e17aaddc6b4f87147b)

    9. 検索した`glycolipid`をクリックすると、ウインドウが開きます。`glycolipid`の左の青い数字をクリックします。
    [![Image from Gyazo](https://i.gyazo.com/0295c4554e5a972adb45b8930f7135f3.png)](https://gyazo.com/0295c4554e5a972adb45b8930f7135f3)

    10. 検索（選択）された化合物のリストが表示されます。右の`Structure Download`をクリックします。
    [![Image from Gyazo](https://i.gyazo.com/9b0d71c3e5475c34b26095a11c0f7d37.png)](https://gyazo.com/9b0d71c3e5475c34b26095a11c0f7d37)

    11. 検索（選択）した化合物のリストをダウンロードするためのサイトが開きます。必要に応じでformatなどを変更し、`Download`ボタンを押します。
    [![Image from Gyazo](https://i.gyazo.com/c6747251202079b73f1849eacc58f11a.png)](https://gyazo.com/c6747251202079b73f1849eacc58f11a)

    12. 自動的に選択した形式でデータのダウンロードが開始されます。この場合は、ファイル名`4363722229543774033.sdf.gz`としてダウンロードされます。
    [![Image from Gyazo](https://i.gyazo.com/2fee934fcd9fbac02c1e830c6724674e.png)](https://gyazo.com/2fee934fcd9fbac02c1e830c6724674e)

    13. ダウンロードされたファイルを解凍すると、エディタなどでデータを見ることができます。

    14. データセットとして、`Gene Ontology:　biological process`を選択してみます。Data typeとして、PubMed, Gene, Protein, Taxonomyが選択できるようになります。
    [![Image from Gyazo](https://i.gyazo.com/99754ac29478b468acd7dfe9231efa9e.png)](https://gyazo.com/99754ac29478b468acd7dfe9231efa9e)

    15. ここでは、Geneを選択し、Biological Process > metabolic process > glycosylation を選択してみます。

        [![Image from Gyazo](https://i.gyazo.com/91d7521e82dc98bafcb326d58e262eca.png)](https://gyazo.com/91d7521e82dc98bafcb326d58e262eca)

    16. glycosylationの右の「520」をクリックすると、新しいウインドウが開きます。Geneのリストが表示されます。Gene IDのリンクをクリックすると詳細画面を見ることができます。
    [![Image from Gyazo](https://i.gyazo.com/e04dbd581ed4173fd9664d4b7040c486.png)](https://gyazo.com/e04dbd581ed4173fd9664d4b7040c486)

    * SDFを選択した場合の例

        ```
        350080125
        -OEChem-07041809452D

        59 60  0     1  0  0  0  0  0999 V2000
        15.5021  -26.1389    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
        17.2204  -26.1388    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
        ...
        13.7741  -22.6873    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
        14.6327  -23.1842    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
        1 12  1  0  0  0  0
        1 15  1  0  0  0  0
        ...
        56 57  1  0  0  0  0
        57 58  1  0  0  0  0
        58 59  1  0  0  0  0
        M  END
        ...
        > <PUBCHEM_SUBSTANCE_ID>
        350080125

        > <PUBCHEM_EXT_DATASOURCE_NAME>
        ChEBI

        > <PUBCHEM_EXT_DATASOURCE_REGID>
        CHEBI:139221

        > <PUBCHEM_SUBSTANCE_SYNONYM>
        CHEBI:139221
        N-[(1S,2S,3R)-1-[(alpha-D-galactopyranosyloxy)methyl]-2,3-dihydroxy-10-phenyldecyl]hexacosanamide
        N-[(2S,3S,4R)-1-(alpha-D-galactopyranosyloxy)-3,4-dihydroxy-11-phenylundecan-2-yl]hexacosanamide
        N-[(2S,3S,4R)-1-(alpha-D-galactosyloxy)-3,4-dihydroxy-11-phenylundecan-2-yl]hexacosanamide

        ...

        $$$$
        350080124
        -OEChem-07041809452D
        ...
        ```

    * SMILESを選択した場合の例
        * 化学構造がSMILESへ変換できない場合は、ID(SID)のみ出力されます。
    [![Image from Gyazo](https://i.gyazo.com/941f927ef7619cc3d7254e49fa79accb.png)](https://gyazo.com/941f927ef7619cc3d7254e49fa79accb)

        ```
        350080125 CCCCCCCCCCCCCCCCCCCCCCCCCC(=O)N[C@@H](CO[C@@H]1[C@@H]([C@H]([C@H]([C@H](O1)CO)O)O)O)[C@@H]([C@@H](CCCCCCCC2=CC=CC=C2)O)O
        350080124 CC(CC/C=C(\C)/CC/C=C(\C)/CC/C=C(\C)/CCC=C(C)C)CCOP(=O)(O)OP(=O)(O)O[C@@H]1[C@@H]([C@H]([C@@H]([C@H](O1)CO)O[C@H]2[C@@H]([C@H]([C@@H]([C@H](O2)CO)O[C@H]3[C@H]([C@H]([C@@H]([C@H](O3)CO[C@@H]4[C@H]([C@H]([C@@H]([C@H](O4)CO[C@@H]5[C@H]([C@H]([C@@H]([C@H](O5)CO)O)O)O[C@@H]6[C@H]([C@H]([C@@H]([C@H](O6)CO)O)O)O)O)O[C@@H]7[C@H]([C@H]([C@@H]([C@H](O7)CO)O)O)O[C@@H]8[C@H]([C@H]([C@@H]([C@H](O8)CO)O)O)O)O)O)O[C@@H]9[C@H]([C@H]([C@@H]([C@H](O9)CO)O)O)O[C@@H]1[C@H]([C@H]([C@@H]([C@H](O1)CO)O)O)O[C@@H]1[C@H]([C@H]([C@@H]([C@H](O1)CO)O)O)O)O)O)NC(=O)C)O)NC(=O)C
        332875751 
        329737157 CCCCCCCCCCCCCCCCCCCCCCCC(=O)N[C@@H](CO[C@H]1[C@@H]([C@H]([C@@H]([C@H](O1)CO)O[C@H]2[C@@H]([C@H]([C@H]([C@H](O2)CO)O[C@H]3[C@@H]([C@H]([C@H]([C@H](O3)CO)O)O)NC(=O)C)O[C@@]4(C[C@@H]([C@H](C(O4)[C@@H]([C@@H](CO)O[C@@]5(C[C@@H]([C@H](C(O5)[C@@H]([C@@H](CO)O)O)NC(=O)C)O)C(=O)O)O)NC(=O)C)O)C(=O)O)O)O)O)[C@@H](/C=C/CCCCCCCCCCCCC)O
        ...
        ```

    ---

* PubChem FTP

    * FTPサイトからデータセットをダウンロードすることができます。
    
    1. 右の`PubChem FTP`をクリック
    
    [![Image from Gyazo](https://i.gyazo.com/02deb07e9c325c38e1a845427a839e2f.png)](https://gyazo.com/02deb07e9c325c38e1a845427a839e2f)
    
    2. FTPサイトが表示されます。
    
    [![Image from Gyazo](https://i.gyazo.com/4ae0fb53636aa99a62b41acbf879a607.png)](https://gyazo.com/4ae0fb53636aa99a62b41acbf879a607)

    3. アッセイデータの例、AID-AID.zip のリストが表示されます。必要なデータをクリックするとダウンロードできます。
    
    [![Image from Gyazo](https://i.gyazo.com/d567b89af9b67ed9931f02604f42d864.png)](https://gyazo.com/d567b89af9b67ed9931f02604f42d864)

    4. 以下のようにディレクトリをたどると、Compoundの2018-06-28更新データをSDF形式でダウンロードできます。ダウンロードしたデータは、上述のように解凍することでエディタなどでデータを見ることができます。
    
    [![Image from Gyazo](https://i.gyazo.com/fa193c7fc567a0591ddcd05a53de847e.png)](https://gyazo.com/fa193c7fc567a0591ddcd05a53de847e)

---

# 6. ツール

* 化合物をコンピュータで扱うためのソフトウェア

    ---

    * 分子表示

        * PubChem 3D Viewer
            * 右の`3D Conformer Tools`をクリック

        [![Image from Gyazo](https://i.gyazo.com/02deb07e9c325c38e1a845427a839e2f.png)](https://gyazo.com/02deb07e9c325c38e1a845427a839e2f)
        
            * 表示したいCIDまたはSIDを入力し、Viewをクリック

        [![Image from Gyazo](https://i.gyazo.com/77a62b290a196d5c35bd2d5c967922ec.png)](https://gyazo.com/77a62b290a196d5c35bd2d5c967922ec)

            * 表示されるウインドウで、化合物のコンフォマーの構造を見ることができます。また、左のツールをクリックして、画像やデータの保存することができます。

        [![Image from Gyazo](https://i.gyazo.com/8ed4e106d2a27edfd0314b24d3402d38.png)](https://gyazo.com/8ed4e106d2a27edfd0314b24d3402d38)

        ---

    ---

---




