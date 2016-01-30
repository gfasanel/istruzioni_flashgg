# istruzioni_flashgg

* Dataset su DAS (da miniAOD) -> flashgg (Seth Zenz che ha i producer e dai miniAOD si crea i microAOD i quali appaiono su DAS anche loro). In metadata/data c'e' il catologo dei file su cui si e' girato

* Dopo aver prodotto i microAOD si girano i taggers (VH, tth ecc, i quali hanno una certa priorita') 

* Dopo i taggers vengono creati i workspace, da cui i limiti

Questo per flashgg (che quindi non passa mai attraverso le ntuple, fa tutto attraverso mini-micro AOD)

**diphotons invece ha anche i Producer (Dumper/Analyzer) che gira sui microAOD e crea le nutple, su cui poi fai i plottini

La chiamata e' la seguente:
```cmsRun xxDumper.py```

xxDumper.py contiene una chiamata a un certo Analyzer/Dumper che sta in plugin

Se devi girare con crab: ``` crab config.py che chiama bla.py```
