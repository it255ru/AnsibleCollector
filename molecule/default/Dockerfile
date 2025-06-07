FROM debian:bullseye
ENV container docker
RUN apt-get update && apt-get install -y systemd systemd-sysv && apt-get clean
STOPSIGNAL SIGRTMIN+3
CMD ["/lib/systemd/systemd"]
