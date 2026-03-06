FROM python:3.13.11

COPY --from=ghcr.io/astral-sh/uv:latest /uv /bin/

WORKDIR /code

ENV PATH="/app/.venv/bin:$PATH"

COPY pyproject.toml .python-version uv.lock

COPY pipeline.py .

ENTRYPOINT ["uv", "run", "python", "pipeline.py"]