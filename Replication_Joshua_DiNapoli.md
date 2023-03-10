---
title: "Starter Notebook"
author: "You, Scientist"
format: html
execute:
  keep-md: true
---


::: {.cell}

```{.r .cell-code}
#Load in any packages you need
library(tidyverse)
```

::: {.cell-output .cell-output-stderr}
```
── Attaching packages ─────────────────────────────────────── tidyverse 1.3.2 ──
✔ ggplot2 3.4.0      ✔ purrr   1.0.0 
✔ tibble  3.1.8      ✔ dplyr   1.0.10
✔ tidyr   1.2.1      ✔ stringr 1.5.0 
✔ readr   2.1.3      ✔ forcats 0.5.2 
── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
✖ dplyr::filter() masks stats::filter()
✖ dplyr::lag()    masks stats::lag()
```
:::

```{.r .cell-code}
#Read in any data
```
:::

::: {.cell}

```{.r .cell-code}
instructors <- c("Duryea", "Gilbert")

instructors
```

::: {.cell-output .cell-output-stdout}
```
[1] "Duryea"  "Gilbert"
```
:::
:::

Challenge 1: List of nucleotides


::: {.cell}

```{.r .cell-code}
nucleotides <- c("Adenosine", "Guanine","Cytosine","Thymine")
nucleotides
```

::: {.cell-output .cell-output-stdout}
```
[1] "Adenosine" "Guanine"   "Cytosine"  "Thymine"  
```
:::
:::

Challenge 2: Random string of 15 nucleotides


::: {.cell}

```{.r .cell-code}
numNucleotide <- 15

randGenome <- sample(nucleotides, size = numNucleotide, replace = TRUE)

randGenome
```

::: {.cell-output .cell-output-stdout}
```
 [1] "Thymine"   "Cytosine"  "Thymine"   "Guanine"   "Thymine"   "Adenosine"
 [7] "Guanine"   "Adenosine" "Adenosine" "Adenosine" "Guanine"   "Guanine"  
[13] "Cytosine"  "Guanine"   "Cytosine" 
```
:::
:::

::: {.cell}

```{.r .cell-code}
numNucleotide <- 1500

randGenome <- sample(nucleotides, size = numNucleotide, replace = TRUE)

randGenome <- paste(randGenome, collapse ="")

randGenome
```

