FROM python:3.8.13-slim-bullseye

COPY app/app_binary.pex /app_binary.pex
ENV PEX_SCRIPT=uvicorn
CMD ["/app_binary.pex", "app.main:app", "--host", "0.0.0.0", "--port", "80"]
