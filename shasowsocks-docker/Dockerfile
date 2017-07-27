FROM python:2.7

MAINTAINER miki <fullstack.lx@gmail.com>

RUN pip install git+https://github.com/shadowsocks/shadowsocks.git@master 


ENV SS_SERVER_ADDR 0.0.0.0
ENV SS_SERVER_PORT 8388
ENV SS_PASSWORD password
ENV SS_METHOD aes-256-cfb
ENV SS_TIMEOUT 300


ADD start_server.sh /start_server.sh
RUN chmod 755 /start_server.sh


EXPOSE $SS_SERVER_PORT

CMD ["sh", "-c", "/start_server.sh"]
