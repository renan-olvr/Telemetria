# Telemetria

Este documento tem por objetivo auxiliar na documentação dos processos de telemetria utilizados nos drones do laboratório, incluindo o hardware utilizado, o modo de funcionamento e recomendações de uso.
Também estão incluídos os métodos já utilizados, os problemas enfrentados e sugestões de melhorias.


## Harware utilizado


## Sik Radio

![radio_telemetry](/docs/SikRadio/img/radio_telemetry_915mhz.png)

Este conjunto de transmissor e receptor possui conectores apropriados para serem conectados aos controladores da [Pixhawk Series](https://github.com/PX4/PX4-Autopilot/blob/main/docs/en/flight_controller/pixhawk_series.md).
A sua utilização se dá pelo fato de possuir um grande alcance, podendo chegar a mais de 5km com antenas comuns. A frequência que os módulos operam é de 915MHz, o que torna possível esse longo alcance, porém, em contrapartida, limita a taxa de transmissão de dados a alguns kbps.

### Conexão

O módulo com entrada USB é conectado a algum computador, enquanto o outro módulo é conectado à controladora de voo na porta **TELEM1**, como mostra a figura abaixo.

![px4_telemetry_radio](/docs/SikRadio/img/px4_telemetry_radio.jpg)

> [!NOTE]
> A extremidade do cabo que vai na controladora possui um conector de 6 pinos, porém apenas 4 fios são utilizados. Caso não possua esse cabo, você pode fazer uma adaptação, respeitando sempre o pinout.

Confira um exemplo de uso aqui (add hiperlink em aqui).

### Problemas enfrentados


## ESP32

Drone Bridge para ESP32 é um solução desenvolvida para telemetria de baixa taxa de dados, que se encaixa perfeitamente ao nosso propósito, permitindo converter uma transmissão serial totalmente transparente para WiFi.
Ele pode rodar em praticamente todas as placas de desenvolvimento ESP32. Recomenda-se o uso de placas e módulos com conector para antena externa, pois estes oferecem maior alcance.

![DroneBridge-ESP32](/docs/ESP32/img/drone_bridge_ESP32.avif)

O modelo utilizado é o [ESP32_DevKitC_V4][https://docs.espressif.com/projects/esp-idf/en/release-v4.2/esp32/hw-reference/esp32/get-started-devkitc.html], que pode ser visto abaixo.

![esp32_devkitc_v4_antenna](/docs/ESP32/img/esp32_devkitc_v4_antenna.png)

### Conexão

Conecte a UART do ESP32 à UART 3.3V da controladora de vôo (nesse caso, a px4). Siga o esquema de ligação abaixo.

![telem2-layout](/docs/ESP32/img/telem2_layout.png)

>[!ATENTION]
> O ESP32 deve sempre ser conectado à porta **TELEM2**.

### Problemas enfrentados


## Sugestões
