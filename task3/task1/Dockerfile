FROM ubuntu:latest

RUN apt-get update && apt-get upgrade -y

# Installer Python et pip
RUN apt-get install -y python3 python3-pip

# Corriger l'erreur "externally managed" si elle apparaît
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Installer Flask via pip3 (obligatoire)
RUN pip3 install flask

# Créer le dossier /app et y travailler
WORKDIR /app

# Copier le fichier Python dans /app
COPY ./api.py /app/api.py

# Lancer le serveur Flask
CMD ["python3", "api.py"]
