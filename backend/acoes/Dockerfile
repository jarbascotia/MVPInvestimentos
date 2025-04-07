FROM python:3.9-slim

# Configuração do diretório de trabalho
WORKDIR /app

# Copiar arquivos e instalar dependências
COPY . .
RUN pip install --no-cache-dir -r requirements.txt && \
    rm -rf /root/.cache/pip

# Criar diretório para o banco de dados
RUN mkdir -p /app/db

# Expor a porta 3003
EXPOSE 3003

# Comando para rodar o servidor Flask
CMD ["python", "app.py"]
