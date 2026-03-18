FROM python:3.12-slim
RUN pip install uv
WORKDIR /app
COPY pyproject.toml ./
RUN uv pip install --system -r pyproject.toml
COPY . .
EXPOSE 3000
CMD ["run", "python", "encriptador.py", "desencriptador.py"]