FROM python:3.11-slim
WORKDIR /app
COPY app.py .
RUN pip install flask
RUN apt-get update && apt-get install -y curl
EXPOSE 8002
CMD ["python", "app.py"]