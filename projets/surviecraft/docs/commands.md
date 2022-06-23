---
order: 100
label: Commandes
icon: list-unordered
---

# Liste des commandes

SurvieCraft Bot embarque de nombreuses commandes ; la plupart d'entre elles sont des commandes slash [!badge variant="primary" text="SLASH"], mais il existe aussi des commandes apparaissant dans les menus contextuels utilisateur [!badge variant="secondary" text="USER"].

Vous pouvez aussi retrouver des commandes avec un préfix [!badge variant="success" text="PREFIX"] mais cette fonctionnalité est vouée à disparaître d'après Discord.

!!!
Ces tag représente les permissions nécessaires pour pouvoir utiliser la commande:

[!badge variant="secondary" text="@everyone"] [!badge variant="danger" text="@| Star SurvieCraft"] [!badge variant="primary" text="@| Guide"] [!badge variant="warning" text="@| Modérateur"] [!badge variant="danger" text="@| SuperModo"] [!badge variant="success" text="@| Développeur"] [!badge variant="primary" text="@| Responsable"] [!badge variant="danger" text="@| Administrateur"]
!!!

## Administration

### `suggestion` [!badge variant="primary" text="SLASH"] [!badge variant="success" text="PREFIX"]

Accepter ou refuser une suggestion

```
/suggestion [message-id] [nouveau-statut] (raison)
```

> Nouveau statut disponible: `ACCEPTED`, `DENIED` et `WAITING`

[!badge variant="success" text="@| Développeur"] [!badge variant="primary" text="@| Responsable"] [!badge variant="danger" text="@| Administrateur"]

---

### `tagedit` [!badge variant="primary" text="SLASH"] [!badge variant="success" text="PREFIX"]

Gérer les messages automatiques du serveur

```Créer un nouveau tag
/tagedit [create] [nom du nouveau tag] (réponse du tag)
```

```Supprimer un tag
/tagedit [delete] [nom du tag]
```

```Ajouter un nouveau keyword à un tag
/tagedit [keyword] [nom du nouveau tag] (nouveau keyword)
```

[!badge variant="success" text="@| Développeur"] [!badge variant="primary" text="@| Responsable"] [!badge variant="danger" text="@| Administrateur"]

---

## Modération

!!!warning Permissions nécessaires
Par défaut, des permissions sont demandées pour les commandes de cette catégorie, et diffèrent suivant la commande. Consultez la page [Modération](/projets/surviecraft/docs/moderation.md) pour en savoir plus.
!!!

### `clearchat` [!badge variant="primary" text="SLASH"] [!badge variant="success" text="PREFIX"]

Supprimer des messages (de moins de 15 jours) en masse dans le salon où est effectuée la commande.

!!!danger
Si le nombre de messages indiqués est strictement supérieur au nombre de messages effectivement envoyés dans le salon, un comportement inattendu peut se produire : des messages envoyés ultérieurement à la commande pourraient être supprimés. Soyez donc attentif au nombre indiqué.
!!!

```
/clearchat [nombre de messages entre 1 et 99]
```

[!badge variant="primary" text="@| Guide"] [!badge variant="warning" text="@| Modérateur"] [!badge variant="danger" text="@| SuperModo"] [!badge variant="success" text="@| Développeur"] [!badge variant="primary" text="@| Responsable"] [!badge variant="danger" text="@| Administrateur"]

---

### `ticket` [!badge variant="primary" text="SLASH"]

Gérer les membres d'un ticket.

```Ajout d'un membre
/ticket [add] [membre]
```

```Retrait d'un membre
/ticket [remove] [membre]
```

[!badge variant="primary" text="@| Guide"] [!badge variant="warning" text="@| Modérateur"] [!badge variant="danger" text="@| SuperModo"] [!badge variant="success" text="@| Développeur"] [!badge variant="primary" text="@| Responsable"] [!badge variant="danger" text="@| Administrateur"]

---

