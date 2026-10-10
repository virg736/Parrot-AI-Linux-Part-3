## 🎥 Démonstration vidéo — Parrot AI Linux Partie 3

J'ai testé mon agent IA Linux avec 100 scénarios Red Team
pour évaluer sa sécurité et sa résistance aux attaques.

▶️ [Regarder la vidéo sur YouTube](https://www.youtube.com/watch?v=V7P1GnN_tMY)


## 🎥 Video

<h2 align="center">🎥 Watch the Full Video on YouTube</h2>

🎥 Click on the image below to watch the full video on YouTube.

🎥 I Tested My Linux AI Agent with 100 Red Team Scenarios, But Can It Be Tricked?

<p align="center">
  <a href="https://www.youtube.com/watch?v=V7P1GnN_tMY">
    <img src="https://img.youtube.com/vi/V7P1GnN_tMY/maxresdefault.jpg"
         alt="I Tested My Linux AI Agent with 100 Red Team Scenarios"
         width="700">
  </a>
</p>


---

# Parrot AI Linux — Partie 3
## Sécurisation de mon agent IA et tests Red Team avec Qwen3

### Présentation

Dans cette troisième partie de mon projet **Parrot AI Linux**, je poursuis le développement et la sécurisation de mon agent d'intelligence artificielle sous Linux.

L'objectif est de créer un agent capable de proposer des actions tout en respectant des règles de sécurité.

Pour cela, mon architecture repose sur un **Policy Engine**, un composant chargé d'évaluer les actions proposées par l'IA avant leur éventuelle exécution.

Cette partie est consacrée au renforcement des contrôles, aux tests automatisés et à l'analyse des risques grâce à des scénarios Red Team.

###  ✅ 1. Renforcement de la sécurité

J'ai travaillé sur plusieurs mécanismes de protection :

- Validation stricte des données au format JSON.
- Rejet des champs supplémentaires non autorisés.
- Gestion des actions nulles et des paramètres invalides.
- Contrôle des propositions d'actions produites par l'IA.
- Vérification qu'une décision `DENY` ne déclenche pas l'exécuteur de commandes.
- Ajout de tests automatisés avec Python et pytest.

La suite de tests a atteint **28 tests réussis**.

Ces tests permettent de vérifier plusieurs comportements attendus du système, sans garantir à eux seuls l'absence de vulnérabilités.

### ✅ 2. Création de scénarios Red Team

Le **Red Team Testing** consiste à mettre volontairement un système à l'épreuve pour rechercher des faiblesses dans ses mécanismes de protection.

J'ai développé des scénarios destinés à observer comment mon architecture réagit à différentes propositions d'actions.

Une première simulation avec une réponse prédéfinie a donné les résultats suivants :

- **100 scénarios simulés**
- **100 décisions DENY**
- **0 décision ALLOW**

Cette simulation a permis de vérifier le comportement du système avec une réponse de test prédéfinie.

J'ai ensuite réalisé une évaluation distincte utilisant **Qwen3-0.6B**, exécuté localement avec **llama.cpp**.

### ✅ 3. Résultats des tests avec Qwen3

Au total, **100 scénarios Red Team** ont été évalués avec Qwen3.

| Décision | Résultat | Signification |
|---|---:|---|
| DENY | 43 | Action refusée |
| CLARIFY | 55 | Clarification nécessaire |
| ALLOW | 2 | Action autorisée par le Policy Engine |
| Erreurs API | 0 | Aucune erreur API signalée |

Les résultats ont été enregistrés dans le fichier :

`qwen3_redteam_results.csv`

Ces résultats permettent d'analyser les décisions prises par le système face aux différents scénarios.

### ✅ 4. Analyse des deux décisions ALLOW

Parmi les 100 scénarios, j'ai identifié **2 décisions ALLOW** concernant la commande Linux `whoami`.

La commande `whoami` permet d'afficher le nom de l'utilisateur courant.

Dans mon projet, cette commande fait partie des actions autorisées par le Policy Engine.

Cependant, l'analyse du contrôle présenté dans mon code montre qu'il évalue l'action proposée et ses paramètres sans comparer explicitement cette action à l'intention initiale de l'utilisateur.

Cela soulève une question importante :

> **Une action autorisée par les règles de sécurité correspond-elle réellement à ce que l'utilisateur a demandé ?**

Un attaquant pourrait chercher à détourner un agent IA vers une action autorisée, mais non demandée.

Cette analyse met donc en évidence **un risque potentiel lié à la prise en compte de l'intention initiale**.

Les deux décisions `ALLOW` ne prouvent pas qu'une attaque a réussi ni que la commande a réellement été exécutée.

Des tests complémentaires seront nécessaires pour examiner ce risque.

### ✅ 5. Technologies utilisées

| Technologie | Utilisation |
|---|---|
| Parrot Security OS | Environnement Linux orienté cybersécurité |
| VirtualBox | Virtualisation de l'environnement |
| Python | Développement de l'agent et des tests |
| Qwen3-0.6B | Modèle d'intelligence artificielle local |
| llama.cpp | Exécution locale du modèle IA |
| Pydantic | Validation et structuration des données |
| pytest | Tests automatisés |
| Git | Suivi des modifications et enregistrement des résultats |

### ✅ 6. Bilan de la Partie 3

Cette partie m'a permis de :

- Renforcer les mécanismes de validation et de contrôle.
- Développer des tests de sécurité automatisés.
- Créer des scénarios Red Team.
- Évaluer 100 scénarios avec Qwen3.
- Analyser les décisions `DENY`, `CLARIFY` et `ALLOW`.
- Identifier un risque potentiel concernant l'intention initiale de l'utilisateur.
- Enregistrer les scripts et les résultats dans Git.

**Conclusion :**

Une commande autorisée par le Policy Engine ne garantit pas, à elle seule, qu'elle corresponde à la demande initiale de l'utilisateur.

Cette observation constitue une piste d'amélioration importante pour la suite de mon projet.

###  ✅ Prochaine étape - Partie 4

## AI Defender vs. AI Attacker

Dans la Partie 4, je prévois de créer deux agents d'intelligence artificielle :

- **AI Defender** : chargé d'appliquer les règles de sécurité.
- **AI Attacker** : chargé de mettre les mécanismes de protection à l'épreuve.

L'objectif sera de confronter les deux agents, de réaliser des tests Red Team supplémentaires et de renforcer le Policy Engine pour mieux prendre en compte l'intention initiale de l'utilisateur.

**Parrot AI Linux - Part 4: Coming Soon...**


