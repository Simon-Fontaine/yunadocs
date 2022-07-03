---
order: 99
label: Modération
icon: law
---

# Modération

!!!warning
Les commandes suivantes nécessitent d'avoir un des roles suivant: [!badge variant="primary" text="@| Guide"] [!badge variant="warning
" text="@| Modérateur"] [!badge variant="danger" text="@| SuperModo"] [!badge variant="success" text="@| Développeur"] [!badge variant="primary" text="@| Responsable"] [!badge variant="danger" text="@| Administrateur"].
!!!

## Avertissements (`warn`)

SurvieCraft Bot vous permet d'avertir les membres de votre serveur.

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

## Exclusion temporaire d'un membre (`mute`)

Pour sanctionner un membre en l'empêchant temporairement de participer aux conversations de votre serveur sans l'expulser ni le bannir, vous pouvez l'exclure temporairement.

!!!
Autrefois, le `mute` était effectué à l'aide d'un rôle avec des permissions qui n'étaient pas toujours bien réglées. Aujourd’hui, nous utilisons le système intégré de Discord qui fait bien mieux les choses.
!!!

### Exclure temporairement un membre

```
/mute [@membre || identifiant] [durée: s/m/h/d => seconde/minute/heure/jour] [raison]
```

Ceci envoie un message privé au membre concerné si cela est possible, exclu temporairement le membre pour la durée indiquée et envoie un log dans le salon paramétré pour les logs de modération, s'il existe.

### Mettre fin à l'exclusion temporaire d'un membre

```
/unmute [@membre || identifiant] [raison]
```

Ceci envoie un message privé au membre concerné si cela est possible, met fin à l'exclusion temporaire du membre et envoie un log dans le salon paramétré pour les logs de modération, s'il existe.

## Expulsion d'un membre (`kick`)

!!!warning
La commande suivante nécessite la permission Expulser des membres.
!!!

```
/kick [@membre || identifiant] [raison]
```

Ceci envoie un message privé au membre concerné si cela est possible, l'expulse du serveur, et envoie un log dans le salon paramétré pour les logs de modération, s'il existe.

## Bannissement d'un membre (`ban`)

!!!warning
La commande suivante nécessite la permission Bannir des membres.
!!!

```
/ban [@membre || identifiant] [raison]
```

Ceci envoie un message privé au membre concerné si cela est possible, le bannit du serveur, et envoie un log dans le salon paramétré pour les logs de modération, s'il existe.

## Gestion des Tickets joueur

SurvieCraft Bot vous permet d'effectuer plusieurs actions rapide, en une seule commande, pour facilement modérer vos tickets joueur.

### Ajouter un member au ticket

```
/ticket [add] [@membre]
```

Ceci ajoute un nouveau membre au ticket. Celui ci pourra voir le salon du ticket, lire l'historique des messages et parler dans le salon.

### Retirer un member au ticket

```
/ticket [remove] [@membre]
```

Ceci retire un nouveau membre au ticket. Celui ci ne pourra plus voir le salon du ticket, lire l'historique des messages et parler dans le salon.

### Fermer un ticket

```
/ticket [close]
```

Ceci ferme le ticket en vous proposant d'indiquer une raison, envoie un message dans le salon archive joueur avec toutes les informations concernant le ticket, envoie un message privé au membre qui a créé le ticket contenant toutes les informations concernant le ticket et supprime le salon du ticket.

### Boutons Ticket

--![Voici la liste des boutons actuellement disponible pour gérer vos tickets](/static/images/boutons-ticket.PNG "Boutons Ticket")--

#### 1) 💾 Sauvegarder & Fermer

Ce bouton ferme le ticket en vous proposant d'indiquer une raison.

1. Il envoie un message dans le salon archive joueur avec toutes les informations concernant le ticket
2. Il envoie un message privé au membre qui a créé le ticket contenant toutes les informations concernant le ticket
3. Il supprime le salon du ticket

#### 2) 🔒 Lock

Ce bouton retire la permission aux membres du ticket de parler dans celui-ci

#### 3) 🔓 Unlock

Ce bouton redonne la permission aux membres du ticket de parler dans celui-ci

#### 4) 🙋‍♂️ Claim

Ce bouton envoie un message dans le ticket indiquant quel membre du staff est chargé de ce ticket

## Gestion des Tickets staff

SurvieCraft Bot vous permet d'effectuer plusieurs actions rapide, en une seule commande, pour facilement modérer vos tickets staff.

!!!warning
Les commandes suivantes nécessitent d'avoir un des roles suivant: [!badge variant="primary" text="@| Responsable"] [!badge variant="danger" text="@| Administrateur"].
!!!

### Ajouter un member au ticket

```
/staffticket [add] [@membre]
```

Ceci ajoute un nouveau membre au ticket. Celui ci pourra voir le salon du ticket, lire l'historique des messages et parler dans le salon.

### Retirer un member au ticket

```
/staffticket [remove] [@membre]
```

Ceci retire un nouveau membre au ticket. Celui ci ne pourra plus voir le salon du ticket, lire l'historique des messages et parler dans le salon.

### Fermer un ticket

```
/staffticket [close]
```

Ceci ferme le ticket en vous proposant d'indiquer une raison, envoie un message dans le salon archive staff avec toutes les informations concernant le ticket, envoie un message privé au membre qui a créé le ticket contenant toutes les informations concernant le ticket et supprime le salon du ticket.

### Boutons Ticket

--![Voici la liste des boutons actuellement disponible pour gérer vos tickets](/static/images/boutons-ticket.PNG "Boutons Ticket")--

#### 1) 💾 Sauvegarder & Fermer

Ce bouton ferme le ticket en vous proposant d'indiquer une raison.

1. Il envoie un message dans le salon archive staff avec toutes les informations concernant le ticket
2. Il envoie un message privé au membre qui a créé le ticket contenant toutes les informations concernant le ticket
3. Il supprime le salon du ticket

#### 2) 🔒 Lock

Ce bouton retire la permission aux membres du ticket de parler dans celui-ci

#### 3) 🔓 Unlock

Ce bouton redonne la permission aux membres du ticket de parler dans celui-ci

#### 4) 🙋‍♂️ Claim

Ce bouton envoie un message dans le ticket indiquant quel membre du staff est chargé de ce ticket

## Nettoyage d'un salon

```
/clearchat [n]
```

Ceci supprime les $n$ derniers messages (de moins de 15 jours) en masse dans le salon où est effectuée la commande. Attentions, cette commande à une limite de 100 messages à la fois.

!!!danger
Si le nombre de messages indiqués est strictement supérieur au nombre de messages effectivement envoyés dans le salon, un comportement inattendu peut se produire : des messages envoyés ultérieurement à la commande pourraient être supprimés. Soyez donc attentif au nombre $n$ indiqué.
!!!
