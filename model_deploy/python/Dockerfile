FROM python:3.8-slim

RUN apt-get update && apt-get install -y && apt-get clean

WORKDIR /app

COPY main.py .env diabetes_model.sav requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

CMD uvicorn main:app --host 0.0.0.0 --port 80 --workers 6