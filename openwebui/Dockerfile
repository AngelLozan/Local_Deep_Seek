FROM python:3.11

RUN apt-get update && apt-get install -y \
    curl \
    ffmpeg \
    && rm -rf /var/lib/apt/lists/*

RUN curl -LsSf https://astral.sh/uv/install.sh | sh
ENV PATH="/root/.local/bin:$PATH"

WORKDIR /app

RUN mkdir /app/env && uv venv /app/env --python=3.11
# RUN uv venv /app/env --python=3.11


ENV DATA_DIR=/root/.open-webui
# ENV DATA_DIR=/app/backend/data
ENV PATH="/app/env/bin:$PATH"

COPY requirements.txt ./

RUN uv pip install -r requirements.txt
RUN uv pip install open-webui


EXPOSE 8080

COPY . .
CMD ["uv", "run", "open-webui", "serve"] 


