FROM python:3.12-slim

WORKDIR /task_manager

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY ./main.py .
COPY ./src ./src
COPY ./config.py .
COPY ./main.py .

ENTRYPOINT ["uvicorn", "main:app"]

CMD ["--host", "0.0.0.0", "--port", "8080", "--reload"]
