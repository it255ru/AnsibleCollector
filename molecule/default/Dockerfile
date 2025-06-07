FROM debian:bullseye

ENV container docker

# Установка systemd и необходимых утилит
RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y \
    systemd systemd-sysv dbus sudo iproute2 python3 python3-pip && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Необходимый сигнал для корректной остановки systemd
STOPSIGNAL SIGRTMIN+3

# Указываем systemd как основной процесс
CMD ["/lib/systemd/systemd"]

