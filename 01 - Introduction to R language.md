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
Operações:
```R
> prostrata <- c(65,58,5,63,78,67)
> max(prostrata)
[1] 78
> min(prostrata)
[1] 5
> range(prostrata)
[1]  5 78
> sum(prostrata)
[1] 336
> length(prostrata)
[1] 6
> mean(prostrata)
[1] 56
> median(prostrata)
[1] 64
> quantile(prostrata)
   0%   25%   50%   75%  100% 
 5.00 59.25 64.00 66.50 78.00 
> summary(prostrata)
   Min. 1st Qu.  Median    Mean 
   5.00   59.25   64.00   56.00 
3rd Qu.    Max. 
  66.50   78.00
````
Indexação:
```R
> prostrata[4]
[1] 63
> a <- prostrata[2]
> prostrata[c(2,3,4)]
[1] 58  5 63
> prostrata[-1]
[1] 58  5 63 78 67
> prostrata[3] <- 66
> prostrata
[1] 65 58 66 63 78 67
```

```R
> a <- c(1:10) #concatenar de 1 a 10
> sequencia <- seq(2,10,2) #uma sequencia de 2 a 10 de 2 em 2 numeros
> sequencia
[1]  2  4  6  8 10
> sequencia2 <- seq(1,15,3) #uma sequencia de 1 a 15 de 3 em 3 numeros
> sequencia2
[1]  1  4  7 10 13
> alfabeto <- letters #letters é um objeto já existente no r
> alfabeto
 [1] "a" "b" "c" "d" "e" "f" "g" "h"
 [9] "i" "j" "k" "l" "m" "n" "o" "p"
[17] "q" "r" "s" "t" "u" "v" "w" "x"
[25] "y" "z"
> alfabeto2 <- letters[1:10]
> alfabeto2
 [1] "a" "b" "c" "d" "e" "f" "g" "h"
 [9] "i" "j"
> ALFABETO <- LETTERS
> ALFABETO
 [1] "A" "B" "C" "D" "E" "F" "G" "H"
 [9] "I" "J" "K" "L" "M" "N" "O" "P"
[17] "Q" "R" "S" "T" "U" "V" "W" "X"
[25] "Y" "Z"
#função repetir
> rep(2,3)
[1] 2 2 2
> rep(prostrata, 2)
 [1] 65 58 66 63 78 67 65 58 66 63 78
[12] 67
```
Histograma e números
```R
> f <- runif(15,10,20)
> f
 [1] 16.47934 17.18744 18.12144
 [4] 18.54327 18.64611 16.93331
 [7] 17.16226 14.09170 10.22172
[10] 14.06639 12.14709 14.64435
[13] 14.93615 13.12749 16.72229
> f <- runif(15,10,20) # 15 numeros entre 10 a 20
> f
 [1] 12.67570 19.44124 12.78294
 [4] 18.07440 14.59955 14.75742
 [7] 11.18068 16.35172 15.76248
[10] 17.11991 17.72799 19.27849
[13] 12.18865 13.59688 16.33185
> g <- rnorm(15,5,6) #gera 15 números em uma distribuição normal
> g
 [1]  1.7277978  2.0079071 11.0777144
 [4]  1.9686593 -4.1624474 14.9029308
 [7] 10.7092010 18.0613417 -2.1321460
[10] 11.9069126  9.6354775 -0.1692335
[13] -1.0689065 10.0346702  3.6044233
> hist(f)
> hist(g)
```
Histograma do f
<img width="619" height="350" alt="image" src="https://github.com/user-attachments/assets/ccacd42f-6e8d-4a47-b646-d6f88bc07537" />
Histograma do g
<img width="619" height="350" alt="image" src="https://github.com/user-attachments/assets/ccf34a12-bea1-466e-b7eb-072b75a1124b" />
Agora maior:
```R
> g <- rnorm(50,5,6)
> g
 [1]  1.1152642  0.2326210  5.8136275
 [4]  2.9353641 -2.4131234  3.4102716
 [7]  8.2406613 10.1335383 -1.9777418
[10] -5.1324662 11.0754231  5.8367826
[13]  6.0776201  0.8431811 -1.2150455
[16] 11.7760919  3.0737193 12.9881690
[19] -3.2388469 -2.9724877 13.6953668
[22] 10.2531276 10.0879070  3.5137253
[25] -4.2202215 11.5657424 11.3388420
[28] -0.6585252  4.9907630  3.3804384
[31] 18.5544843  2.2721888  9.6969512
[34]  5.7728794  4.9919770 -1.9717776
[37] 18.2377849  7.6591944  0.3050835
[40] 10.5771955 -5.6126034 -4.9376436
[43] -1.8215743 -5.7166548 -0.7126365
[46]  7.8478000  4.1143193  4.6290295
[49] -3.0236476 -2.4180878
> hist(g)
```
Histograma do g de 50 unid:
<img width="304" height="344" alt="image" src="https://github.com/user-attachments/assets/45edf21a-d452-4bd2-bbde-d137cd985ccb" />
Histograma de 200 unid, nos mesmos parâmetros:
<img width="304" height="344" alt="image" src="https://github.com/user-attachments/assets/a25c82dd-fdab-410c-ae72-d067093edbe2" />

### Matrizes:
São objetos que possuem elementos com coordenadas(linhas e colunas)
```R
> mat <- matrix(c(1:9), ncol = 3)
> mat
     [,1] [,2] [,3]
