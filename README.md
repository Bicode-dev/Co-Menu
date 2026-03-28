# NEY-MENU · v2.2

> Lanceur central de la suite **Koyney** — accédez à NEY-TUBE depuis un seul menu interactif.

```
╔════════════════════════════════════════════════════════════════════════════╗
║  ███╗   ██╗███████╗██╗   ██╗      ███╗   ███╗███████╗███╗   ██╗██╗   ██╗   ║
║  ████╗  ██║██╔════╝╚██╗ ██╔╝      ████╗ ████║██╔════╝████╗  ██║██║   ██║   ║
║  ██╔██╗ ██║█████╗   ╚████╔╝ █████╗██╔████╔██║█████╗  ██╔██╗ ██║██║   ██║   ║
║  ██║╚██╗██║██╔══╝    ╚██╔╝  ╚════╝██║╚██╔╝██║██╔══╝  ██║╚██╗██║██║   ██║   ║
║  ██║ ╚████║███████╗   ██║         ██║ ╚═╝ ██║███████╗██║ ╚████║╚██████╔╝   ║
║  ╚═╝  ╚═══╝╚══════╝   ╚═╝         ╚═╝     ╚═╝╚══════╝╚═╝  ╚═══╝ ╚═════╝    ║
╚════════════════════════════════════════════════════════════════════════════╝
```

[![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Plateforme](https://img.shields.io/badge/Plateforme-Windows%20|%20Linux%20|%20Android-green?style=for-the-badge&logo=windows)](https://github.com/Koyney/Ney-Menu/)
[![Licence](https://img.shields.io/badge/Licence-CC%20BY--NC--ND%204.0-orange?style=for-the-badge)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![Télécharger](https://img.shields.io/badge/Télécharger-Ney--Menu.py-0078D6?style=for-the-badge&logo=python&logoColor=white)](https://raw.githubusercontent.com/Koyney/Ney-Menu/refs/heads/main/Ney-Menu.py)

**Ney-Menu** est le lanceur central des projets Koyney. Il permet d'installer et de lancer les scripts directement depuis un menu interactif. Il est portable et open-source.

---

## Contenu du menu

| Option | Script | Description |
|---|---|---|
| 🔴 YouTube | `Ney-tube.py` | Téléchargeur de vidéos YouTube |
| ⬇️ Mise à jour | — | Met à jour Ney-tube |
| ❌ Quitter | — | Ferme NEY-MENU proprement |


---

## Compatibilité

| Plateforme | Navigation | Chemin d'installation |
|---|---|---|
| Windows | Flèches ↑↓ + Entrée | `%LOCALAPPDATA%\Koyney\Ney-Menu\` |
| Linux / macOS | Flèches ↑↓ + Entrée | `~/.local/share/Koyney/Ney-Menu/` |
| Android (Termux) | Saisie numérique `[1]…[n]` | `~/.local/share/Koyney/Ney-Menu/` |

---

## Prérequis

- **Python 3.8+**
- Aucune dépendance externe — NEY-MENU n'utilise que la bibliothèque standard Python.

---

## Installation

### Windows

```bat
curl -o Ney-Menu.py https://raw.githubusercontent.com/Koyney/Ney-Menu/refs/heads/main/Ney-Menu.py
python Ney-Menu.py
```

### Linux / macOS

```bash
curl -o Ney-Menu.py https://raw.githubusercontent.com/Koyney/Ney-Menu/refs/heads/main/Ney-Menu.py
python3 Ney-Menu.py
```

### Android (Termux)

```bash
pkg install python
curl -o Ney-Menu.py https://raw.githubusercontent.com/Koyney/Ney-Menu/refs/heads/main/Ney-Menu.py
python Ney-Menu.py
```

---

## Utilisation

Lancez simplement le script :

```bash
python Ney-Menu.py      # Windows
python3 Ney-Menu.py     # Linux / macOS / Termux
```

Au démarrage, NEY-MENU effectue automatiquement les opérations suivantes :

1. **Auto-mise à jour** — compare le fichier local avec la version GitHub via hash SHA-256. Si une nouvelle version est détectée, le script se met à jour et se relance tout seul.
2. **Vérification des scripts** — signale les scripts manquants et invite à les installer via le menu *Mise à jour*.
3. **Panneau de statut** — affiche l'état de chaque script directement dans le menu (à jour, mise à jour disponible, absent, etc.).

### Navigation PC (Windows / Linux / macOS)

| Touche | Action |
|---|---|
| `↑` / `↓` | Déplacer le curseur |
| `Entrée` | Valider le choix |
| `Échap` | Quitter |

### Navigation Termux (Android)

Entrez le numéro correspondant à l'option souhaitée, puis validez avec `Entrée`. Tapez `0` pour quitter.

---

## Mise à jour des scripts enfants

Depuis le menu, sélectionnez **⬇️ Mise à jour des scripts** pour télécharger ou mettre à jour Ney-tube.


---

## Structure des fichiers

```
# Windows
%LOCALAPPDATA%\Koyney\Ney-Menu\
├── Ney-tube.py

# Linux / macOS / Termux
~/.local/share/Koyney/Ney-Menu/
├── Ney-tube.py
```

> `Ney-Menu.py` lui-même se lance depuis n'importe quel emplacement — il se met à jour automatiquement au démarrage.

---

## Panneau de statut

Le menu affiche un panneau **ETAT DES SCRIPTS** résumant la situation de chaque script :

| Badge | Signification |
|---|---|
| `✔ A jour` | Le script local correspond à la version GitHub |
| `^ MaJ (+Xo)` | Une mise à jour est disponible |
| `✘ Manquant` | Le script n'est pas encore téléchargé |
| `* Présent` | Le script est présent mais géré manuellement |
| `? Inconnu` | Taille distante non disponible (réseau inaccessible) |

Le statut est mis en cache **5 minutes** pour éviter des requêtes réseau répétées.

---

## Dépôts liés

| Script | Dépôt |
|---|---|
| Ney-Menu | [Koyney/Ney-Menu](https://github.com/Koyney/Ney-Menu) |
| Ney-Tube | [Koyney/Ney-Tube](https://github.com/Koyney/Ney-Tube) |

---

## Licence

Voir le fichier `LICENSE` du dépôt.