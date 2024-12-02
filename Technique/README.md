# Technique

## Plantation
### Vue de face
![Vue de face](Technique/Desktop-5.png)

## Synoptique

### Web
Voici un diagrame expliquant les communications entre la plante physique qui sera dans le studio et le site web et la plante virtuelle.

````mermaid
flowchart TD
    subgraph "Installation Physique"
        n1["Plante physique"]
        n3["Diffusion en direct"]
    end
    subgraph "Backend"
        n4["Serveur"]
        n5["Traitement des stats\net interactions"]
    end
    subgraph "Interface Utilisateur"
        n2["Site Web"]
    end
    %% Relations
    n1 ---|"Capture de l'installation et\ninteractions sonores"| n3
    n3 ---|"Stream de la plante et\nson évolution"| n2
    n4 ---|"Statistiques\nd'évolution"| n5
    n5 ---|"Visualisation des stats\nsur le site"| n2
    n4 ---|"Gestion des interactions"| n1
    n2 -->|"Actions utilisateur\n(envoyées au serveur)"| n4
````

## **Technologies utilisées**

### **Matériel :**  
1. **Instrument de musique :**  
   - Synthétiseur
   - Microphone
2. **Télévisions :**  
   - Affichage de la plante 3D en temps réel. 
3. **Haut-parleurs (4 unités) :**  
   - Son immersif et spatialisé.  
4. **Décor recyclé :**  
   - Technologie vintage (moniteurs CRT, câbles usés) et végétation intégrée.
5. **Site Web :**  
   - Diffusion de la plante en temps réel.
   - Possibilité d'envoyer des clips vocals pour aider la plante à se développer.  

### **Logiciels :**  
1. **Touch Designer :**  
2. **Max :**  
   - Génération des sons et leur modulation par le M5Stack Button.  
3. **OSC :**  
   - Communication entre le matériel et le logiciel Unity.  
4. **QLC+ :**  
   - Contrôle des lumières

