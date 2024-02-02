# Document markdown
## Définir le problème

Le problème est que le centre CNMH manque un système efficace de gestion des données, ce qui entraîne des difficultés dans la génération de rapports précis et complets. Chaque département du centre utilise des méthodes traditionnelles de tenue de registres sur papier et à la plume, et seuls quelques-uns utilisent des feuilles de calcul Excel. Cela rend difficile et chronophage pour la directrice de rassembler les données dont elle a besoin périodiquement. Par conséquent, les rapports générés peuvent ne pas refléter avec précision le travail effectué par le centre et ne pas mettre en valeur leurs réalisations.

Le centre CNMH manque d'un système efficace de gestion des données, ce qui entraîne des difficultés dans la génération de rapports précis et complets.


## Idéation
Créer une application conviviale pour le centre CNMH en utilisant Laravel, Bootstrap et AdminLTE. Cette application permettra une gestion plus efficace des données et une génération améliorée de rapports, avec une interface facile à utiliser pour les employés.


## Empathie avec service social
![service social Carte d'empathie](images/service-social.png)

### Persona
Khawla souan

### Ce qu'il dit 
- a  l’accueil ( réception au visiteur de centre - repondre a leurs questions)
- après entretien social ils l'enregistrent ou pas  selon leur condition (est ce qu'ils ont une handicapé ou pas) création de dossier social(tout les informations du patient avec N°A…) 
- remplir bon d’orientation(date inscription,Dossier social N°A…,Nom et Prénom du bénéficiaire)
- Gestion des rendez-vous
- dossier ça reste en liste d’attente enregistrement
- dossier va passer à l'infirmière

### Faire
- Affiche les information en table exel :
  - N dossier
  - Nom
  - Prénom
  - Sexe
  - TH
  - Date naissance
  - Age
  - Couverture médicale
  - cnops
  - cnss
  - ramed
  - assurance
  - FAR
  - Sans
  - Date enregistrement
  - Date entrée

## Code Source
```bash
<?php
namespace App\Repositories;

use App\Models\Project;

class ProjectRepository extends BaseRepository
{
    public function __construct(Project $Project)
    {
        parent::__construct($Project);
    }
    public function getData()
    {
        return parent::getData()->paginate(5);
    }
    public function projectsFilter()
    {
        return parent::getData()->select('id', 'name')->get();
    }

}

```