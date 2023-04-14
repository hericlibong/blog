---
title: "Scraping_images_via_hidden_API"
date: 2023-03-23T17:16:56Z
draft: true
---


Dans cet exemple, nous créons un dossier appelé 'asos_images' pour stocker les images en dehors du spider. Le chemin complet du dossier est créé en utilisant os.path.join pour joindre le chemin actuel du programme (os.getcwd()) avec le nom du dossier (folder_name). Nous utilisons ensuite os.makedirs pour créer le dossier s'il n'existe pas déjà, avec le paramètre exist_ok=True pour éviter les erreurs si le dossier existe déjà.

Pour stocker chaque image dans ce dossier, nous utilisons à nouveau os.path.join pour créer le chemin complet du fichier (file_path). Nous utilisons ce chemin pour ouvrir le fichier avec open et écrire le contenu de l'image. Nous utilisons également ce chemin pour ouvrir l'image avec Image.open.

Enfin, nous supprimons le fichier d'origine en utilisant os.remove et renvoyons les informations requises via le dictionnaire yield.


`filename = os.path.basename(image_url)`

This line extracts the filename from the image URL using the os.path.basename() method. For example, if the image URL is https://example.com/images/image1.png, this line will set filename to image1.png.

```python

folder_name = 'asos_images'  # Nom du dossier de stockage 
folder_path = os.path.join(os.getcwd(), folder_name)  # Chemin du dossier de stockage
os.makedirs(folder_path, exist_ok=True)  # Créer le dossier s'il n'existe pas


```

These lines define the name and path of the directory where the images will be stored. `os.path.join()` is used to join the current working directory with the folder_name variable to create the full path. The `os.makedirs()` method is then used to create the directory if it does not already exist. The `exist_ok=True` argument is used to avoid raising an error if the directory already exists.


```python

file_path = os.path.join(folder_path, f"{filename}.png")  # Chemin complet du fichier
with open(file_path, 'wb') as f:
    f.write(requests.get(image_url).content)
img = Image.open(file_path)

```
These lines use the full path of the directory created earlier and the filename variable to create the full path to the image file. `The requests.get()` method is used to download the image from the URL and save it to the specified file path using the `open()` method. The file is opened using Image.`open()` method to create an `Image` object that can be used for further processing.
