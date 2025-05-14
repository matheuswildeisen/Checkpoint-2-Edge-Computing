# 🍷 Projeto Vinheria Agnello - Checkpoint 02

**Disciplina:** Engenharia de Software - Edge Computing & Computer Systems  
**Turma:** 1ESPW  
**Professor:** Lucas Demetrius Augusto  
**Data de Entrega:** 16/05/2025

---

## 📌 Descrição do Projeto

Este projeto tem como objetivo desenvolver um sistema de monitoramento ambiental para a **Vinheria Agnello**, garantindo as condições ideais de armazenamento dos vinhos. O sistema simula um ambiente inteligente capaz de monitorar a **temperatura**, **umidade** e **luminosidade**, alertando o usuário em caso de situações críticas e exibindo os dados em um display LCD.

### Interagindo com o Projeto
- Para testar o sensor de luminosidade, altere a iluminação do ambiente (ou ajuste a simulação no Wokwi).

- Para testar temperaturas e umidades fora do ideal, ajuste os valores no simulador ou use um sensor físico em ambientes controlados.

- Observe que o sistema atualiza os valores e os alertas a cada 5 segundos, mostrando uma média de 5 leituras para maior precisão.

### Dicas Finais
- Certifique-se que todos os componentes estejam bem conectados.

- Caso o display não mostre nada, verifique a comunicação I2C e o endereço do display.

- Sempre acompanhe os alertas para garantir que o ambiente esteja adequado para o armazenamento dos vinhos.

---

## 🎯 Objetivos Técnicos

- Medir **temperatura** e **umidade** com o sensor **DHT22** (substituindo o DHT11).
- Medir **luminosidade** com um sensor **LDR**.
- Exibir os valores no **display LCD I2C**.
- Utilizar **LEDs** e **buzzer** como alertas visuais e sonoros.
- Realizar a **média de 5 leituras** dos sensores.
- Atualizar os dados no LCD a cada **5 segundos**.

---

## 🧰 Componentes Utilizados

- Arduino UNO
- Sensor DHT22 (substituindo DHT11)
- Sensor LDR
- Display LCD I2C (16x2)
- LEDs: verde, amarelo e vermelho
- Buzzer
- Resistores
- Protoboard e fios de conexão

---

### ⚙️ Funcionalidades: 
⚙️ Explicação Técnica do Funcionamento
O projeto simula um sistema embarcado de monitoramento ambiental para a Vinheria Agnello, que realiza a leitura de três variáveis fundamentais para a conservação do vinho: temperatura, umidade e luminosidade.

### 🧪 Leitura dos Sensores
O sensor DHT22 coleta os valores de temperatura (em °C) e umidade relativa do ar (em %).

Um sensor LDR (fotoresistor) mede a intensidade de luz no ambiente.

Cada sensor realiza 5 leituras consecutivas com pequenos intervalos e calcula-se a média, garantindo maior precisão nas medições.

### Lógica de Controle:

### 💡 Luminosidade:
- **Escuro**: LED **verde** aceso.
- **Meia luz**: LED **amarelo** aceso + mensagem "Meia luz" no LCD.
- **Muito claro**: LED **vermelho** aceso + mensagem "Luz alta" + buzzer ligado.

### 🌡️ Temperatura:
- **Entre 10°C e 15°C**: Mensagem "Temp OK" + valor exibido.
- **Abaixo de 10°C**: LED **amarelo** + mensagem "Temp Baixa" + buzzer.
- **Acima de 15°C**: LED **amarelo** + mensagem "Temp Alta" + buzzer.

### 💧 Umidade:
- **Entre 50% e 70%**: Mensagem "Umidade OK" + valor exibido.
- **Abaixo de 50%**: LED **vermelho** + mensagem "Umid. Baixa" + buzzer.
- **Acima de 70%**: LED **vermelho** + mensagem "Umid. Alta" + buzzer.

### 📺 Display LCD
- O display LCD I2C (16x2) alterna entre mensagens de status e os valores médios de temperatura e umidade, atualizados a cada 5 segundos. Isso fornece ao usuário informações em tempo real sobre o ambiente.

---

## 🖥️ Simulação no Wokwi

🔗 [Clique aqui para acessar o projeto no Wokwi](https://wokwi.com/projects/429251841577819137)

---

## 🧠 Desafios e Soluções

- **Leitura de sensores múltiplos:** Resolvemos utilizando arrays e média de 5 leituras.
- **Gerenciamento de tempo:** Usamos a função `millis()` para evitar `delay()` excessivos.
- **Mensagens no LCD:** Priorizamos clareza e alternância entre status e valores numéricos.

---

## 🗣️ Explicação em Vídeo

🎥 *(Inserir link do vídeo após gravação)*

---

## 📝 Autores

- Matheus von Koss Wildeisen - RM: 561539
- Ana Clara Rocha de Oliveira – RM: 564298
- Joao Nishikawa – RM: 562376
- Deivid ruan Marques – RM: 566356
- Felipe Cordeiro - RM: 566518
