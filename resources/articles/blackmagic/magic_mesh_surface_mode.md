En fonctionnement standard, Cura crée des coupes transversales de tous les triangles de votre maillage. 
Ces segments sont réunis ensemble pour former des boucles. 
Toutes les boucles qui ne sont pas fermées seront supprimées.

Ce paramètre contrôle ce qui sera fait avec ces boucles non fermées. 
Défini sur "Normal", les boucles sont supprimés. 
Défini sur "Surface", toutes les coupes transversales sont imprimées sous forme de contours. 
Définie sur "Les deux", les contours fermés sont imprimés normalement mais ceux non fermés sont imprimés séparément en tant que murs supplémentaires.

![Le mode normal laisse de côté la seule surface non fermée sur la droite](../images/magic_mesh_surface_mode_normal.png)
![Le mode Surface imprime uniquement les surfaces sans les traiter comme des volumes fermés](../images/magic_mesh_surface_mode_surface.png)
!["Les deux" imprime des volumes et de la surface supplémentaire non fermés sur la droite](../images/magic_mesh_surface_mode_both.png)

Les surfaces supplémentaires imprimées incluront uniquement les surfaces verticales sous forme de lignes simples. Il n'y a pas de technique de remplissage pour les surfaces horizontales, car les surfaces ne sont pas des polygones fermés. Ils ne peuvent pas être remplis car il n'y a pas à l'intérieur. Il ne peut y avoir ni dessus, ni dessous, ni remplissage, ni support. Seulement des lignes simples.

Les surfaces supplémentaires seront imprimées comme s'il s'agissait de murs extérieurs, elles seront donc affectées par la vitesse d'impression du mur extérieur, la largeur de ligne, etc.

*Si vous imprimez à la fois les volumes normaux et les surfaces supplémentaires, gardez à l'esprit que les volumes seront imprimés avec la paroi extérieure complètement à l'intérieur du volume. Les surfaces supplémentaires sont imprimées avec la ligne centrée sur la surface, avec la moitié de la largeur de la ligne de chaque côté. Si une surface supplémentaire est alignée sur la surface d'un volume fermé, comme dans les images ci-dessus, la surface sera décalée d'une demi-largeur de ligne. Après tout, la surface supplémentaire n'a aucun intérieur vers lequel se diriger. *
