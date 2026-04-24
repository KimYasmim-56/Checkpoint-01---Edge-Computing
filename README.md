# Checkpoint-01---Edge-Computing

🍷 Sistema de Monitoramento de Luminosidade para Vinheria

📌 Descrição do Projeto

Este projeto foi desenvolvido como parte de um desafio proposto pela Vinheria Agnello. O objetivo é criar um sistema de monitoramento de luminosidade utilizando Arduino, garantindo que as condições ambientais estejam adequadas para o armazenamento de vinhos.

A luminosidade é um fator crítico que pode impactar diretamente a qualidade do vinho. Portanto, o sistema coleta dados do ambiente e sinaliza possíveis problemas por meio de LEDs e um buzzer.


🎯 Objetivos
- Monitorar a luminosidade do ambiente utilizando um sensor LDR.
- Converter sinais analógicos em digitais através do ADC do Arduino.
- Indicar o estado do ambiente com LEDs:
🟢 Verde: Ambiente OK;
🟡 Amarelo: Nível de alerta;
🔴 Vermelho: Problema detectado.
Acionar um buzzer quando houver problema na luminosidade.

🛠️ Componentes Utilizados
- Arduino (Uno, Nano ou similar);
- LDR (serve para medir a luz do ambiente);
- Resistores (para divisor de tensão e LEDs).
- LEDs(indicar a luminosidade ideal para a conserva do vinho):
  Verde ;
  Amarelo ;
  Vermelho.
- Buzzer;
- Protoboard;
- Jumpers.

⚙️ Funcionamento do Sistema

1. O LDR capta a intensidade luminosa do ambiente.
2. O Arduino lê o valor analógico através de sua porta ADC.
3. Com base em limites pré-definidos:
- Valor dentro do ideal → LED verde aceso;
- Valor em alerta → LED amarelo aceso;
- Valor crítico → LED vermelho aceso + buzzer ativado.
4. Caso o problema persista, o buzzer é acionado novamente por 3 segundos.

🔌 Esquema Básico

- LDR conectado em um divisor de tensão (entrada analógica A0);
- LEDs conectados a pinos digitais (com resistores);
- Buzzer conectado a um pino digital.

💡 Lógica de Controle (Resumo)

if (luminosidade < limite_ok) {
  // LED verde
}
else if (luminosidade < limite_alerta) {
  // LED amarelo
}
else {
  // LED vermelho + buzzer
}

🔔 Comportamento do Buzzer

- Ativado quando a luminosidade estiver em nível crítico;
- Permanece ligado por 3 segundos;
- Reativa caso o problema continue.

📊 Possíveis Melhorias

- Monitoramento de temperatura e umidade;
- Integração com display LCD/OLED;
- Envio de dados para a nuvem (IoT);
- Notificações via aplicativo.

🚀 Como Executar

1. Monte o circuito conforme descrito;
2. Conecte o Arduino ao computador;
3. Faça upload do código via Arduino IDE;
4. Observe os LEDs e o buzzer conforme a variação de luz.

📚 Conceitos Envolvidos

- LDR (Sensor de luz);
- Divisor de tensão;
- Conversão Analógico-Digital (ADC);
- Sistemas embarcados;
- Monitoramento ambiental.

📄 Licença

Este projeto é de uso educacional.