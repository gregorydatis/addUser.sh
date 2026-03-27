#!/bin/bash


# Vérif de la présence d'argument

if [ $# -eq 0 ]; then
    echo "Il manque les noms d'utilisateurs en argument"
    exit 1
fi
