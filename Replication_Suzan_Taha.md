---
title: "Starter Notebook"
author: "Suzan Taha"
format: html
execute:
  keep-md: true
---




### Challenge 1
In this block of code we are developing our four nucleotides, Adenine, Guanine, Cytosine, and Thymine and then proceeding to print them out into our notebook.

::: {.cell}

```{.r .cell-code}
nucleotides <- c("A","G","C", "T")
nucleotides
```

::: {.cell-output .cell-output-stdout}
```
[1] "A" "G" "C" "T"
```
:::
:::

### Challenge 2
In this challenge we are giving our string a set number, in this case 15 so that our outcome is a random list of our nucleotides that is of length 15.

::: {.cell}

```{.r .cell-code}
randString <- 15

randGenome <- sample(nucleotides, size = randString, replace = TRUE)

randGenome
```

::: {.cell-output .cell-output-stdout}
```
 [1] "A" "T" "T" "G" "T" "C" "A" "C" "A" "G" "A" "T" "A" "G" "G"
```
:::
:::

### Challenge 3
We are about to create another random string of length 1500. This string however is going to be collapsed into one large line of nucleotides rather than having quotation marks between each character. 

::: {.cell}

```{.r .cell-code}
randString2 <- 1500
randGenome2 <- sample(nucleotides, size =randString2, replace = TRUE)
randGenome2
```

