---
# Title, summary, and page position.
linktitle: "Generalisierte Lineare Modelle"
weight: 6
date: "2021-01-25"

# Page metadata.
title: "Generalisierte Lineare Modelle"
type: book  # Do not modify.
---

<style>
code{
  color: #2a7792;
}
.hljs{
  font-size: 16px
}
.minih{
  font-size: 1px;
  margin: 0px 0px 0px 0px;
}

.highlight {
    position: relative;
}
.highlight pre {
    padding: 15px;
}
.highlight-copy-btn {
    position: absolute;
    top: 7px;
    right: 7px;
    border: 0;
    border-radius: 4px;
    padding: 5px;
    font-size: 0.7em;
    line-height: 1.8;
    color: #fff;
    background-color: #777;
    min-width: 55px;
    text-align: center;
}
.highlight-copy-btn:hover {
    background-color: #666;
}
</style>

---



## Foliensatz {.minih}


<iframe src="https://drive.google.com/file/d/1SdHf64DL6odKCzWrFLhrxoGMBvEeH8X_/preview" width="736" height="552" allow="autoplay"></iframe>


<br></br>

## Praxis-Teil

---


### Logistische Regression

{{< highlight R >}}
# Wir fokussieren hier auf die logistische Regression.
# Wir nutzen die neu generierte Reliable Improvement-Variable als Repsonse

# In einem Set:
m.logreg <- glm(ri ~ 1 + group + pss.0, data = implist[[1]],
                family = binomial("logit"))
summary(m.logreg)


# In den MI-Sets:
with(implist, glm(ri ~ 1 + group + pss.0,binomial("logit"))) %>%
  testEstimates() -> mi.logreg
mi.logreg
{{< / highlight >}}


<style>
h1 {color: #2a7792;}
</style>
