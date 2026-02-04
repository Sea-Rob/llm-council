FROM python:alpine
WORKDIR /app
COPY uv.lock uv.lock
COPY pyproject.toml pyproject.toml
COPY backend backend
RUN uv sync
CMD uv run python -m backend.main