::: {.cell-output .cell-output-stdout}
```
   [1] "T" "A" "C" "T" "T" "A" "G" "A" "A" "C" "G" "T" "G" "G" "T" "T" "A" "T"
  [19] "T" "A" "T" "T" "G" "C" "G" "C" "A" "A" "A" "T" "A" "G" "A" "C" "A" "G"
  [37] "T" "C" "C" "G" "T" "T" "A" "T" "G" "T" "A" "A" "G" "C" "T" "C" "C" "G"
  [55] "T" "G" "T" "A" "A" "A" "T" "A" "A" "T" "A" "A" "G" "C" "C" "G" "T" "C"
  [73] "G" "C" "G" "C" "G" "G" "T" "C" "C" "A" "C" "G" "T" "C" "A" "T" "T" "A"
  [91] "C" "A" "G" "G" "C" "G" "T" "G" "A" "T" "G" "T" "C" "G" "T" "A" "G" "G"
 [109] "T" "T" "G" "G" "A" "T" "G" "C" "T" "C" "G" "G" "T" "T" "C" "C" "G" "C"
 [127] "C" "G" "C" "C" "T" "A" "G" "G" "G" "C" "G" "A" "A" "T" "T" "C" "T" "G"
 [145] "T" "G" "G" "C" "A" "C" "G" "T" "C" "T" "C" "A" "C" "T" "A" "A" "C" "T"
 [163] "C" "A" "T" "C" "A" "G" "A" "T" "T" "T" "A" "G" "G" "G" "T" "C" "G" "C"
 [181] "G" "T" "A" "C" "C" "G" "C" "A" "T" "G" "T" "G" "G" "C" "G" "A" "T" "C"
 [199] "T" "G" "G" "C" "T" "A" "A" "G" "G" "G" "C" "C" "T" "T" "G" "A" "T" "C"
 [217] "T" "A" "A" "T" "C" "T" "A" "T" "C" "G" "C" "T" "A" "G" "T" "T" "G" "G"
 [235] "T" "A" "C" "G" "C" "A" "C" "G" "A" "C" "C" "T" "A" "T" "A" "A" "T" "A"
 [253] "A" "T" "C" "A" "G" "C" "A" "G" "C" "A" "A" "A" "C" "C" "A" "C" "T" "T"
 [271] "T" "G" "T" "G" "T" "C" "A" "T" "G" "T" "A" "G" "T" "C" "G" "T" "G" "T"
 [289] "A" "C" "G" "C" "C" "T" "C" "A" "A" "C" "C" "C" "C" "G" "C" "A" "T" "G"
 [307] "A" "A" "C" "G" "C" "G" "C" "T" "C" "C" "G" "G" "T" "C" "C" "G" "G" "T"
 [325] "T" "G" "G" "T" "G" "T" "C" "G" "A" "G" "T" "A" "G" "G" "G" "G" "C" "T"
 [343] "G" "A" "T" "T" "T" "G" "G" "T" "A" "A" "A" "A" "T" "G" "T" "T" "A" "C"
 [361] "A" "C" "T" "A" "C" "C" "C" "A" "T" "G" "T" "A" "C" "T" "A" "G" "T" "A"
 [379] "C" "C" "T" "C" "G" "T" "A" "C" "G" "A" "C" "G" "T" "A" "G" "C" "A" "A"
 [397] "G" "A" "C" "A" "C" "C" "A" "T" "C" "G" "G" "G" "G" "G" "G" "T" "G" "A"
 [415] "A" "T" "A" "A" "A" "G" "C" "T" "A" "C" "T" "T" "G" "G" "A" "A" "G" "T"
 [433] "A" "G" "C" "T" "T" "G" "C" "T" "G" "T" "C" "C" "T" "A" "G" "G" "T" "C"
 [451] "G" "A" "T" "A" "C" "A" "G" "A" "G" "A" "T" "T" "G" "T" "C" "G" "T" "T"
 [469] "T" "A" "A" "A" "A" "T" "A" "T" "C" "A" "C" "A" "G" "T" "T" "T" "T" "A"
 [487] "T" "A" "C" "C" "A" "G" "T" "G" "C" "G" "C" "A" "A" "C" "A" "T" "A" "C"
 [505] "C" "T" "G" "C" "T" "T" "C" "T" "T" "T" "A" "A" "C" "A" "A" "A" "T" "A"
 [523] "A" "T" "T" "C" "A" "C" "T" "C" "A" "G" "T" "C" "T" "A" "A" "A" "T" "A"
 [541] "T" "G" "G" "A" "C" "A" "G" "G" "A" "C" "A" "G" "A" "T" "G" "T" "G" "G"
 [559] "C" "G" "G" "C" "C" "A" "T" "T" "A" "A" "G" "C" "A" "C" "G" "G" "A" "T"
 [577] "G" "G" "G" "T" "T" "T" "T" "T" "T" "T" "G" "G" "A" "C" "T" "T" "G" "C"
 [595] "A" "A" "G" "T" "G" "T" "C" "C" "A" "G" "A" "C" "T" "G" "T" "T" "T" "T"
 [613] "G" "G" "C" "A" "G" "T" "C" "G" "A" "C" "G" "A" "G" "A" "A" "G" "G" "C"
 [631] "A" "T" "T" "T" "C" "G" "A" "A" "C" "T" "C" "T" "A" "T" "C" "A" "G" "G"
 [649] "A" "C" "C" "C" "A" "T" "T" "A" "A" "C" "T" "C" "G" "A" "T" "T" "C" "C"
 [667] "T" "C" "G" "A" "G" "C" "A" "T" "G" "A" "C" "C" "A" "G" "T" "G" "C" "C"
 [685] "T" "A" "G" "T" "C" "C" "G" "C" "G" "G" "T" "T" "T" "C" "T" "C" "A" "A"
 [703] "G" "C" "G" "A" "A" "A" "A" "T" "T" "G" "T" "T" "A" "C" "A" "A" "G" "A"
 [721] "A" "G" "T" "G" "T" "G" "G" "G" "A" "T" "C" "G" "C" "T" "G" "T" "A" "C"
 [739] "G" "G" "T" "T" "A" "G" "T" "A" "C" "T" "G" "T" "A" "C" "A" "A" "C" "A"
 [757] "G" "G" "A" "T" "C" "T" "T" "A" "G" "C" "C" "C" "G" "C" "C" "C" "T" "T"
 [775] "C" "A" "T" "G" "A" "C" "A" "T" "T" "T" "C" "G" "T" "A" "A" "G" "G" "G"
 [793] "C" "T" "A" "A" "G" "T" "C" "G" "C" "C" "G" "G" "C" "A" "A" "G" "T" "G"
 [811] "C" "G" "G" "G" "T" "T" "G" "G" "A" "G" "T" "T" "A" "C" "T" "C" "A" "T"
 [829] "T" "G" "A" "T" "T" "T" "C" "T" "C" "C" "C" "A" "G" "C" "A" "A" "A" "G"
 [847] "T" "C" "G" "C" "A" "C" "G" "A" "T" "C" "G" "G" "G" "G" "G" "G" "T" "G"
 [865] "C" "A" "G" "G" "C" "T" "G" "G" "G" "G" "C" "C" "A" "T" "C" "G" "A" "G"
 [883] "C" "G" "C" "C" "T" "G" "G" "T" "C" "G" "C" "C" "C" "A" "T" "G" "G" "G"
 [901] "T" "A" "A" "C" "C" "G" "G" "A" "G" "C" "A" "G" "C" "T" "C" "C" "G" "T"
 [919] "G" "G" "T" "G" "C" "C" "G" "G" "C" "G" "T" "C" "A" "A" "G" "T" "A" "G"
 [937] "T" "A" "G" "C" "A" "C" "G" "A" "A" "T" "A" "T" "C" "T" "G" "G" "C" "A"
 [955] "T" "G" "T" "G" "G" "C" "C" "G" "A" "T" "A" "A" "C" "A" "A" "T" "C" "G"
 [973] "T" "A" "C" "T" "T" "T" "G" "A" "G" "C" "G" "T" "C" "A" "T" "G" "G" "T"
 [991] "C" "T" "C" "A" "C" "C" "C" "C" "G" "A" "G" "C" "T" "G" "G" "C" "A" "T"
[1009] "C" "A" "T" "T" "C" "C" "G" "G" "T" "A" "C" "T" "C" "C" "C" "G" "C" "C"
[1027] "T" "T" "G" "A" "T" "T" "T" "A" "C" "G" "C" "T" "C" "G" "G" "A" "A" "C"
[1045] "A" "G" "T" "T" "C" "A" "A" "A" "C" "G" "C" "T" "A" "G" "C" "C" "C" "A"
[1063] "A" "G" "G" "G" "T" "T" "T" "G" "T" "C" "A" "T" "G" "G" "T" "A" "A" "C"
[1081] "A" "T" "A" "A" "G" "C" "G" "A" "T" "A" "C" "G" "A" "C" "C" "A" "T" "C"
[1099] "T" "T" "T" "T" "T" "A" "T" "C" "C" "T" "A" "C" "T" "G" "G" "C" "T" "G"
[1117] "G" "C" "T" "A" "G" "C" "T" "C" "G" "T" "C" "C" "C" "T" "A" "T" "C" "G"
[1135] "A" "G" "G" "T" "T" "T" "G" "G" "C" "A" "T" "T" "T" "T" "A" "C" "A" "G"
[1153] "T" "A" "G" "A" "A" "T" "T" "G" "T" "T" "G" "C" "T" "A" "T" "G" "G" "C"
[1171] "G" "A" "A" "G" "T" "T" "A" "G" "A" "A" "T" "C" "A" "G" "T" "C" "A" "A"
[1189] "A" "T" "G" "G" "A" "A" "T" "T" "T" "A" "G" "C" "T" "G" "G" "G" "A" "T"
[1207] "G" "C" "G" "T" "A" "T" "C" "T" "G" "T" "T" "A" "C" "T" "C" "C" "T" "A"
[1225] "G" "T" "T" "G" "G" "T" "T" "T" "C" "A" "G" "G" "G" "T" "G" "C" "C" "G"
[1243] "G" "T" "T" "A" "T" "C" "C" "T" "A" "G" "C" "T" "T" "G" "A" "C" "A" "C"
[1261] "A" "G" "G" "C" "G" "C" "T" "A" "G" "C" "C" "G" "A" "G" "A" "A" "T" "C"
[1279] "G" "G" "G" "T" "A" "C" "T" "G" "T" "G" "T" "A" "T" "G" "C" "A" "G" "C"
[1297] "C" "G" "A" "C" "G" "A" "C" "T" "T" "A" "T" "T" "C" "T" "C" "A" "A" "C"
[1315] "C" "G" "G" "T" "A" "A" "T" "G" "C" "A" "T" "G" "T" "C" "G" "G" "T" "T"
[1333] "G" "T" "C" "A" "C" "T" "A" "G" "A" "C" "G" "T" "T" "A" "G" "C" "A" "T"
[1351] "C" "G" "G" "C" "C" "T" "C" "T" "G" "A" "G" "T" "A" "G" "C" "C" "T" "G"
[1369] "G" "C" "A" "T" "A" "A" "A" "G" "G" "C" "A" "G" "G" "C" "C" "A" "A" "A"
[1387] "A" "T" "A" "A" "T" "C" "C" "C" "T" "T" "G" "C" "T" "T" "G" "A" "C" "G"
[1405] "T" "T" "C" "A" "T" "G" "G" "A" "C" "T" "G" "C" "T" "T" "A" "C" "C" "C"
[1423] "G" "T" "A" "A" "C" "C" "G" "T" "T" "C" "T" "T" "C" "G" "T" "C" "A" "C"
[1441] "T" "A" "C" "T" "C" "A" "C" "A" "G" "C" "G" "G" "C" "C" "A" "G" "G" "C"
[1459] "G" "A" "C" "G" "C" "T" "A" "T" "G" "G" "A" "A" "A" "A" "G" "G" "A" "G"
[1477] "G" "A" "A" "A" "A" "G" "T" "T" "A" "C" "T" "G" "T" "T" "T" "T" "T" "G"
[1495] "A" "G" "G" "C" "C" "G"
```
:::

