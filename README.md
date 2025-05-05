docker build -f task0/Dockerfile -t softy-pinko:task0 task0
Tu dis à Docker :
➡️ « Va chercher un fichier task0/Dockerfile à partir d'ici (alors que tu es déjà dans task0) »
➡️ Donc Docker ne trouve pas le chemin task0.


docker build -t softy-pinko:task0 .

Une fois l'image construite, teste-la avec :

bash
Copier le code
docker run --rm softy-pinko:task0