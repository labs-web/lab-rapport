---
layout: default
order: 3
---

# Présentation de solicode

## A propos de nous

SOLICODE est un centre de formation solidaire et inclusif, ouvert aux jeunes motivés et intéressés par les métiers du Développement Web et Mobile. L’apprenant à SOLICODE se considère comme acteur principal tout au long de son processus d’apprentissage. 

![Apprenant en travail](./images/apprenant-en-travail.jpg){:width="80%"  }
*Figure 1 : Apprenant en travail*

C’est lui qui construit ses savoirs à travers la réalisation des projets, individuels ou par groupe, inspirés du milieu professionnel afin de favoriser une meilleure insertion au marché de travail. La formation au sein de SOLICODE est axée sur différents volets: technique, soft-skills, entreprenariat et gestion de projet. A l’issue de cette formation, les apprenants bénéficieront d’une double certification délivrée par SIMPLON et OFPPT.


## Formation Web

Une séance d’empathie a été réalisée avec Khawla souan, en tant que personnel du service social, le 20 mars 2023.

![service social Carte d'empathie](./images/service-social.png){:width="100%"  }
*Figure : Carte d'empathie*


## Code source 

Code source d'entretien social

```bash
public function FormEntretienSocial($PatientID){
        $editMode = false; 
        $couvertureMedical = new CouvertureMedicalRepository;
        $couverture_medical = $couvertureMedical->all();
        $typeHandicap = new TypeHandicapRepository;
        $type_handicap = $typeHandicap->all();
        $service = new ServiceRepository;
        $services = $service->all();
        $latestDossier = $this->dossierPatientRepository->NumeroDossier();
        $counter = $latestDossier ? (int)substr($latestDossier, 2) + 1 : 1;
        $numeroDossier = 'A-' . $counter;
        $PatientID = $PatientID;
        return view('PoleSocial.dossier_patients.entretien', compact('type_handicap', 'couverture_medical','services','editMode','PatientID','numeroDossier'));
}

```