```{.r .cell-code}
paste(randGenome2, collapse = "")
```

::: {.cell-output .cell-output-stdout}
```
[1] "TACTTAGAACGTGGTTATTATTGCGCAAATAGACAGTCCGTTATGTAAGCTCCGTGTAAATAATAAGCCGTCGCGCGGTCCACGTCATTACAGGCGTGATGTCGTAGGTTGGATGCTCGGTTCCGCCGCCTAGGGCGAATTCTGTGGCACGTCTCACTAACTCATCAGATTTAGGGTCGCGTACCGCATGTGGCGATCTGGCTAAGGGCCTTGATCTAATCTATCGCTAGTTGGTACGCACGACCTATAATAATCAGCAGCAAACCACTTTGTGTCATGTAGTCGTGTACGCCTCAACCCCGCATGAACGCGCTCCGGTCCGGTTGGTGTCGAGTAGGGGCTGATTTGGTAAAATGTTACACTACCCATGTACTAGTACCTCGTACGACGTAGCAAGACACCATCGGGGGGTGAATAAAGCTACTTGGAAGTAGCTTGCTGTCCTAGGTCGATACAGAGATTGTCGTTTAAAATATCACAGTTTTATACCAGTGCGCAACATACCTGCTTCTTTAACAAATAATTCACTCAGTCTAAATATGGACAGGACAGATGTGGCGGCCATTAAGCACGGATGGGTTTTTTTGGACTTGCAAGTGTCCAGACTGTTTTGGCAGTCGACGAGAAGGCATTTCGAACTCTATCAGGACCCATTAACTCGATTCCTCGAGCATGACCAGTGCCTAGTCCGCGGTTTCTCAAGCGAAAATTGTTACAAGAAGTGTGGGATCGCTGTACGGTTAGTACTGTACAACAGGATCTTAGCCCGCCCTTCATGACATTTCGTAAGGGCTAAGTCGCCGGCAAGTGCGGGTTGGAGTTACTCATTGATTTCTCCCAGCAAAGTCGCACGATCGGGGGGTGCAGGCTGGGGCCATCGAGCGCCTGGTCGCCCATGGGTAACCGGAGCAGCTCCGTGGTGCCGGCGTCAAGTAGTAGCACGAATATCTGGCATGTGGCCGATAACAATCGTACTTTGAGCGTCATGGTCTCACCCCGAGCTGGCATCATTCCGGTACTCCCGCCTTGATTTACGCTCGGAACAGTTCAAACGCTAGCCCAAGGGTTTGTCATGGTAACATAAGCGATACGACCATCTTTTTATCCTACTGGCTGGCTAGCTCGTCCCTATCGAGGTTTGGCATTTTACAGTAGAATTGTTGCTATGGCGAAGTTAGAATCAGTCAAATGGAATTTAGCTGGGATGCGTATCTGTTACTCCTAGTTGGTTTCAGGGTGCCGGTTATCCTAGCTTGACACAGGCGCTAGCCGAGAATCGGGTACTGTGTATGCAGCCGACGACTTATTCTCAACCGGTAATGCATGTCGGTTGTCACTAGACGTTAGCATCGGCCTCTGAGTAGCCTGGCATAAAGGCAGGCCAAAATAATCCCTTGCTTGACGTTCATGGACTGCTTACCCGTAACCGTTCTTCGTCACTACTCACAGCGGCCAGGCGACGCTATGGAAAAGGAGGAAAAGTTACTGTTTTTGAGGCCG"
```
:::
:::