::: {.cell-output .cell-output-stdout}
```
[1] "ThymineAdenosineGuanineGuanineCytosineThymineThymineThymineThymineAdenosineThymineAdenosineThymineThymineAdenosineGuanineCytosineThymineGuanineAdenosineThymineAdenosineAdenosineAdenosineGuanineAdenosineAdenosineThymineAdenosineCytosineGuanineGuanineCytosineGuanineThymineAdenosineCytosineCytosineThymineGuanineAdenosineGuanineGuanineGuanineCytosineAdenosineAdenosineThymineAdenosineAdenosineAdenosineThymineThymineThymineThymineAdenosineAdenosineCytosineGuanineAdenosineCytosineGuanineAdenosineGuanineThymineCytosineAdenosineThymineThymineCytosineAdenosineAdenosineCytosineThymineAdenosineCytosineCytosineCytosineAdenosineThymineThymineCytosineThymineThymineGuanineGuanineAdenosineGuanineCytosineAdenosineGuanineGuanineCytosineAdenosineAdenosineThymineGuanineThymineCytosineGuanineGuanineThymineAdenosineThymineCytosineGuanineCytosineAdenosineThymineCytosineThymineAdenosineGuanineThymineCytosineGuanineGuanineThymineAdenosineAdenosineGuanineThymineThymineCytosineThymineAdenosineGuanineThymineCytosineGuanineThymineAdenosineCytosineGuanineGuanineAdenosineCytosineGuanineGuanineAdenosineThymineThymineThymineCytosineThymineCytosineThymineGuanineAdenosineAdenosineAdenosineAdenosineThymineThymineThymineThymineGuanineAdenosineAdenosineGuanineThymineCytosineCytosineThymineGuanineThymineAdenosineAdenosineGuanineGuanineCytosineThymineCytosineAdenosineThymineThymineAdenosineCytosineThymineCytosineCytosineThymineGuanineCytosineThymineThymineGuanineAdenosineGuanineAdenosineCytosineAdenosineThymineAdenosineCytosineGuanineThymineThymineCytosineGuanineAdenosineAdenosineCytosineThymineAdenosineGuanineCytosineAdenosineGuanineAdenosineThymineCytosineThymineGuanineCytosineGuanineAdenosineThymineThymineCytosineCytosineThymineCytosineAdenosineGuanineGuanineGuanineCytosineCytosineGuanineThymineGuanineThymineThymineAdenosineThymineAdenosineAdenosineAdenosineThymineCytosineAdenosineGuanineCytosineCytosineCytosineGuanineCytosineThymineCytosineCytosineCytosineThymineThymineAdenosineGuanineCytosineThymineAdenosineCytosineCytosineThymineAdenosineCytosineGuanineCytosineCytosineCytosineGuanineAdenosineThymineCytosineCytosineAdenosineCytosineGuanineCytosineCytosineAdenosineAdenosineCytosineCytosineGuanineThymineGuanineThymineThymineCytosineAdenosineCytosineGuanineGuanineThymineThymineGuanineCytosineCytosineAdenosineAdenosineAdenosineGuanineAdenosineThymineCytosineAdenosineAdenosineAdenosineCytosineAdenosineGuanineGuanineAdenosineThymineAdenosineGuanineCytosineGuanineThymineGuanineThymineThymineThymineAdenosineCytosineCytosineThymineThymineThymineCytosineGuanineAdenosineThymineAdenosineGuanineAdenosineThymineGuanineGuanineCytosineGuanineAdenosineThymineCytosineGuanineThymineCytosineThymineThymineGuanineThymineGuanineThymineGuanineCytosineCytosineCytosineGuanineAdenosineThymineGuanineCytosineCytosineAdenosineThymineCytosineGuanineThymineCytosineCytosineAdenosineCytosineCytosineAdenosineGuanineThymineGuanineAdenosineThymineThymineThymineCytosineCytosineGuanineAdenosineThymineAdenosineAdenosineAdenosineThymineThymineThymineGuanineCytosineCytosineThymineThymineThymineCytosineThymineCytosineCytosineGuanineAdenosineThymineThymineCytosineCytosineAdenosineGuanineThymineGuanineAdenosineCytosineCytosineAdenosineAdenosineCytosineThymineCytosineGuanineAdenosineGuanineAdenosineAdenosineAdenosineThymineAdenosineGuanineGuanineThymineAdenosineAdenosineAdenosineGuanineThymineAdenosineGuanineThymineAdenosineThymineCytosineCytosineThymineThymineCytosineGuanineGuanineThymineGuanineCytosineGuanineGuanineGuanineThymineAdenosineAdenosineGuanineAdenosineGuanineAdenosineCytosineAdenosineAdenosineGuanineThymineAdenosineAdenosineCytosineCytosineAdenosineAdenosineGuanineAdenosineCytosineGuanineThymineAdenosineThymineCytosineAdenosineAdenosineGuanineAdenosineCytosineGuanineThymineThymineGuanineCytosineAdenosineCytosineGuanineAdenosineCytosineGuanineThymineAdenosineGuanineThymineCytosineThymineGuanineCytosineThymineAdenosineGuanineCytosineCytosineAdenosineAdenosineThymineGuanineAdenosineCytosineThymineGuanineThymineThymineCytosineGuanineAdenosineThymineAdenosineAdenosineCytosineCytosineCytosineThymineAdenosineAdenosineAdenosineCytosineGuanineAdenosineThymineAdenosineCytosineThymineCytosineGuanineCytosineCytosineGuanineCytosineCytosineThymineGuanineGuanineCytosineGuanineGuanineCytosineCytosineAdenosineGuanineGuanineGuanineThymineThymineCytosineThymineAdenosineThymineCytosineAdenosineGuanineThymineAdenosineAdenosineCytosineGuanineGuanineGuanineGuanineCytosineAdenosineGuanineGuanineGuanineCytosineAdenosineCytosineAdenosineGuanineCytosineGuanineAdenosineGuanineThymineAdenosineGuanineCytosineGuanineGuanineGuanineGuanineAdenosineCytosineGuanineCytosineCytosineCytosineAdenosineAdenosineAdenosineAdenosineAdenosineGuanineGuanineAdenosineCytosineAdenosineThymineGuanineAdenosineThymineAdenosineCytosineGuanineThymineAdenosineThymineCytosineThymineGuanineAdenosineThymineAdenosineThymineThymineGuanineCytosineThymineAdenosineGuanineAdenosineThymineCytosineGuanineGuanineThymineAdenosineThymineCytosineGuanineCytosineGuanineCytosineGuanineAdenosineGuanineGuanineThymineCytosineAdenosineGuanineThymineGuanineGuanineGuanineCytosineCytosineThymineGuanineThymineAdenosineGuanineThymineGuanineGuanineGuanineThymineCytosineGuanineAdenosineAdenosineAdenosineThymineThymineAdenosineThymineGuanineGuanineAdenosineAdenosineAdenosineAdenosineCytosineAdenosineGuanineThymineCytosineAdenosineCytosineCytosineThymineThymineCytosineAdenosineAdenosineCytosineGuanineGuanineThymineThymineGuanineCytosineCytosineGuanineAdenosineCytosineThymineAdenosineGuanineCytosineCytosineThymineAdenosineAdenosineAdenosineGuanineGuanineAdenosineCytosineAdenosineGuanineAdenosineThymineGuanineGuanineAdenosineThymineGuanineCytosineCytosineCytosineThymineThymineCytosineAdenosineCytosineCytosineCytosineAdenosineCytosineAdenosineAdenosineCytosineGuanineGuanineGuanineCytosineCytosineThymineCytosineThymineGuanineGuanineThymineGuanineGuanineGuanineAdenosineGuanineAdenosineGuanineAdenosineThymineAdenosineAdenosineGuanineGuanineGuanineAdenosineGuanineThymineGuanineGuanineCytosineGuanineCytosineAdenosineCytosineThymineAdenosineAdenosineCytosineGuanineCytosineThymineCytosineThymineCytosineThymineGuanineCytosineCytosineThymineGuanineCytosineAdenosineCytosineCytosineGuanineCytosineGuanineAdenosineCytosineAdenosineThymineAdenosineGuanineGuanineAdenosineCytosineGuanineCytosineThymineAdenosineGuanineGuanineCytosineGuanineCytosineGuanineCytosineAdenosineGuanineCytosineThymineAdenosineAdenosineAdenosineThymineThymineCytosineThymineGuanineCytosineThymineThymineGuanineCytosineGuanineCytosineAdenosineAdenosineCytosineCytosineThymineAdenosineThymineCytosineThymineGuanineAdenosineGuanineGuanineThymineAdenosineGuanineAdenosineAdenosineAdenosineCytosineCytosineGuanineAdenosineAdenosineGuanineCytosineGuanineAdenosineThymineThymineThymineGuanineGuanineCytosineThymineAdenosineGuanineCytosineThymineGuanineCytosineAdenosineGuanineAdenosineThymineGuanineAdenosineGuanineCytosineCytosineGuanineThymineThymineAdenosineAdenosineAdenosineAdenosineGuanineCytosineCytosineAdenosineAdenosineGuanineAdenosineGuanineCytosineThymineCytosineCytosineAdenosineThymineGuanineAdenosineGuanineGuanineAdenosineCytosineAdenosineGuanineAdenosineThymineAdenosineCytosineThymineCytosineCytosineAdenosineAdenosineThymineThymineThymineCytosineThymineGuanineGuanineCytosineAdenosineThymineThymineGuanineGuanineCytosineThymineAdenosineCytosineAdenosineGuanineCytosineAdenosineThymineAdenosineAdenosineThymineGuanineCytosineThymineCytosineGuanineGuanineAdenosineAdenosineCytosineAdenosineGuanineCytosineGuanineAdenosineAdenosineCytosineThymineThymineGuanineGuanineThymineGuanineCytosineCytosineAdenosineCytosineGuanineThymineThymineThymineCytosineGuanineThymineAdenosineThymineCytosineGuanineCytosineCytosineCytosineCytosineThymineCytosineThymineCytosineCytosineCytosineAdenosineCytosineThymineCytosineCytosineThymineAdenosineGuanineCytosineGuanineCytosineGuanineCytosineGuanineCytosineGuanineAdenosineCytosineCytosineThymineAdenosineAdenosineThymineAdenosineThymineAdenosineCytosineAdenosineCytosineAdenosineCytosineAdenosineThymineCytosineAdenosineGuanineCytosineAdenosineCytosineCytosineAdenosineAdenosineCytosineAdenosineThymineAdenosineCytosineGuanineGuanineCytosineCytosineGuanineCytosineAdenosineThymineCytosineAdenosineCytosineGuanineAdenosineCytosineAdenosineThymineCytosineAdenosineGuanineGuanineGuanineAdenosineThymineThymineGuanineGuanineThymineGuanineGuanineCytosineGuanineThymineAdenosineGuanineGuanineAdenosineAdenosineCytosineGuanineThymineThymineGuanineGuanineGuanineCytosineAdenosineGuanineAdenosineCytosineAdenosineCytosineCytosineCytosineThymineGuanineThymineAdenosineAdenosineThymineCytosineAdenosineCytosineAdenosineGuanineAdenosineThymineAdenosineCytosineAdenosineThymineAdenosineThymineThymineThymineCytosineThymineCytosineGuanineAdenosineCytosineThymineAdenosineThymineAdenosineCytosineGuanineCytosineGuanineThymineThymineCytosineGuanineGuanineGuanineAdenosineCytosineThymineThymineThymineGuanineCytosineThymineAdenosineGuanineCytosineGuanineCytosineThymineCytosineThymineAdenosineGuanineAdenosineCytosineGuanineAdenosineGuanineAdenosineGuanineThymineAdenosineCytosineAdenosineGuanineThymineAdenosineGuanineCytosineAdenosineAdenosineAdenosineAdenosineGuanineGuanineCytosineThymineAdenosineThymineThymineGuanineCytosineCytosineGuanineAdenosineThymineThymineAdenosineGuanineAdenosineThymineThymineAdenosineThymineAdenosineThymineAdenosineCytosineThymineThymineAdenosineGuanineThymineCytosineCytosineAdenosineGuanineCytosineAdenosineAdenosineGuanineGuanineGuanineCytosineThymineAdenosineAdenosineGuanineCytosineAdenosineCytosineCytosineThymineAdenosineCytosineGuanineAdenosineGuanineAdenosineGuanineGuanineCytosineAdenosineGuanineThymineGuanineCytosineAdenosineThymineCytosineThymineThymineGuanineCytosineAdenosineGuanineGuanineThymineGuanineAdenosineAdenosineThymineGuanineThymineGuanineCytosineCytosineGuanineCytosineGuanineCytosineCytosineGuanineGuanineThymineCytosineGuanineAdenosineThymineGuanineCytosineThymineAdenosineAdenosineCytosineAdenosineCytosineThymineThymineCytosineCytosineCytosineCytosineGuanineAdenosineThymineAdenosineThymineCytosineCytosineAdenosineGuanineThymineAdenosineThymineThymineCytosineThymineCytosineAdenosineThymineGuanineThymineGuanineCytosineAdenosineCytosineCytosineAdenosineAdenosineCytosineAdenosineGuanineAdenosineGuanineGuanineGuanineCytosineGuanineGuanineThymineThymineGuanineCytosineThymineThymineGuanineThymineThymineGuanineThymineThymineCytosineCytosineThymineGuanineGuanineGuanineAdenosineAdenosineCytosineThymineThymineGuanineGuanineGuanineCytosineGuanineCytosineGuanineThymineCytosineCytosineAdenosineThymineGuanineGuanineGuanineThymineAdenosineCytosineGuanineCytosineThymineAdenosineThymineThymineCytosineThymineThymineCytosineGuanineThymineAdenosineThymineCytosineCytosineThymineGuanineGuanineAdenosineThymineGuanineCytosineAdenosineThymineThymineGuanineCytosineGuanineAdenosineAdenosineAdenosineGuanineGuanineThymineCytosineAdenosineThymineGuanineCytosineThymineGuanineAdenosineAdenosineGuanineAdenosineAdenosineThymineCytosineThymineThymineCytosineCytosineThymineGuanineGuanineAdenosineThymineThymineThymineGuanineGuanineThymineGuanineCytosineCytosineAdenosineAdenosineThymineAdenosineGuanineThymineThymineThymineThymineGuanineCytosineAdenosineGuanineAdenosineCytosineThymineCytosineCytosineThymineThymineThymineCytosineAdenosineGuanineThymineGuanineAdenosineThymineAdenosineAdenosineThymineCytosineGuanineCytosineCytosineThymineCytosineCytosineCytosineThymineAdenosineCytosineCytosineThymineAdenosineCytosineAdenosineGuanineCytosineAdenosineThymineGuanineThymineCytosineGuanineGuanineGuanineGuanineAdenosineAdenosineCytosineAdenosine"
```
:::
:::

