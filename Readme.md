
# L'objectif du projet

    - Ce project consiste à écrire un Encodeur et Décodeur RLE s'appliquant à une image
        binaire mais aussi en niveau de gris.

# Prérequis

    - Tout d'abord il faut installer les librairies suivante :
        - import cv2 
        - import matplotlib.pyplot as plt
        - import numpy as np
        - import qrcode
        - from pyzbar import pyzbar
        - import os
        - from natsort import natsorted 

# Comment ça fonctionne

    - Pour Encoder/Decoder une image nous retrouvons respectivement les fonctions : 
        - RLE_Encode(chaine_a_coder,nombre_de_repetition,nombre_de_bits)
        - RLE_Decode(chaine_a_decoder,largeur,hauteur)

    - Pour decoder la chaine Encoder du QRCode nous retrouvons la fonction :
        - QR_Decode()

    - Pour avoir un exemple d'execution nous avons la fonction :
        - MainImage()

# Note pour la fonction RLE_Encode()

    - Cette fonction en plus de compresser une image, elle sauvegarder la chaine obtenue dans un QRCode
    - Lorseque l'image est trop grande pour le QRCode les étapes suivantes sont effectuées : 
       
        - Division de la chaine en sous chaine de moins de 2000 caractères
        - Création de N QRCode tel que N est le nombre de division de la chaine précédente.
        - Les QRCodes sont numérotés pour effectuer la décompression dans le bon ordre a l'appel de QR_Decode()


