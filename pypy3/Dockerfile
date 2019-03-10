FROM pypy:3.6-7

LABEL maintainer="Andrij David <david@geek.mg>"

RUN apt update && apt install build-essential gcc

RUN pypy3 -m ensurepip

RUN pip install uvicorn gunicorn

RUN rm -rf /var/lib/apt/lists/*

COPY ./start.sh /start.sh
RUN chmod +x /start.sh

COPY ./gunicorn_conf.py /gunicorn_conf.py

COPY ./start-reload.sh /start-reload.sh
RUN chmod +x /start-reload.sh

COPY ./app /app
WORKDIR /app/

ENV PYTHONPATH=/app

EXPOSE 80

# Run the start script, it will check for an /app/prestart.sh script (e.g. for migrations)
# And then will start Gunicorn with Uvicorn
CMD ["/start.sh"]
