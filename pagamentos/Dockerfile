# Imagem base mínima
FROM alpine:3.19

# Cria diretório de trabalho
WORKDIR /app

# Cria usuário não-root (boa prática de segurança)
RUN addgroup -S appgroup && adduser -S appuser -G appgroup

# Simula aplicação (MVP acadêmico)
RUN echo "Microsserviço em execução" > app.txt

# Ajusta permissões
RUN chown -R appuser:appgroup /app

# Usa usuário não-root
USER appuser

# Comando padrão
CMD ["sh", "-c", "echo 'Serviço iniciado' && tail -f /dev/null"]