[1,]    1    4    7
[2,]    2    5    8
[3,]    3    6    9
> x <- 1:8
> mat2 <- matrix(x, ncol = 2)
> mat2
     [,1] [,2]
[1,]    1    5
[2,]    2    6
[3,]    3    7
[4,]    4    8
> a <- 1:5
> b <- seq(12,20,2)
> mat3 <- cbind(a,b) #organiza em colunas
> mat3
     a  b
[1,] 1 12
[2,] 2 14
[3,] 3 16
[4,] 4 18
[5,] 5 20
> mat4 <- rbind(a,b)
> mat4
  [,1] [,2] [,3] [,4] [,5]
a    1    2    3    4    5
b   12   14   16   18   20
> mat3[3,2]
 b 
16
#matriz[LINHAS, COLUNAS]
> mat3[,1] #todas as linhas e só a primeira coluna(ele retorna na horizontal)
[1] 1 2 3 4 5
> mat3[1,] #todas as colunas e só a primeira linha
 a  b 
 1 12 
> mat3[2:3,1] #2° e 3° linha e só a primeira coluna
[1] 2 3
> mat3[2:3,] #linhas 2 e 3, todas as colunas
     a  b
[1,] 2 14
[2,] 3 16
```
### Dataframes
São como bancos de dados, as coluas são variáveis e as linhas são os registros.
- Criando um dataframe: data.frame(nome_do_dataframe)
- Exibindo as primeiras observações: head(nome_do_dataframe)
- Exibindo as últimas observações: tail(nome_do_dataframe)
- Nome das colunas: names(nome_do_dataframe)
- Exibindo o número de linhas e colunas: dim(nome_do_dataframe)
```R
> #dataframes
> data("iris")  #iris é um banco de dado integrado do r, retornei ele ao console
> dados <- iris #coloquei iris no objeto dados
> dados         #li dados
    Sepal.Length Sepal.Width Petal.Length Petal.Width    Species
1            5.1         3.5          1.4         0.2     setosa
2            4.9         3.0          1.4         0.2     setosa
3            4.7         3.2          1.3         0.2     setosa
4            4.6         3.1          1.5         0.2     setosa
5            5.0         3.6          1.4         0.2     setosa
6            5.4         3.9          1.7         0.4     setosa
7            4.6         3.4          1.4         0.3     setosa
8            5.0         3.4          1.5         0.2     setosa
9            4.4         2.9          1.4         0.2     setosa
10           4.9         3.1          1.5         0.1     setosa
11...50
51           7.0         3.2          4.7         1.4 versicolor
52           6.4         3.2          4.5         1.5 versicolor
53           6.9         3.1          4.9         1.5 versicolor
54           5.5         2.3          4.0         1.3 versicolor
55           6.5         2.8          4.6         1.5 versicolor
56           5.7         2.8          4.5         1.3 versicolor
57           6.3         3.3          4.7         1.6 versicolor
58           4.9         2.4          3.3         1.0 versicolor
59           6.6         2.9          4.6         1.3 versicolor
60...150
#criando um dataframe, atenção ao uso da virgula e parentese abertp
> metadados_pac <- data.frame(paciente = c("a01","a02","a03", "a04", "a05"),
+ idade = c(4,48,65,54,72),
+ sexo = c("masculino","feminino", "masculino", "feminino", "masculino"),
+ fumante = c(TRUE, FALSE, FALSE, TRUE, TRUE))
> metadados_pac #retornando ele
  paciente idade      sexo fumante
1      a01     4 masculino    TRUE
2      a02    48  feminino   FALSE
3      a03    65 masculino   FALSE
4      a04    54  feminino    TRUE
5      a05    72 masculino    TRUE
> ?iris #para ler informações do dataframe
> dados[1:5,1:5] #para retornar as 5 primeiras linhas e colunas
  Sepal.Length Sepal.Width Petal.Length Petal.Width Species
1          5.1         3.5          1.4         0.2  setosa
2          4.9         3.0          1.4         0.2  setosa
3          4.7         3.2          1.3         0.2  setosa
4          4.6         3.1          1.5         0.2  setosa
5          5.0         3.6          1.4         0.2  setosa
> names(dados) #para retornar somente o nome das colunas
[1] "Sepal.Length" "Sepal.Width"  "Petal.Length" "Petal.Width"  "Species"     
> dados$Species #Para retornar somente os dados da coluna espécie
  [1] setosa     setosa     setosa    
  [4] setosa     setosa     setosa    
  [7] setosa     setosa     setosa    
 [10] setosa     setosa     setosa    
...
[148] virginica  virginica  virginica 
3 Levels: setosa ... virginica
> dados_spec <- dados$Species #para relacionar ao objeto
> class(dados_spec)
[1] "factor"
> dados$Sepal.Length[1]
[1] 5.1
```
