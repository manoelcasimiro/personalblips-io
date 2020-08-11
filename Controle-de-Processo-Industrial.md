---
date: 2017-05-28 05:54:23
title: Controle de Processo Industrial
description: Fundamentos de malha de controle
category: Auto
background: "#47650b"
---

Existem diferentes controles a serem estudados, mas incialmente devemos conhecer seus fundamentos.

### Planta: 
É o sistema onde estão dispostos organizadamente os equipamentos e instrumentos de medição que formam as malhas de controle de produção. 

<iframe width="853" height="480" src="https://www.youtube.com/embed/kSgkbis_Gj4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Controle Automático: 
Substituímos neste controle, as observações e decisões humanas por um instrumento CLP (controlador lógico programável), que torna automática a produção industrial.

### PV: 
Variável de Processo: No controle industrial temos diferentes variáveis que afetam o processo na produção, sendo as mais importantes, a pressão, o nível, a temperatura e a vazão, sendo que a variável de processo é aquela que desejamos controlar. 
### SP: 
Set Point: São os valores que desejamos que a variável de processo alcance, chamamos o set point de valores desejados. 
### MV: 
Variável Manipulada: Modificamos valores de outra variável(MV), para que a variável de processo (PV) alcance o valor desejado ou set – point (SP).
## Erro: 
Enquanto a variável que desejamos controlar (PV), não chegar ao valor desejado (SP), através das alterações da variável manipulada (MV), haverá um erro, representado por essa diferença entre o valor da PV e do SP. Podemos então representar o erro através da seguinte equação:
> - Erro = PV – SP, quando os valores de PV e SP são diferentes.

### Malha aberta: 
Entendemos com malha aberta, aquela que não corrige os erros, onde não temos a comparação entre a PV e o SP, a saída não está acoplada da entrada 
 
![malha](/assets/img/malha.jpg)

### Malha fechada: 
Podemos dizer que é aquela que a saída está acoplada a entrada, onde a PV captada na saída é comparada com o SP definido na entrada, corrigindo o erro, levando o controle ao valor desejado (PV-SP = 0).  

![malhafechada](/assets/img/malhafechada.jpg)

## Formas de atuação do Controlador 

Atuação Direta: 
A atuação do controlador é direta, quando a variável de processo(PV) ao aumentar o seu valor em relação ao valor desejado(SP), provoca um aumento do valor da variável Manipulada(MV) na saída do controlador. 

Atuação Reversa: 
A atuação do controlador é reversa, quando a variável de processo(PV) ao aumentar o seu valor em relação ao valor desejado(SP) provoca uma redução do valor da variável Manipulada(MV) na saída do controlador. 

## Algoritmos de controle 

 Nesta etapa vamos conhecer os cálculos matemáticos ou algoritmos, onde podemos definir as seguintes ações de controle.  

### On off:  
Para entendermos esta ação devemos saber que a variável manipulada(MV) é o sinal que sai do controlador para o elemento final de controle. 

Na ação On - off o sinal é recebido e é cortado em função do valor desejado de controle (SP), ora tenho sinal, ora não tenho sinal na saída do controlador. 

![onoff](/assets/img/onoff.jpg)
                   ação On-Off

Quando a temperatura (PV) chegar ao valor de ajuste(SP) , o contato fechado do termostato abre, mas a temperatura(PV) é uma variável que demora a responder ultrapassa o valor desejado(SP) e depois com o arrefecimento do aquecedor começa a cair até um valor inferior ao desejado(SP) , fechando o contato novamente. Este ciclo se repete, mantendo a temperatura(PV) próximo ao valor de ajuste (SP) através da circulação e corte da corrente(MV) que alimenta o aquecedor.  

Observamos que na ação On-off temos dois valores extremos, é tudo ou nada, para corrigirmos o erro(PV-SP)   

![controleonoff](/assets/img/controleonoff.jpg)
