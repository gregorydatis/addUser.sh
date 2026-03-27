 - 1 si le nombre d'arguments est égal à 0 alors
    Afficher : "Il manque les noms d'utilisateurs en argument - Fin du script"
    Quitter le script avec le code d'erreur 1
  fin 

   Pour chaque utilisateur dans la liste des arguments faire

 - 2    Vérification existence
    si l'utilisateur existe déjà dans le système ALORS
      Afficher : "L'utilisateur <nom> existe déjà"
      Passer au suivant  →  retour au début de la boucle
    fin

    
    Exécuter la commande de création de l'utilisateur

    
    si la commande s'est terminée sans erreur ALORS
      Afficher : "L'utilisateur <nom> a été créé"
    sinon
      Afficher : "Erreur à la création de l'utilisateur <nom>"
    fin si

    Dans tous les cas, on continue avec le prochain utilisateur

fin 

fin du script