### Challenge 4
In challenge 4 we are setting a seed of 215 to allow my group members and I to obtain the same 100 values within our nucleotides. 

::: {.cell}

```{.r .cell-code}
set.seed(215)

randString3 <- 100
randGenome3 <- sample(nucleotides, size = randString3, replace = TRUE)
randGenome3
```

::: {.cell-output .cell-output-stdout}
```
  [1] "T" "C" "C" "A" "A" "T" "G" "T" "T" "T" "A" "A" "T" "C" "T" "T" "G" "G"
 [19] "C" "A" "G" "G" "T" "T" "T" "C" "A" "C" "G" "G" "T" "G" "A" "A" "C" "T"
 [37] "T" "C" "C" "A" "G" "T" "A" "G" "G" "C" "G" "C" "C" "G" "G" "G" "G" "G"
 [55] "C" "A" "G" "G" "C" "A" "C" "A" "C" "G" "T" "A" "A" "G" "T" "G" "T" "A"
 [73] "A" "A" "T" "C" "A" "T" "C" "G" "A" "A" "C" "G" "A" "C" "G" "C" "G" "C"
 [91] "T" "C" "G" "G" "C" "A" "C" "T" "G" "T"
```
:::

```{.r .cell-code}
randGenome3 <- paste(randGenome3, collapse = "")
```
:::

