FROM rabbitmq 

ENV RABBITMQ_DEFAULT_USER =roboshop \
    RABBITMQ_DEFAULT_PASS = roboshop123

RUN rabbitmq-plugins enable --offline rabbitmq_mqtt rabbitmq_federation_management rabbitmq_stomp