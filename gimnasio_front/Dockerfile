# =====================
# Etapa 1: Build React
# =====================
FROM node:22-alpine AS build

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build

# =====================
# Etapa 2: Copiar dist al volumen compartido
# =====================
FROM alpine:3.19

# Copiar los archivos compilados al volumen
COPY --from=build /app/dist /usr/share/nginx/html

# Este contenedor solo existe para poblar el volumen
# nginx externo monta ese volumen y sirve los archivos
CMD ["sh", "-c", "echo 'Frontend dist listo en /usr/share/nginx/html' && tail -f /dev/null"]
