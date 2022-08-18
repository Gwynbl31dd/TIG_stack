FROM telegraf:latest

USER root

RUN apt-get update && apt-get -y install build-essential hddtemp

ADD telegraf.conf.template /telegraf.conf.template
ADD telegraf.conf.template /etc/telegraf/telegraf.conf
COPY *.conf /etc/telegraf/telegraf.d/

ADD run.sh /run.sh

RUN chmod +x /*.sh

CMD ["/run.sh"]