## 1 - Introduction
Function on R is a command, that can or not receive a argument, a input, but will give us a output, which is a result of a modification on the object or the program, given that instruction for the modification caused by the function has already been programmed.

- Help Fuctions:
```R
> ?mean
"abre a página de ajuda da função"
> ??mean
"quando não sabe o nome específico da função"
> example("plot")
"gera vários exemplos de aplicações da função entre os parenteses, plot seria gráficos
```
- Fuction Média Aritmética:
```R
> mean(1:8)
[1] 4.5
> ?mean
"abre a página de ajuda da função"
> ??mean
"quando não sabe o nome específico da função"
```
- Install Packages:
```R
> install.packages('installr')
  to install the package
> library(installr)
  to run the package and use its functions
> vignette("grid")
  mostrar a documentação da fução, quando houver
```

## 2 - Types of objects
Object is data structure with certain attributes designed for a single variable. Each structure have methods that act on attributes of the object.
Basically, all that we create at R are objects.

Objects store various data structures:
- Vectors
- Functions
- Data frames
- Matrices
- Arrays
- Lists

Objects are created by assigning a value to a name, allowing you to manipulate that data:
```R
> vetor_num <- 12
  to create a vector with number
> Vetor_txt = 'Bioinformática'
  to create a vector with text
> ls()
 [1] "vetor_num" "Vetor_txt"
  to return the vectors creates  
> a <- ls()
  to designate
> rm(a)
  to remove the vector
> rm(list = ls())
  to remove all vectors
```

### Vectors
In R, a vector is any one-dimensional set containing values, which can be numbers, strings, or logical values.

Tipos:
- Vetores numéricos
- Vetores com strings
- Vetores lógicos
```R
> vetor_num <- 4
> a <- c(1,3,5,7,9)
> amostras <- c('a1','a2','a3','a4','a5')
> genes <- c('TP53', 'KR4S', 'BRAF', 'PIKSCA', 'AFC')
> prole <- c(TRUE, FALSE, FALSE, TRUE)
> tudo <- c(amostras, genes)
> tudo
 [1] "a1"     "a2"     "a3"    
 [4] "a4"     "a5"     "TP53"  
 [7] "KR4S"   "BRAF"   "PIKSCA"
[10] "AFC" 
```
