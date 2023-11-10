---
description: via le code CSS
---

# 📑 Personnalisation de la mise en page du tableau de bord

Tous les blocs du tableau de bord peuvent être modifiés pour être personnalisé. Par exemple, il est possible de mettre tous les graphiques "Gros nombres" avec un arrière plan d'une autre couleur. Ou bien de changer la police de la page.. ect

Voici la marche à suivre :&#x20;

1. Éditer le tableau de bord, puis cliquer sur les "..." et modifier le CSS

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption><p>Edition puis ... et modifier le CSS</p></figcaption></figure>

2. Ajouter une syntaxe dans l'éditeur CSS

Par exemple, je veux modifier la couleur du bloc filtre à gauche de mon tableau de bord :&#x20;

Je vais copier coller ce code dans la fenêtre :&#x20;

```
/* changing the filters bar background */
  div[data-test=filter-bar] > div {
    background: #ececfe;
```

Pour trouver le code à appliquer selon ce qu'on veut faire, cliquer sur ce lien :&#x20;

{% embed url="https://preset.io/blog/customizing-superset-dashboards-with-css/#general-backgrounds-fonts-and-colors" %}

Pour le tableau de bord du MOS, voici le code appliqué :



<pre><code>  /* changer tous les graphiques big number avec un fond 
  d'une couleur et ajuster la taille */
  
<strong>div[data-test-viz-type=big_number_total] {
</strong>  background: #ececfe;
  border-radius: 30px;
  padding: 5px;
}
  /* changer le fond du bloc filtre */
  div[data-test=filter-bar] > div {
    background: #ececfe;
  }
div[data-test-viz-type=big_number_total] > div:first-child {
    display: none;
  
      /* changer le fond du tableau de bord en blanc */
}
.dashboard-content{
      background-color:white;
  }
  }
</code></pre>

**Ce qui donne ce résultat :**&#x20;

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption><p>tableau de bord MOS</p></figcaption></figure>
