FROM nginx:latest
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    apt-get clean
RUN pip3 install flask
WORKDIR /app
COPY softy-pinko-front-end /app/softy-pinko-front-end
COPY softy-pinko-front-end/* /var/www/html/softy-pinko-front-end
COPY softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf


CMD ["python3", "/app/api.py"]