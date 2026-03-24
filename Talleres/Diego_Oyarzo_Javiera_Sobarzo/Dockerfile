FROM python:3.12-alpine


RUN pip install --no-cache-dir uv

WORKDIR /app

# 1. Copia específicamente el archivo de requerimientos primero
# Ajusta esta ruta según dónde esté realmente en tu PC
COPY docker_with_problems/src/requirements.txt ./ 

# 2. Instala las dependencias
RUN uv pip install --system -r requirements.txt

# 3. Copia el resto del código
COPY . .

# 4. Comando para ejecutar
CMD ["uv", "run", "python", "docker_with_problems/src/app.py"]