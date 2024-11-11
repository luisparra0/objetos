# Descrição do Projeto

Este projeto utiliza um microcontrolador ESP8266 para coletar dados ambientais (temperatura e umidade) a partir de um sensor DHT11 e enviá-los para a plataforma Adafruit IO via protocolo MQTT. A comunicação ocorre via rede Wi-Fi, e o envio dos dados é realizado em intervalos regulares de 5 segundos. Com isso, é possível monitorar em tempo real as condições ambientais do local em que o dispositivo está instalado. O projeto pode ser utilizado em aplicações domésticas, industriais ou agrícolas, como uma forma de monitoramento remoto de condições climáticas.

## Software Desenvolvido

O código foi desenvolvido em C++, utilizando a IDE do Arduino, que é amplamente utilizada para programas embarcados. O código inicializa o sensor DHT11 e se conecta a uma rede Wi-Fi. Em seguida, conecta-se ao broker MQTT da Adafruit IO para enviar os dados coletados.

O código possui uma estrutura que garante a reconexão automática ao servidor MQTT caso a conexão seja perdida. Também é responsável por ler os valores do sensor, arredondá-los e transmiti-los de forma segura para os feeds definidos. Cada parte do código está comentada para facilitar a compreensão, explicando o funcionamento de cada função e o propósito de cada comando.

## Hardware Utilizado

- Placa de Desenvolvimento: NodeMCU ESP8266, utilizado como microcontrolador principal, pois oferece um processador eficiente e comunicação Wi-Fi integrada.

- Sensor DHT11: Responsável por medir a temperatura e umidade do ambiente.

- Protoboard e Jumpers: Utilizados para facilitar as conexões durante o desenvolvimento e prototipagem.

- Fonte de Alimentação: O ESP8266 pode ser alimentado via USB (5V) ou com uma fonte de energia externa.


## Interfaces, Protocolos e Módulos de Comunicação

- Wi-Fi: Utiliza o módulo Wi-Fi do ESP8266 para conectar à internet.

- Protocolo MQTT: Para a comunicação com o Adafruit IO, é utilizado o protocolo MQTT, que é leve e eficiente para o envio de dados em aplicações IoT.

- Adafruit IO: Serve como broker MQTT, onde os dados enviados são armazenados e visualizados.

- DHT11: Comunicação com o ESP8266 através de um pino digital, utilizando a biblioteca DHT para Arduino.

## Comunicação via Internet e Protocolo MQTT

Este projeto utiliza a pilha TCP/IP do ESP8266 para conectar-se à internet e ao servidor MQTT da Adafruit. A conexão é realizada utilizando a porta 1883, padrão do protocolo MQTT. A transmissão dos dados ocorre de forma periódica, garantindo que as informações coletadas estejam sempre atualizadas no painel do Adafruit IO, permitindo ao usuário o monitoramento remoto de temperatura e umidade através de um navegador ou aplicação móvel. Também é possível acompanhar as atualizações via aplicativo MQTT-IOT (versão IOS) ou via MQTT-Dashboard (versão ANDROID).


## Como reproduzir o Proejto

- Clone o código presente em  https://github.com/luisparra0/objetos.git  para sua máquina local.

- Instalar a IDE do Arduino: Certifique-se de ter a IDE do Arduino instalada.

- Instalar Bibliotecas Necessárias: Instale as bibliotecas necessárias na IDE do Arduino: ESP8266WiFi, Adafruit_MQTT, DHT.

- Configurar o Código: Atualize o código com suas credenciais de Wi-Fi e as informações da sua conta Adafruit IO (nome de usuário e chave AIO).

- Upload para o ESP8266: Conecte o NodeMCU ESP8266 ao seu computador e faça o upload do código utilizando a IDE do Arduino.

- Montar o Hardware: Monte o circuito utilizando o sensor DHT11, protoboard e jumpers conforme descrito.

- Monitorar os Dados: Acesse o painel do Adafruit IO para visualizar os dados de temperatura e umidade em tempo real.


