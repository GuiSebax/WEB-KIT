# Etapa 1: construir a aplicação React
# OBS: Se for React + vite é (/app/dist), se for React + CRA é (/app/build)
FROM node:18 AS build
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build

# Etapa 2: Servir com NGINX
FROM nginx:alpine
COPY --from-build /app/build /usr/share/nginx/html

# Copia a configuração default do nginx
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
