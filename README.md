# FCSC 2023 Sous marin

Vous êtes invité par un collègue à venir tester son nouveau modèle miniature de sous-marin. Ce modèle est équipé d’une caméra « vue à la première personne » et d’un système adéquat pour diffuser ce flux vidéo.

Pour vous appâter, votre collègue précise que sa carte embarquée est basée sur **un cœur Risc-V**. Vous acceptez donc immédiatement. Le soir venu, vous passez plusieurs minutes à explorer les fonds marins du bassin du campus. Néanmoins, au bout d’une demi-heure, le système de supervision panique et vous perdez la communication. Vous vous jetez dans le bassin pour récupérer le modèle. Votre collègue voit au loin des étudiants partir en courant avec du matériel radio en main. Mais que s’est-il passé ? Est-ce que ces étudiants auraient compromis le système du sous-marin à distance ? Vous proposez d’aider votre collègue à extraire le contenu de sa mémoire Flash et à l’analyser.

Le lendemain, après une douche et une courte nuit de repos, votre collègue dépose la carte électronique du sous-marin sur votre bureau. Il vous confirme qu’il a implémenté un port série en mode 8-N-1, mais il précise qu’il a potentiellement fait **une erreur d’implémentation dans la logique du port série synthétisé**, mais il ne s’en souvient plus trop.

Parce que le sous-marin n’est pas sous l’eau, son électronique n’est pas correctement refroidie. Vous ne pouvez pas le garder allumé plus que quelques minutes avant qu’il ne s’éteigne par sécurité.

Vous prenez un adaptateur port série vers USB pour vous connecter sur le système et vous commencez à investiguer…

**Pour s’interfacer avec le port série à distance, vous aurez besoin de Telnet.**

Votre collègue a réussi à retrouver une sauvegarde du chargeur de démarrage *bootloader.bin* et vous indique que vous pouvez émuler la séquence de démarrage avec la commande *qemu-system-riscv64 -M sifive_u -m 45M -kernel bootloader.bin* (port série disponible dans *View > Serial 0*). Cela vous permet de prototyper des idées avant de risquer d’abîmer le sous-marin.

**Il faut QEMU 5.1 ou ultérieur pour pouvoir émuler ce challenge.**


Fichier:
- [bootloader.bin](bootloader.bin)



Auteur : erdnaxe

Origine : [Sous marin](https://hackropole.fr/fr/challenges/hardware/fcsc2023-hardware-sous-marin/)



-----------

## Connectez vous en WEBSSH
> http://localhost

#### tentez 
> nc sous-marin.cyrhades.fr 4000

-----------

## Ou directement avec netcat
> nc localhost 4000


-----------


## Installation manuel
Vous n'utilisez pas l'application **les CTFs de Cyrhades** ? C'est dommage !
Mais voici comment installer ce CTF manuellement :

> git clone https://github.com/Hack-Oeil/fcsc2023-hardware-sous-marin.git

> cd fcsc2023-hardware-sous-marin


-----------


## Sur le site officiel hackropole.fr
> https://hackropole.fr/fr/challenges/hardware/fcsc2023-hardware-sous-marin/