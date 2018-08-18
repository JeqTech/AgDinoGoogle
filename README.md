# Algoritmo Genético
# Jogo do Chrome Dinossauro automatizado.


Este projeto tem como fonte principal os códigos dos link abaixo.

https://github.com/ivanseidel/IAMDinosaur
https://github.com/ajaiswal-ht/imdino

Usando Python v2.7 e Tensoflow, utiliza algoritmos genéticos com uma evolução constante com o passar das gerações.
Consiste em um mecanismo de busca direcionada baseado na evolução dos seres biológicos.
Provêem técnicas eficazes (mas não tão eficientes) de otimização e de aprendizado de máquina.
Para saber mais recomendo a leitura abaixo.

http://edirlei.3dgb.com.br/aulas/ia_2012_1/IA_Aula_04_Algoritmos_Geneticos.pdf


## Requirements:
- redis
- flask
- tensorflow, numpy
- pyautogui for key presses
- npyscreen for displaying stats
- virtual environment


clone o código
```
git clone https://github.com/JeqTech/AgDinoGoogle.git
```

O sistema utilizado para realizar o procedimento foi o MacOS, portanto, foi ajustado as dependências de acordo com o sistema operacional.

Instale redis
Redis é um open source (licenciado pelo BSD), armazenamento de estrutura de dados na memória, usado como banco de dados, cache e message broker.
https://redis.io/

```
brew install redis
```

Crie um virtualenv com o nome do projeto que deseja:

```
virtualenv dino
source dino/bin/activate
```

Instale as dependências
```
pip install -r requirements.txt
```


##For capturing data :

Inicie o Redis Server
```
redis-server
```

Execute:

```
python fl.py

```

Copie o código abaixo:

```
var http = new XMLHttpRequest();setInterval(function(){
var obs = Runner.instance_.horizon.obstacles.length;
if(obs==0){
  var fs = null;
  var fd = null;
}
else{
   var fs=Runner.instance_.horizon.obstacles[0].width;
   var fd=Runner.instance_.horizon.obstacles[0].xPos;}
var d = { "s": Runner.instance_.currentSpeed/13, "fs":fs/60.0 , "fd": fd/50.0, "sc": Runner.instance_.distanceRan*.025, "o":Runner.instance_.crashed , "n": obs}
var url='http://127.0.1:5000/?r='+JSON.stringify(d);http.open("GET", url);
http.send(null);console.log('yes');}, 90)
```

Agora abra o chrome e digite no navegador "chrome://dino/", clique com o botão na pagina e vá em "Inspencionar", na aba console cole o códico copiado acima e de um enter.
Retorne para a pagina do jogo. Mova o navegador até a parte mais baixa possivel.


## Running game
Encurtar a largura da janela do navegador em 2/3 do tamanho da tela. Abra o terminal e ajuste o tamanho do ecrã para 1/3 do espaço restante. Ative o virtualenv e execute na pasta src:

```
python main.py

```
###  Propostas de melhorias:
* Atualizar o código e as bibliotecas para mais rescentes .
* Atualizar o código e as bibliotecas para versões mais recentes .
* Realizar hum Processo de Simulação fazer Aprendizado fazer algortimo genético, AO inves de executar em Tempo Real, podera acelerar o Processo de Aprendizado.



Credits:

Project: https://github.com/aymericdamien/TensorFlow-Examples/
