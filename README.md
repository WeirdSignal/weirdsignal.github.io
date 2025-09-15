# Blog

## Article

### WIP (3 tasks max)
  - Faire un article avec image pour montrer la configuration d'un noeud Gaulix depuis l'application Android (Un client par example) on fera un mobile plus tard avec tableau récapitulatif)
  - Comment apparaitre rapidement sur une carte en tracker
  - Rager les articles par tags ou categories

### Régles générales
  - Rendre attractifs les articles -> Des images, des plantuml et des animations
    - Trier par tagjekyll : meshtastic / gaulix / procedure / oducmentaiton / technique 
  - Un joli theme
  - Une page pour selctionner des tags ou des categories
  - Analytics
  - SEO

### BackLog

- Article PIXEL Server : 
  - Pourquoi les traits sont verts / Comment appariatre sur une carte
   - Pixel Server amélioration 
      - Améliorer les affichagesur la carte avec des icones a parit du usermask, ovir les 2 dernières heures de deplacement d'un node
      - Icone a partir du user mask pour les noeuds / fixe mobile etc (ou a partir du nom long)
      - Afficher les 2 dernières heures des positions d'un tracker par exemple
    -  Gaulix apparaitre sur la carte pixel :
      -   Il faut que les 2 nœuds informent le site qu'ils sont voisins :
      - via des trames neighborinfo envoyé des 2 côté
      - via des traceroutes
      - en relayant la trame de l'autre sur mqtt avec un hop à 0
      - avec le "relay node" présent dans les trames
      - Les 2 nœuds doivent avoir une position gps et s'entendre une fois par jour au moins.      
        Sur le site Gaulix c'est pareil sauf que c'est restreint au mqtt Gaulix donc tu as moins de chance d'avoir de traits verts si tu n'es pas sur leur mqtt.
        En Isère (et globalement en France) c'est la carte pixel qu'il faut regarder car elle regroupe la plupart des mqtt français
 
- Article Gaulix :
  - Swot Gaulix
    - Trop de canaux, a diminuer, virer admin, ajouter des canaux locaux
    - Communauté Francaise, diffile de passer dans les payx limitrophes
    - Ajouter un canal ping comme la PACA  
    - Gaulix amélioration (liste smartphone)
    -   Des icones sympas, le temp sur le reseau
    -   Un statut des stations
    -   Animer le reseau 
    - Sur quel canal communiquer :
      - LongMod : pour discuter localement et pour vos tests
      - Fr_Blabla : pour discuter avec Gaulix du côté du 69, 26, 42, 43, 07. Vos messages arriveront sur leur MQTT et passeront donc dans toute la France via internet.   - Les réponses de ceux qui essaieront de vous répondre via internet n'arriveront pas jusqu'à nous car on est en 100% radio
    - France : la communauté francophone sur Facebook l'utilise, c'est au cas où
    - Fr_EMCOM : utiliser pour les situations d'urgence, norme gaulix 
    - Fr_Balise : pas utilisé, toutes les informations qui ne sont pas des messages transitent de manière invisible sur ce canal

- Article : Animer votre réseau meshtastic :
  -   Ce qu iexiste le test emcomm le premier mercredi du mois
  -   Ajouter des infos sur la carte
  -   
- Articles CAS Concrets 
  - Cas concret la coupure SFR plus de reseau mobile => Ajouter dans le susages de meshtastics 
  - Cas concret mes enfants se servent d'un clavier

  - Articles Hardware :
    - https://www.google.com/search?client=firefox-b-d&q=armachat+tracksenger

