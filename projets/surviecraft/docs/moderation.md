---
order: 99
label: Modération
icon: law
---

# Modération

## Avertissements (`warn`)

SurvieCraft Bot vous permet d'avertir les membres de votre serveur.

!!!warning
Les commandes suivantes nécessitent d'avoir un des roles suivant: [!badge variant="primary" text="@| Guide"] [!badge variant="warning
" text="@| Modérateur"] [!badge variant="danger" text="@| SuperModo"] [!badge variant="success" text="@| Développeur"] [!badge variant="primary" text="@| Responsable"] [!badge variant="danger" text="@| Administrateur"].
!!!

### Ajouter un avertissement

```
/warn add [@membre] [raison]
```

Ceci enregistre un avertissement dans la base de données, envoie un message privé au membre concerné si cela est possible, et envoie un log dans le salon paramétré pour les logs de modération, s'il existe.

### Retirer un avertissement

```
/warn remove [@membre] [numéro]
```

Ceci retire l'avertissement mentionné de la base de données et envoie un log dans le salon paramétré pour les logs de modération, s'il existe. Le numéro de l'avertissement est celui qui s'affiche dans la liste des avertissements.

### Lister les avertissements d'un membre

```
/warn list [@membre]
```

Ceci liste les avertissements du membre mentionné.

## Nettoyage d'un salon

```
/clearchat [n]
```

Ceci supprime les $n$ derniers messages (de moins de 15 jours) en masse dans le salon où est effectuée la commande. Attentions, cette commande à une limite de 100 messages à la fois.

!!!danger
Si le nombre de messages indiqués est strictement supérieur au nombre de messages effectivement envoyés dans le salon, un comportement inattendu peut se produire : des messages envoyés ultérieurement à la commande pourraient être supprimés. Soyez donc attentif au nombre $n$ indiqué.
!!!
