FROM python:alpine
WORKDIR /app
RUN apk add --no-cache uv 
RUN pip install uvicorn
COPY uv.lock uv.lock
COPY pyproject.toml pyproject.toml
COPY backend backend
RUN uv sync
CMD uv run python -m backend.main