### `warn` [!badge variant="primary" text="SLASH"]

Gérer les avertissements d'un membre

```Ajout d'un avertissement
/warn [add] [membre] [raison]
```

```Retrait d'un avertissement
/warn [remove] [membre] [id de l'avertissement]
```

```Liste des avertissements
/warn [list] [membre]
```

[!badge variant="primary" text="@| Guide"] [!badge variant="warning" text="@| Modérateur"] [!badge variant="danger" text="@| SuperModo"] [!badge variant="success" text="@| Développeur"] [!badge variant="primary" text="@| Responsable"] [!badge variant="danger" text="@| Administrateur"]

---

## Premium

### `rolecolor` [!badge variant="primary" text="SLASH"] [!badge variant="success" text="PREFIX"]

Permet aux Nitro Boosters de changer la [couleur de leur rôle](https://www.google.com/search?q=color+picker)

```
/rolecolor [hex-color]
```

[!badge variant="danger" text="@| Star SurvieCraft"]

---

## Testing

### `ping` [!badge variant="primary" text="SLASH"] [!badge variant="success" text="PREFIX"]

Test rapidement une réponse du bot.

```
/ping
```

!!!secondary
Cooldown: `10s`
!!!

[!badge variant="secondary" text="@everyone"]

---

### `simjoin` [!badge variant="primary" text="SLASH"] [!badge variant="success" text="PREFIX"]

Simule une arrivée sur le serveur Discord.

```
/simjoin
```

[!badge variant="success" text="@| Développeur"] [!badge variant="primary" text="@| Responsable"] [!badge variant="danger" text="@| Administrateur"]

---

### `simleave` [!badge variant="primary" text="SLASH"] [!badge variant="success" text="PREFIX"]

Simule une sortie sur le serveur Discord.

```
/simleave
```

[!badge variant="success" text="@| Développeur"] [!badge variant="primary" text="@| Responsable"] [!badge variant="danger" text="@| Administrateur"]

---

## Utilitaire

### `ask` [!badge variant="primary" text="SLASH"] [!badge variant="success" text="PREFIX"]

Lien vers comment poser une question.

```
/ask
```

!!!secondary
Cooldown: `10s`
!!!

[!badge variant="secondary" text="@everyone"]

---

### `dnw` [!badge variant="primary" text="SLASH"] [!badge variant="success" text="PREFIX"]

Explique comment poser correctement une question.

```
/dnw
```

!!!secondary
Cooldown: `10s`
!!!

[!badge variant="secondary" text="@everyone"]

---

### `space` [!badge variant="primary" text="SLASH"] [!badge variant="success" text="PREFIX"]

La commande space renvoie une barre de separation de salon.

```
/space
```

!!!secondary
Cooldown: `15s`
!!!

[!badge variant="primary" text="@| Guide"] [!badge variant="warning" text="@| Modérateur"] [!badge variant="danger" text="@| SuperModo"] [!badge variant="success" text="@| Développeur"] [!badge variant="primary" text="@| Responsable"] [!badge variant="danger" text="@| Administrateur"]

---

### `tag` [!badge variant="primary" text="SLASH"] [!badge variant="success" text="PREFIX"]

Renvoie le message automatique associé à ce tag.

```
/tag [nom du tag]
```

!!!secondary
Cooldown: `10s`
!!!

[!badge variant="secondary" text="@everyone"]

---

### `taginfo` [!badge variant="primary" text="SLASH"] [!badge variant="success" text="PREFIX"]

Renvoie des informations sur un tag spécifique.

```
/taginfo [nom du tag]
```

!!!secondary
Cooldown: `10s`
!!!

[!badge variant="secondary" text="@everyone"]

---

### `taglist` [!badge variant="primary" text="SLASH"] [!badge variant="success" text="PREFIX"]

Renvoie une liste des tags existantes.

```
/taglist
```

!!!secondary
Cooldown: `10s`
!!!

[!badge variant="secondary" text="@everyone"]
