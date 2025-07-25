FROM python:3.9
EXPOSE 8080
WORKDIR /opt/server
COPY requirements.txt .
COPY *.py .
COPY payment.ini .
ENV CART_HOST=cart
ENV CART_PORT=8080
ENV USER_HOST=user
ENV USER_PORT=8080
ENV AMQP_HOST=rabbitmq
ENV MQP_USER=roboshop
ENV AMQP_PASS=roboshop123
RUN pip3 install -r requirements.txt
CMD ["uwsgi", "--ini", "payment.ini"]