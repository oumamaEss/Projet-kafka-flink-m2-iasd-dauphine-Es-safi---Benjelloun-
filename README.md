# Projet-kafka-flink-m2-iasd-dauphine-Es-safi---Benjelloun-
#Projet détecteur de fraudes de clicks : 

#StreamingJob.java

#5 patterns de détéction de fraude :
 

#-Clicks sans displays per impression id
#-Ctr (nb clicks/nb displays) per impression id >0.2
#-Seuil de clicks per uid-impression id >30
#-Seui de clicks per ip >4
#-ctr per uid >0.1

#-Tous les calclus sont faits dans des windows définis par EventTime(utilisation des timpestamp) et implémentation des Watermarks.
#-Lecture JSON inputs from kafka en utilisant JSONKeyValueDeserializationSchema.
#-Récupération des deux topics en un seul stream.
#-Ecriture en streaming des fraudes dans des fichiers textes enregistrés en local. (un fichier par pattern)
