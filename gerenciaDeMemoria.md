# Gerência de memoria

## Introdução

O sistema operacional tem duas funções, a primeira e servir de interface entre a maquina e o usuário, a segunda e servir como gerenciador de recursos, para saber quando ele deve alocar um determinado recursos para um programa e quando ele deve retirar um determinado recurso de um outro programa

Um sistema computacional possui varis recursos sendo os dois principais, o processador, e a memória

nesta apresentação iremos entender como o sistema operacional administra a memória, que e um dos mais importantes recursos do sistema operacional

## A memória ideal segundo os programadores

Idealmente os programadores querem uma memória que seja:

- **Grande**, para armazenar enormes quantidades de informação
- **Rápida**, uma memoria que de uma resposta o quanto antes do acesso que foi solicitado
- **Não volátil**, quanto eu desligar o computador as informações contidas na memória devem ser mantidas, persistidas, ate que o usuário estrua a computador a excluir tal informação da memória
- **De baixo custo**, que não seja preciso pagar muito para ter essa memória

Infelizmente, a pesar da grande evolução da tecnologia nos últimos anos nem sempre a memória do sistema em que estamos trabalhando possui todos estes benefícios.

E por vezes os programadores precisam se adequar a esse ambiente de polca me moria, memórias lentas, voláteis, e de alto custo.

## Hierarquia de memória

O sistema de computação possui diversos tipos de memória que são organizadas de maneira hierárquica, são elas

**Register**, ou registrador, são essencialmente memórias que se encontram dentro do processador e consequentemente como ela se encontra dentro do processador a distancia percorrida para acessar uma informação e pequena, e menor do que acessar de uma memória principal, ou seja ele e mais rapido na hora de acessar informações.

**Cache, (L2 Cache)**, e uma memória intermediaria que fica entre a memória principal e a própria CPU, e possui vários níveis, esses níveis representam essencialmente o local onde as cache se localizam.

Essa divisão em níveis da memória cache existe por conta dos sistemas que usam arquitetura multicor, neste caso cada cache pode ser usado por um ou mais cores do sistema.

**Main Memory**, ou memória ram, são memórias consideradas memórias principais, quanto maior a memória ram, melhor para a aplicação do usuário, pois ela tera mais espaço de trabalho.

**Disk**, ou armazenamentos persistentes, e não voláteis, ou seja você desligou o computador as informações contidas nesta memória continuam armazenadas e não são excluídas.

## Tarefas do Gerenciador de Memória

- **Gerenciar a hierarquia de memória**
 - Gerenciar espaços livres/ocupados
 - Alocar e localizar processos/dados na memória.
- **Controlar as partes que estão em uso, e as que não, para:**
 - **Alocar** memória aos processos, quando estes precisarem.
 - **Liberar** memória quando um processo termina.
 - Tratar do problema do **swapping.** Responsável por gerenciar **chaveamento entre a memória principal e o disco** e memória principal e memória cache.

Se você não entendeu o que e **swapping** não se preocupe, mas afrente nesta apresentação isso sera explicado.

Todo esse trabalho e feito por um modulo do sistema operacional que se chama gerenciador de recursos.

## Gerencia de Memória - Monoprogramação

Em sistemas operacionais mono tarefas e monoprogramação e memória era usa de 3 formas diferentes

A primeira e mais intiga em mainframes(computadores de grande porte), o sistema operacional era armazenado na memória principal 

O segundo usada em alguns handhelds(Sistemas moveis por exemplo), tem o sistema operacional aramzenado em uma mamória de leitura apenas, ou seja fez o boot, assim que o boot e feito essa memória de leitura e acessada para caregar o sistema operacional.

E a terceiro forma de gerenciamento de memória em sistemas operacionais mono tarefas e monoprogramação foi usada em computadores pessoais, onde o sistema operacional ficava na memória principal começando com o endereço 0 e os drivers de dispositivos, (driverns de dispositivos são softwares que controlam o dispositivo) ficam armazenados em memorias apenas de leitura.
