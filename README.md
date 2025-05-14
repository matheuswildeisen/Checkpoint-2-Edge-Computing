# 🍷 Projeto Vinheria Agnello - Checkpoint 02

**Disciplina:** Engenharia de Software - Edge Computing & Computer Systems  
**Turma:** 1ESPW  
**Professor:** Lucas Demetrius Augusto  
**Data de Entrega:** 16/05/2025

---

## 📌 Descrição do Projeto

Este projeto tem como objetivo desenvolver um sistema de monitoramento ambiental para a **Vinheria Agnello**, garantindo as condições ideais de armazenamento dos vinhos. O sistema simula um ambiente inteligente capaz de monitorar a **temperatura**, **umidade** e **luminosidade**, alertando o usuário em caso de situações críticas e exibindo os dados em um display LCD.

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

## ⚙️ Funcionalidades

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
