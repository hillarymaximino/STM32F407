# Lista de Exercício STM32F407
---
### Questão 01
Piscar um led em um frequência de 4Hz, com largura de pulso de 100ms.

---
### Questão 02
Acionar um buzzer para emitir clicamente o seguinte sinal sonoro: 1 beep curto, aguarda um tempo e, em seguida 2 beeps curtos, aguardando mais um tempo.

---
### Questão 03
Acender dois LEDs com diferentes intensidades de brilho, alterando alternadamente a intensidade em tempo de execução: enquanto um LED estiver aumentando o brilho, o outro deve estar diminuindo o brilho.

---
### Questão 04
Utilizar os botões da placa KO, K1 e K_UP para acionar 3 leds, independentemente. Cada vez que um botão for pressionado, o LED correspondente deverá ser acionado. Apenas um dos LEDs deve estar ativo por vez.

---
### Questão 05
Utilizar 3 botões (KO, K1 e K UP) e 2 LEDs (D2 e D3). Os botões KO e K1 correspondem a dois participantes, enquanto o botão K_UP funciona como um botão de reinício. Quando KO for pressionado, o LED D2 deve acender e bloquear o acionamento do outro LED, mesmo que K1 seja pressionado em seguida. Da mesma forma, se K1 for pressionado primeiro, o LED D3 deve acender e impedir que o KO acenda o D2. O LED aceso só pode ser desligado quando o botão K_UP for pressionado, liberando o sistema para uma nova rodada. Esse tipo de lógica é frequentemente utilizado em programas de perguntas e respostas, onde o primeiro jogador que aperta o botão "trava" o sistema, impedindo que o outro responda até que o apresentador libere novamente.

---
### Questão 06
Apresentar uma contagem binária de 8 bits a partir de 8 LEDs externos. (obs.: para facilitar a implementação do código, conecte os LEDs a pinos contiguos de um mesmo GPIO e use a função GPIO_Write_Port () para acionar simultaneamente todos os pinos de uma porta).

---
### Questão 07
Implementar o efeito "LED andante" nos 8 LEDs da questão anterior: ative o primeiro LED e faça com que o LED aceso se desloque do primeiro ao último: Ligue o primeiro LED e, após um tempo, apague esse LED enquanto acende o segundo, e assim sucessivamente até o oitavo LED. O único LED aceso em cada passo deve se deslocar de um extremo a outro e em seguida fazer a operação no sentido inverso.

---
### Questão 08
Simular o funcionamento de um cruzamento viário com dois semáforos de trânsito usando 6 LEDs.

---
### Questão 09
Apresentar uma contagem hexadecimal (crescente e decrescente) de um dígito em um display de 7 segmentos. A contagem deve incrementar de 0x0 até 0xF e em seguida decrementar até 0x0 novamente, repetindo o processo indefinidamente.

---
### Questão 10
Apresentar uma contagem hexadecimal (crescente e decrescente) de dois dígitos em dois displays de 7 segmentos. A contagem deve incrementar de 0x00 até 0xFF e em seguida decrementar até 0x00 novamente, repetindo o processo indefinidamente. (obs.: utilize a técnica de multiplexação para usar a menor quantidade possível de terminais. Utilize transistores como drive de potência para fazer a comutação do sistema de multiplexação).

---
### Questão 11
Exibir o seu primeiro nome na primeira linha de um display de cristal líquido, o segundo nome na segunda IIinha, o terceiro nome na terceira e uma contagem regressiva de 10 até 0 na quarta linha, repetindo o processo
indefinidamente.

---
### Questão 12
Implementar o controle de velocidade de um motor DC para que ele acelere suavemente até sua
velocidade máxima e em seguida desacelere suavemente e repita o mesmo procedimento no sentido contrário, repetindo o processo indefinidamente. Utilize uma ponte H como drive de potência para o motor e uma frequência PWM de 2kHz.