### Challenge 5
In the code block below, we are learning how to use a for loop of 1 which will allow us to portray all 'j' values from 1 to 15. This is useful when we want to use the same chunck of code over and over again.

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

### Challenge 6
We are about to use a randome genome of length 10 and execute a for loop to determine each individual nucleotide that is present.

::: {.cell}

```{.r .cell-code}
genomeLength <- 10

randGenome <- sample(nucleotides, size = genomeLength, replace = TRUE)

randGenome <- paste(randGenome, collapse = "")
randGenome
```

::: {.cell-output .cell-output-stdout}
```
[1] "GTCTCCAGAC"
```
:::

```{.r .cell-code}
for(i in 1:10){
print(str_sub(randGenome, start=i, end= i))
}
```

::: {.cell-output .cell-output-stdout}
```
[1] "G"
[1] "T"
[1] "C"
[1] "T"
[1] "C"
[1] "C"
[1] "A"
[1] "G"
[1] "A"
[1] "C"
```
:::
:::

### Challenge 7
We are about to use the same random genome as previously, however we are going to use a for loop and 'nchar' to give us the amount of Adenine's we have in our nucleotide as a number.

::: {.cell}

```{.r .cell-code}
randGenome
```

::: {.cell-output .cell-output-stdout}
```
[1] "GTCTCCAGAC"
```
:::

```{.r .cell-code}
adeninecount <- 0
for(i in 1:nchar(randGenome)){
  if(str_sub(randGenome, start = i, end = i) == "A"){
    adeninecount <- adeninecount + 1
  }
}
print(adeninecount)
```

::: {.cell-output .cell-output-stdout}
```
[1] 2
```
:::
:::

### Challenge 8
In challenge 8, we are going to us our same randome genome of length 10 to view how much of each base we have in our ten letter long nucleotide. 

::: {.cell}

```{.r .cell-code}
#Use this code chunk to complete Challenge 8
randGenome
```

::: {.cell-output .cell-output-stdout}
```
[1] "GTCTCCAGAC"
```
:::

```{.r .cell-code}
adenine_count <- 0
cytosine_count <- 0
guanine_count <- 0
thymine_count <- 0
for(i in 1:nchar(randGenome)){
  if(str_sub(randGenome, start = i, end = i) == "A"){
    adenine_count <- adenine_count + 1
  }
  if(str_sub(randGenome, start = i, end = i) == "C"){
    cytosine_count <- cytosine_count + 1
  }
  if(str_sub(randGenome, start = i, end = i) == "G"){
    guanine_count <- guanine_count + 1
  }
  if(str_sub(randGenome, start = i, end = i) == "T"){
    thymine_count <- thymine_count + 1
  }
}
print(c(adenine_count,thymine_count,guanine_count, cytosine_count))
```

::: {.cell-output .cell-output-stdout}
```
[1] 2 2 2 4
```
:::
:::

### Challenge 9
We are about to read in a file that contains an extensive amount of nucleotides so that we can work with a bigger environment. 

::: {.cell}

```{.r .cell-code}
#Use this code chunk to complete Challenge 9
```
:::