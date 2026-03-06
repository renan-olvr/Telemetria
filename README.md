# Telemetria

Este documento tem por objetivo auxiliar na documentação dos processos de telemetria utilizados nos drones do laboratório, incluindo o hardware utilizado, o modo de funcionamento e recomendações de uso.
Também estão incluídos os métodos já utilizados, os problemas enfrentados e sugestões de melhorias.


## Harware utilizado


## Sik Radio

![radio_telemetry](/docs/img/radio_telemetry_915mhz.png)

Este conjunto de transmissor e receptor possui conectores apropriados para serem conectados aos controladores da [Pixhawk Series](https://github.com/PX4/PX4-Autopilot/blob/main/docs/en/flight_controller/pixhawk_series.md).
A sua utilização se dá pelo fato de possuir um grande alcance, podendo chegar a mais de 5km com antenas comuns. A frequência que os módulos operam é de 915MHz, o que torna possível esse longo alcance, porém, em contrapartida, limita a taxa de transmissão de dados a alguns kbps.

### Conexão

O módulo com entrada USB é conectado a algum computador, enquanto o outro módulo é conectado à controladora de voo na porta ** TELEM1 **, como mostra a figura abaixo.

![px4_telemetry_radio](/docs/img/px4_telemetry_radio.jpg)

> [!NOTE]
> A extremidade do cabo que vai na controladora possui um conector de 6 pinos, porém apenas 4 são utilizados. Caso não possua esse cabo, você pode fazer uma adaptação, respeitando sempre o pinout.

Confira um exemplo de uso aqui (add hiperlink em aqui).

### Problemas enfrentados


## ESP8266

## Sugestões