Challenge 4: Generate a random genome of 100 nucleotides and count adenosine


::: {.cell}

```{.r .cell-code}
set.seed(215)
numNucleotide <- 100

randGenome <- sample(nucleotides, size = numNucleotide, replace = TRUE)

randGenome <- paste(randGenome, collapse ="")

randGenome
```

::: {.cell-output .cell-output-stdout}
```
[1] "ThymineCytosineCytosineAdenosineAdenosineThymineGuanineThymineThymineThymineAdenosineAdenosineThymineCytosineThymineThymineGuanineGuanineCytosineAdenosineGuanineGuanineThymineThymineThymineCytosineAdenosineCytosineGuanineGuanineThymineGuanineAdenosineAdenosineCytosineThymineThymineCytosineCytosineAdenosineGuanineThymineAdenosineGuanineGuanineCytosineGuanineCytosineCytosineGuanineGuanineGuanineGuanineGuanineCytosineAdenosineGuanineGuanineCytosineAdenosineCytosineAdenosineCytosineGuanineThymineAdenosineAdenosineGuanineThymineGuanineThymineAdenosineAdenosineAdenosineThymineCytosineAdenosineThymineCytosineGuanineAdenosineAdenosineCytosineGuanineAdenosineCytosineGuanineCytosineGuanineCytosineThymineCytosineGuanineGuanineCytosineAdenosineCytosineThymineGuanineThymine"
```
:::
:::

::: {.cell}

```{.r .cell-code}
myProduct <- 1

for(j in 1:15){
  myProduct <- myProduct + j
  print(myProduct)
}
```

::: {.cell-output .cell-output-stdout}
```
[1] 2
[1] 4
[1] 7
[1] 11
[1] 16
[1] 22
[1] 29
[1] 37
[1] 46
[1] 56
[1] 67
[1] 79
[1] 92
[1] 106
[1] 121
```
:::
:::
