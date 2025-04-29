# 🩺 Pulseira IoT para Monitoramento de Sinais Vitais Pediátricos

Este projeto propõe uma solução de saúde inteligente baseada em IoT para monitorar sinais vitais de crianças internadas no Hospital Sabará. A pulseira realiza a leitura contínua de frequência cardíaca, oxigenação do sangue e temperatura corporal, transmitindo os dados para uma plataforma central acessada por médicos e enfermeiros.

---

## 🎯 Objetivo

Desenvolver uma pulseira inteligente capaz de monitorar em tempo real os sinais vitais de pacientes pediátricos, enviando os dados para um sistema, permitindo resposta rápida da equipe médica em casos de emergência e maior conforto para os pacientes.

---

## 🧱 Arquitetura da Solução

A solução é composta por três camadas principais:

### 1. **IoT (Dispositivo)**
- **Paciente (criança):** Fonte dos dados fisiológicos.
- **Sensores:**
  - `MAX30100` – Mede batimentos cardíacos e oxigenação do sangue (SpO₂).
  - `MLX90614` – Mede a temperatura corporal sem contato.
- **Microcontrolador:**
  - `ESP32` – Responsável pela coleta dos dados dos sensores e envio via Wi-Fi.
- **Atuadores (opcional):**
  - `Buzzer/LED` – Para alertas locais em caso de anomalias.

### 2. **Back-end (Plataforma IoT)**
- API construída em `Node.js` para receber dados via MQTT.
- Armazenamento dos dados em `MongoDB`.

### 3. **Aplicação (Visualização)**
- Dashboard Web.
- Acesso para médicos e enfermeiros.
- Exibição dos sinais vitais em tempo real e alertas automáticos.

---

## 🗂 Especificações Técnicas

| Componente        | Especificação                                       |
|-------------------|-----------------------------------------------------|
| ESP32             | Microcontrolador com Wi-Fi embutido                 |
| MAX30100          | Sensor de batimento cardíaco e oxigenação           |
| MLX90614          | Sensor infravermelho para temperatura corporal      |
| Buzzer / LED      | Atuador para alertas locais (opcional)              |
| Plataforma IoT    | Node.js + MongoDB + MQTT                            |
| Visualização      | React.js                                            |

---

## 🧠 Diagrama da Arquitetura

🔗 O diagrama em camadas foi desenvolvido no [draw.io](https://app.diagrams.net/) e no arquivo VitalCare.drawio

### 🖼 Descrição do Diagrama

1. **Paciente**: Fonte dos sinais vitais.
2. **Sensores (MAX30100 e MLX90614)**: Realizam a coleta de batimentos, oxigenação e temperatura.
3. **ESP32**: Envia os dados via Wi-Fi para o servidor.
4. **Servidor**: Recebe os dados, processa e salva no banco.
5. **Dashboard**: Visualização pelos médicos e enfermeiros.
6. **Usuários**: Profissionais de saúde têm acesso.

---

## 👥 Equipe

- Diogo Cecchini      RM560427
- Gustavo Neri        RM560239
- Gustavo Pandolfo    RM560271
- Matheus Aparecido   RM559813


