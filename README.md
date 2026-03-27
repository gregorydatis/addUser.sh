#!/bin/bash


# Vérif de la présence d'argument

    if [ $# -eq 0 ]; then
    echo "Il manque les noms d'utilisateurs en argument"
    exit 1
fi
# traitemnt de chaque user
    for utilisateur in "$@"; do

# Vérification de lexistence de l'utilisateur dans le système:
    if id "$utilisateur" &>/dev/null; then
        echo "L'utilisateur $utilisateur existe déjà"

    fi
# Création de l'utilisateur:
     useradd "$utilisateur" &>/dev/null
 
 # Vérification du résultat de la création
    if [ $? -eq 0 ]; then
        echo "L'utilisateur $utilisateur a été créé"
    else
        echo "Erreur à la création de l'utilisateur $utilisateur"
    fi
done
