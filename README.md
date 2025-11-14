# Global-Solution---Edge
# Grupo:
Cristian Belasco Arancibia RM:565710

Victor Antonio Teixeira da Silva Rm: 562573

Lucas Oliveira de Mendonça Almeida RM:562613
# Link para o projeto:
https://wokwi.com/projects/447539582011144193
# Link para o video:

# Sistema de Monitoramento Sustentável – Global Solutions 2025

Esse projeto é uma ideia simples para mostrar como tecnologias como ESP32, sensores e MQTT podem ajudar no tema economia verde e sustentabilidade dentro do futuro do trabalho.
A ideia geral é usar sensores para entender como está o ambiente e avisar quando algo foge do ideal — assim dá pra economizar energia, melhorar o conforto e tomar decisões melhores.

# O que o sistema faz

O ESP32 coleta dados do ambiente usando:

DHT22 → temperatura e umidade

Ultrassônico → mede a distância (pode representar presença de pessoas num espaço)

LEDs (verde, amarelo, vermelho) → mostram rapidamente a situação do ambiente

Buzzer → dispara quando algo está crítico

MQTT → envia tudo para um broker (o servidor que recebe/troca mensagens)

Esse conjunto permite entender em tempo real se o ambiente está confortável, se está começando a ficar ruim ou se já virou alerta vermelho.
Quanto mais cedo você percebe esses sinais, mais fácil é tomar decisões que evitam desperdício de energia — como ar-condicionado forte demais, aquecedor desnecessário, espaço sem ventilação, etc.

# Como funciona a lógica

- O LED muda de cor dependendo da combinação entre:

Temperatura

Umidade

Distância medida pelo ultrassônico

- Resumo:

Verde → tudo está dentro do normal

Amarelo → condições começando a sair do confortável

Vermelho → algo está ruim (temperatura alta ou pessoa muito próxima), buzzer liga

Além disso, o ESP32 manda esses dados via MQTT em formato JSON

Esse JSON pode ser usado em dashboards, relatórios, automações… o que fizer sentido.

# Comunicação MQTT

O dispositivo publica em dois tópicos:

gs2025/office1/env → sempre manda temperatura, umidade, distância e status

gs2025/office1/alert → manda alerta apenas quando está no nível crítico

Essas mensagens são leves e funcionam bem em qualquer broker público como HiveMQ ou EMQX.

# Testes no Wokwi

O projeto roda bem no Wokwi usando:

Wokwi-GUEST como rede WiFi (sem senha)

Um broker MQTT público (ex.: broker.hivemq.com)

Durante o teste você pode mudar manualmente a temperatura ou a distância no simulador para ver o LED mudando e o buzzer acionando.
Também dá pra abrir o painel MQTT para ver os dados chegando.

# Por que isso importa no tema “Economia Verde e Sustentabilidade”?

O foco principal é mostrar que dá para:

Monitorar o ambiente em tempo real

Evitar uso excessivo de climatização

Reagir rápido a situações desconfortáveis

Criar espaços de trabalho mais saudáveis

Reduzir consumo energético com base em dados

Não é sobre criar um produto pronto, mas sim mostrar como uma pequena automação pode ajudar nesse caminho.
Esse tipo de solução escala muito bem: dá pra usar em salas, escritórios híbridos, coworkings ou até home office.

# O que está incluído

Código usando ESP32 + DHT22 + Ultrassônico + MQTT

LED verde/amarelo/vermelho indicando o nível atual

Buzzer ligado somente quando algo está crítico

JSON publicado em tópicos MQTT

Lógica simples de “conforto → atenção → alerta”

Estrutura clara para expandir (mais sensores, automações, dashboards, etc.)

# Fotos:
<img width="677" height="755" alt="image" src="https://github.com/user-attachments/assets/6a412217-449a-4cc2-8f9b-146f8a22b835" />
<img width="961" height="857" alt="image" src="https://github.com/user-attachments/assets/e6cfc00e-d04b-49c4-86b0-88246c9ec97b" />