---
### Questão 13
Realizar o acionamento de um motor de passo bipolar. O eixo do motor deve fazer dois giros completos no sentido horário e depois um no sentido anti-horário, repetindo o processo indefinidamente. Realize o acionamento através de passo completo. (obs.: utilize duas pontes H como drive de potência).

---
### Questão 14
Escreva um programa que, ao pressionar o botão KO, o LED D2 da placa seja ligado e permaneça ligado por aproximadamente 2 segundos e, ao pressionar o botão K1, o LED D3 da placa seja ligado e permaneça ligado por aproximadamente 4 segundos. Ao final dos respectivos períodos, os LEDs devem ser desligados e aguardar um novo pressionamento dos botões para repetir o processo. Os botões devem ser monitorados pelas interrupções externas dos seus respectivos pinos: PE4 para o botão KO e PE3 para o botão K1. Os períodos durante os quais os LEDs são acionados não devem travar/bloquear o programa. Se o LED D2 já estiver ligado e um novo pressionamento em KO for feito, um novo intervalo de 2 segundos deve ser iniciado a partir do pressionamento do botão. Por exemplo, se o LED D2 já estiver ligado há 1,5 segundos desde o último pressionamento do botão KO e o usuário pressionou o botão mais uma vez, o LED só será desligado após 2 segundos deste último pressionamento, ficando ligado por um tempo total de 3 segundos e meio. Em resumo, a cada pressionamento do botão KO, o LED só poderá ser desligado após 2 segundos, independentemente de quando ocorreu o pressionamento, se quando o LED já estava ligado ou se quando o LED estava apagado. O mesmo não deve ocorrer com o LED D3 e o botão K1. Isto é, mesmo que o usuário pressione o botão K1 enquanto o LED D3 estiver ligado, primeiro deverá ser concluído o período de 3 segundos para, em seguida, poder atender novos pressionamentos do botão K1.

---
### Questão 15
Utilizar dois push-buttons (KO e K1) para acionar um LED com a seguinte regra: o LED só deve acender se o usuário pressionar os dois botões juntos, mas primeiro o botão KO deve ser pressionado e só depois o botão K1.

---
### Questão 16
Utilizar dois push-button (KO e K1) para acionar um LED com a seguinte regra: o LED só deve acender se o usuário pressionar os dois botões juntos, mas primeiro o botão KO e em seguida o botão K1. Se o botão K1 não for pressionado dentro de no máximo 1 segundo após KO ser pressionado, o LED não deve acender.

---
### Questão 17
Controlar um micro servomotor para que ele alterne lenta e suavemente a posição do seu eixo entre 0° e 180° por meio de dois push-buttons, sendo um para aumentar o ângulo de posicionamento do eixo e outro para diminuir.

---
### Questão 18
Utilizar um teclado de membrana 4x4, fazendo sua decodificação, apresentando a tecla pressionada em um display de 7 segmentos

---
### Questão 19
Fazer a leitura de um sensor de proximidade ultrassônico, semelhante aos sensores de estacionamento de automóveis. Escolher 3 limiares de distância ( D * 1 = 10cm , D * 2 = 30cm D * 3 = 50cm ) , sinalizando a distância medida por meio de um buzzer. Se a distância medida for maior que 50cm, o buzzer não deve ser acionado. Se a distância medida estiver entre 50cm e 30cm, o buzzer deve emitir beeps a uma frequência baixa. Se a distância medida estiver entre 30cm e 10cm, o buzzer deve emitir beeps a uma frequência intermediária. Se a distância medida for menor que 10cm, o buzzer deve emitir beeps a uma frequência alta.

---
### Questão 20
Utilizando 4 botões e 4 Leds externos, implementar o antigo jogo da memória "Genius". (Para criar aleatoriedade, utilize a função Random_Number() da biblioteca Utility.h, que retorna um número inteiro sem sinal de 32 bits).

---





