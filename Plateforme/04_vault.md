# Vault

## 🛡️ Comment gérer les secrets dans une plateforme d’automatisation réseau ? 
 
🔑 Différents types de secrets sont nécessaires pour automatiser un réseau : des couples de nom d’utilisateur et mot de passe, des clés d’API, etc. Ils sont associés à des comptes qui permettre à la plateforme : 

-  D’une part de fonctionner : accès au dépôt de code, à la source d’intention, etc.   
- D’autre part d’exécuter des tâches auprès des équipements à automatiser : accès aux switchs, aux firewalls, etc.

🦸 Ces comptes ont des super pouvoirs : ils peuvent créer, modifier et supprimer toutes les configurations de l’infrastructure réseau. Leur sécurisation est donc un point critique. Il ne faut évidemment pas les exposer, mais il faut également les gérer avec des méthode et rigueur. 

- Pour chaque service ou équipement, il est recommandé d’avoir différents comptes respectant les pratiques de moindre privilège (ex : un compte en lecture seule et un compte en lecture/écriture), et de ségrégation des responsabilités (ex : un compte pour le lab, un compte pour la production). 
- L’expiration et la fréquence de rotation de ces secrets doivent être strictement définies et respectées

🧰 L’utilisation d’un gestionnaire de secrets permet de faciliter ces tâches et de sécuriser ces secrets. Il gère entre autres : 
-  Un stockage centralisé et structuré des secrets 
-  Une gestion fine des droits d’accès aux administrateurs à ces secrets 
-  Un alerting des besoins de rotation voire leur automatisation

🤖 Ces différents secrets peuvent ensuite être mis à disposition et consommés par un orchestrateur d’automatisation (pipelines ou outil dédié) pour permettre à la plateforme : 
-  D’une part de fonctionner : accès au dépôt de code, à la source d’intention, etc. 
-  D’autre part d’exécuter des tâches auprès des équipements à automatiser : accès aux switchs, aux firewalls, etc.

🤓 Cela permet également de mettre à disposition des équipes d’automatisation des secrets avec différents niveaux de droits et d’autorisation sans en partager les détails.

De nombreuses solutions existent sur le marché, open source ou propriétaires : OpenBao, Hashicorp Vault, CyberArk, Azure Key Vault, etc.

🤔 Et vous, utilisez-vous un gestionnaire de secrets pour votre automatisation réseau ? Si oui, lequel ? Avez-vous des bonnes pratiques à partager ?

## Visuel

![Visuel des dangers avec les drifts](img/04_vault.jpg)

---
>**Guillaume MAULE**
