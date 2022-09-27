from pathlib import Path
import shutil


choix=input(str("sur quel chemin iterer ?"))

chemin_path=Path.home()/choix
print(chemin_path)

extension_dict={".mp3": "Musique",
        ".wav": "Musique",
        ".flac":"Musique",
        ".mp4": "Videos",
        ".avi": "Videos",
        ".gif": "Videos",
        ".bmp": "Images",
        ".png": "Images",
        ".jpg": "Images",
        ".jpeg": "Images",
        ".txt": "Documents",
        ".pptx": "Documents",
        ".csv": "Documents",
        ".xls": "Documents",
        ".odp": "Documents",
        ".pages": "Documents",
        ".pdf": "Documents",
        ".exe": "Applications"}

#recupere exclusivement les fichiers dans une liste
files=[f for f in chemin_path.iterdir() if f.is_file()]

#pour chaque fichier dans la liste, crée le dossier associé en fonction de la clé qui est recupéré dans le dictionnaire
for f in files:
# on peut donner à la methode get une valeur par defaut, le deuxieme arguments est la valeur par defaut qui va etre utlisé si on n a pas d'association dans notre dict
    dossier=chemin_path/extension_dict.get(f.suffix,"Autre")
    dossier.mkdir(exist_ok=True)
    shutil.move(f, dossier)
