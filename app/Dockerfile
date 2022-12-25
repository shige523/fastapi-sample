FROM python:3.9-alpine3.12
RUN apk --update add \
    curl \
    gcc \
    musl-dev \
    linux-headers \
    build-base \
    libffi-dev \
    bash \
    rust \
    cargo
COPY ./ /app
WORKDIR /app
RUN pip install -r requirements.txt
RUN pip install cryptography
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]
