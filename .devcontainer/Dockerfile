FROM mcr.microsoft.com/devcontainers/base:jammy

USER root 
RUN curl -fsSL https://raw.githubusercontent.com/arduino/arduino-cli/master/install.sh | BINDIR=/usr/local/bin sh

USER vscode
ENV PATH="$PATH:/opt/arduino/bin"
RUN arduino-cli config init && arduino-cli config add board_manager.additional_urls  https://arduino.esp8266.com/stable/package_esp8266com_index.json && arduino-cli core update-index && arduino-cli core install esp8266:esp8266 && arduino-cli lib install ArduinoJson