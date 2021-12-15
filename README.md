Atividade Avaliativa I
================
edivan dos santos do rosaro
Estat 2021.1

*Questão 01*

*(a)* O erro dele é que o mesmo considerou a mala mais pesada sendo a
que representa o valor do quartis superior e a análise que pelo boxplot
existem malas mais pesadas entre esse quartil e o limite superior
(29kg), onde está localizado 25% da amostra. Portanto, 23kg não
representa a mala mais pesada da distribuição.

*(b)* A mediana é representada pelo segundo quartil, assim, o seu valor
é de 17kg

*(c)* A distância interquartílica é a diferença entre o quartil superior
pelo quartil inferior, assim, a distância seria 23 - 10 = 13.

*(d)* A quantidade de malas presente entre 5kg e 10kg está no primeiro
quartil que corresponde a 25% do total da amostra, assim, corresponderia
a 25% de 240 malas, ou seja, 60 malas.

*Questão 2*

A soma de todas as médias dos 30 alunos, multiplicando 30 pela média
aritmética das notas, ou seja, 6.40 encontrando como resultado 192. Da
mesma forma, obtive a soma total das médias dos outros 50 alunos da
outra turma, multiplicando o total de alunos (50) por 5,20 tendo como
total 260. Feito isso, somei a soma total das médias das duas turma (192
+ 260 = 452) e dividi por 80 (total de alunos correspondentes as duas
turmas) (452/80) . Assim, obtive que a média aritmética dos 80 alunos é
(a) 5,65

*Questão 3*

``` r
X  <- c ( 68 , 70 , 72 , 58 , 90 , 110 , 68 , 70 , 72 , 80 , 80 , 67 , 90 , 94 , 100 , 80 , 75 , 79 , 84 , 90 )
```

*(b)* Média = 79,85; Primeiro quartil = 70,0; Mediana = 79,5; Quartil
Terceiro = 90; Desvio padrão = 12.78681 Para encontrar essa resposta,
utilizei os seguintes códigos

``` r
mean ( X )
```

    ## [1] 79.85

``` r
quantile ( X )
```

    ##    0%   25%   50%   75%  100% 
    ##  58.0  70.0  79.5  90.0 110.0

``` r
median ( X )
```

    ## [1] 79.5

``` r
sd ( X )
```

    ## [1] 12.78681

*(c)* No histograma, é possível perceber uma certa assimetria entre os
valores, por isso que a mediana representa a melhor medida central do
conjunto de dados.

*Questão 04* *(a)* Importei o dataset para o Rstudio com o seguinte
código

``` r
frango_dieta <- read_csv("dados/brutos/frango_dieta.csv") 
```

    ## Rows: 578 Columns: 4

    ## -- Column specification --------------------------------------------------------
    ## Delimiter: ","
    ## dbl (4): peso, tempo, frango, dieta

    ## 
    ## i Use `spec()` to retrieve the full column specification for this data.
    ## i Specify the column types or set `show_col_types = FALSE` to quiet this message.

Ao analisar o conjunto de dados foi possível identificar que cada coluna
representa uma variável (peso, tempo, frango, dieta), cada linha
apresentava sobre as variáveis e cada célula apresentava uma única
observação, logo, este dataset está organizado na forma tidy

*(b)* Usando o código

``` r
mean(frango_dieta$peso )
```

    ## [1] 121.8183

Encontrei que a média do peso dos fragos é 121.8183

*(c)* Usando o código

``` r
sd(frango_dieta$peso )
```

    ## [1] 71.07196

Encontrei como desvio padrão o valor 71.07196

*(d)* A variável peso é quantitativa contínua. A variável tempo é
quantitativa discreta A variável é frango qualitativa nominal A variável
dieta é qualitativa nominal

*Questão 5* Rodando o seguinte código

``` r
N <- 1000
x <- rnbinom(N, 4, .5)
hist(
x,
xlim = c(min(x), max(x)),
probability = T,
nclass = max(x) - min(x) + 1,
col = 'lightblue', xlab = ' ', ylab = ' ', axes = F,
main = 'Positive Skewed'
)
lines(density(x, bw = 1), col = 'red', lwd = 3)
```

![](readme_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

Analisando esse gráfico, é possível perceber que a disposição dos
valores é assimétrica, logo, a mediana é a melhor medida central para
representar esses dados.

*Questao 06*
