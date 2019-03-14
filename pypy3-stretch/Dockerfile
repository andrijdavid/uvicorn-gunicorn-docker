FROM debian:stretch

LABEL maintainer="Andrij David <david@geek.mg>"

RUN apt-get update && apt-get install -y pypy

COPY ./start.sh /start.sh
RUN chmod +x /start.sh

COPY ./gunicorn_conf.py /gunicorn_conf.py

COPY ./start-reload.sh /start-reload.sh
RUN chmod +x /start-reload.sh

COPY ./app /app
WORKDIR /app/

RUN pypy -m ensurepip

RUN pip install --no-cache-dir uvicorn gunicorn

RUN rm -rf /var/lib/apt/lists/*

ENV PYTHONPATH=/app

EXPOSE 80

# Run the start script, it will check for an /app/prestart.sh script (e.g. for migrations)
# And then will start Gunicorn with Uvicorn
CMD ["/start.sh"]