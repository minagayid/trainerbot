FROM python:3.12-slim
WORKDIR /app
COPY pyproject.toml .
RUN pip install -U pip \
 && pip install fastapi uvicorn pydantic
COPY app ./app
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
