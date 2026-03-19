# Sensor Fusion: Camera-LiDAR Object Detection

## perçu du Projet
Ce projet implémente un algorithme de fusion de capteurs pour la conduite autonome. Il permet de détecter des objets (voitures, piétons) et d'estimer leur distance réelle en mètres en projetant les données d'un scanner laser (LiDAR) sur les images d'une caméra.

## Stack Technique
- **Language :** Python
- **Deep Learning :** YOLOv8 (Ultralytics)
- **Traitement de données :** NumPy, OpenCV
- **Dataset :** KITTI Vision Benchmark

## Pipeline Technique
1. **Détection 2D** : Localisation des objets via YOLOv8.
2. **Transformation de Coordonnées** : Passage du repère LiDAR (3D) au repère Caméra (2D) via des matrices de rotation et translation.

3. **Association de Données** : Filtrage des points LiDAR situés à l'intérieur des boîtes de détection.
4. **Estimation de Profondeur** : Extraction de l'axe Z pour calculer la distance métrique.

## Résultats
- **Identification** : Classification précise des objets.
- **Localisation** : Estimation de la distance avec une erreur minimale.
- **Visualisation** : Projection alignée des points LiDAR colorés selon la distance sur l'image d'origine.
