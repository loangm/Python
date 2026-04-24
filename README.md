# Wavit

Programme de reconnaissance musicale de vinyles développée en Python. Identifie automatiquement des morceaux audio via ACRCloud, enrichit les métadonnées via YouTube et Discogs, et stocke les résultats dans une base de données locale SQLite.

-----

## 🎵 Fonctionnalités

- 🎙️ **Reconnaissance audio** — Identification de pistes via ACRCloud
- 📻 **Empreinte audio** — Analyse MFCC, spectrogram, chroma, tempo (librosa)
- 🎞️ **Recherche YouTube** — Récupération de pistes par genre musical
- 💿 **Enrichissement Discogs** — Métadonnées : album, label, année, ISRC
- 🗄️ **Base de données SQLite** — Stockage local des pistes identifiées
- 📊 **Statistiques** — Répartition des pistes par genre

-----

## 🎯 Genres ciblés

Minimal · Jungle · Drum and Bass · Breakbeat · IDM · Techno · House · Dubstep

-----

## 🛠️ Stack technique

|Technologie        |Rôle                               |
|-------------------|-----------------------------------|
|Python             |Langage principal                  |
|librosa            |Analyse audio (MFCC, chroma, tempo)|
|ACRCloud SDK       |Reconnaissance musicale            |
|YouTube Data API v3|Recherche de pistes                |
|Discogs API        |Métadonnées musicales              |
|pydub              |Traitement audio                   |
|scipy              |Spectrogram                        |
|SQLite             |Base de données locale             |
|youtube-dl         |Téléchargement audio               |

-----

## 📥 Installation

### Prérequis

- Python 3.8+
- ffmpeg installé sur le système

### Installer les dépendances

```bash
pip install librosa pydub scipy numpy requests google-api-python-client discogs-client youtube-dl
pip install git+https://github.com/acrcloud/acrcloud_sdk_python
```

### Configurer les clés API

Dans le fichier principal, renseigne tes clés :

```python
YOUTUBE_API_KEY = "ta_cle_youtube"
DISCOGS_TOKEN = "ton_token_discogs"
ACRCLOUD_ACCESS_KEY = "ta_cle_acrcloud"
ACRCLOUD_ACCESS_SECRET = "ton_secret_acrcloud"
ACRCLOUD_HOST = "identify-eu-west-1.acrcloud.com"
```

-----

## 🚀 Lancement

```bash
python main.py
```

-----

## 📋 Menu principal

```
1. Rechercher et ajouter des pistes (Minimal, Jungle, etc.)
2. Identifier une piste audio
3. Afficher les statistiques de la base de données
4. Lister les pistes stockées
5. Quitter
```

-----

## 🏗️ Structure du projet

```
Python/
├── main.py                        # Point d'entrée
├── electronic_music_database.db   # Base de données SQLite (générée)
└── youtube_audio/                 # Fichiers audio téléchargés (générés)
```

-----

© 2024 Wavit by Entreprod
