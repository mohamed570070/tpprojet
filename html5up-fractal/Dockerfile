# Utiliser une image Nginx légère
FROM nginx:alpine

# Copier la configuration personnalisée de Nginx
COPY nginx.conf /etc/nginx/nginx.conf

# Copier les fichiers HTML et les dossiers associés dans le répertoire de Nginx
COPY . /usr/share/nginx/html

# Exposer le port interne (6000)
EXPOSE 6000

# Lancer Nginx
CMD ["nginx", "-g", "daemon off;"]
