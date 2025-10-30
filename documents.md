# Semáforo - IOT

## Autor
**Nome:** Rafael Cabral da Silva  
**Turma:**  15 
**Grupo:** 2

## Sobre o projeto
O projeto é um protótipo de um semáforo, na qual usa componentes eletrônicos e programação para representar sua aplicabilidade no dia a dia da sociedade. 

## Regra de negócio:
#### Acionamento: 
No circuito existe um botão que começa o loop no vermelho e ao ser pressionado pela segunda vez, desliga todos os leds. Assim, repetidamente. 

#### Duração em cada estágio do loop: <br>
**Vermelho**: 6 segundos <br>
**Verde** : 4 segundos <br>
**Amarelo**: 2 segundos <br>

#### Montagem

| Item | Especificação | Conexão 
|-------------|-------------|-------------|
| Microcontrolador| ESP32 | USB notebook
| Led vermelho| 2 volts | porta 25
| Led amarelo| 2 volts | porta 26
| Led verde| 2 volts | porta 27
| resistor| 330 ohms | - Led vermelho
| resistor| 330 ohms | - Led amarelo
| resistor| 330 ohms | - Led verde
| resistor| 1k ohms | - Led botão
| botão| ---| porta 34
| jumpers| ---| ---
| protoboard| ---| ---

#### Resumo
Basicamente, os polos negativos dos leds estão conectados a resistores, que por sua vez estão ligados ao GND do ESP32. Enquanto os polos positivo estão ligados nos pinos do ESP32 descritos na tabela anterior. O botão segue a mesma lógica dos leds, com a única alteração de que ele recebe no seu lado positivo o pino 3.3v do ESP32, e possui um jumper no mesmo lado do negativo que vai para a porta analógica 34

## Demonstração
#### Vídeo do funcionamento no YouTube
[Acesse aqui!](https://youtu.be/ZeOBXryTUpY?feature=shared)
### Imagens do circuito
<img src="assets\semaforo_1.jpg">
<img src="assets\semaforo_2.jpg">
<img src="assets\semaforo_3.jpg">

### Código do circuito
<img src="assets\code_semaforo.png">
<img src="assets\code_semaforo2.png">

## Avaliação em pares

**Avaliador X**: 
| Critério | Contempla (Pontos) | Contempla Parcialmente (Pontos) | Não Contempla (Pontos) |Observações do Avaliador
|-------------|-------------|-------------|-------------|-------------|
Montagem física com cores corretas, boa disposição dos fios e uso adequado de resistores| Até 3 | Até 1,5 | 0 | X |
Temporização adequada conforme tempos medidos com auxílio de algum instrumento externo| Até 3 | Até 1,5 | 0 | X |
Código implementa corretamente as fases do semáforo e estrutura do código (variáveis representativas e comentários)| Até 3 | Até 1,5 | 0 | X |
Ir além: Implementou um componente de extra, fez com millis() ao invés do delay() e/ou usou ponteiros no código| Até 1 | Até 0,5 | 0 | X |
| |  | | | X |
| |  | | | Pontuação Total |

<br>

**Avaliador Y**: 
| Critério | Contempla (Pontos) | Contempla Parcialmente (Pontos) | Não Contempla (Pontos) |Observações do Avaliador
|-------------|-------------|-------------|-------------|-------------|
Montagem física com cores corretas, boa disposição dos fios e uso adequado de resistores| Até 3 | Até 1,5 | 0 | Y |
Temporização adequada conforme tempos medidos com auxílio de algum instrumento externo| Até 3 | Até 1,5 | 0 | Y |
Código implementa corretamente as fases do semáforo e estrutura do código (variáveis representativas e comentários)| Até 3 | Até 1,5 | 0 | Y |
Ir além: Implementou um componente de extra, fez com millis() ao invés do delay() e/ou usou ponteiros no código| Até 1 | Até 0,5 | 0 | Y |
| |  | | | Y |
| |  | | | Pontuação Total |