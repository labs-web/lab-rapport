---
layout : default
---

# Lab Rapport

# Empathie avec infirmière de médecine général 

Elle mentionne que son rôle d'infirmière en médecine générale implique diverses responsabilités, telles que la rédaction d'un dossier médico-social, la prise en charge des patients avec l'inscription des données pertinentes comme la date, les informations personnelles et médicales, la conclusion clinique, ainsi que l'orientation. En outre, elle doit également compléter les informations nécessaires dans le dossier du patient avant de le transmettre à l'équipe médicale pour poursuivre le processus de documentation.

![medecine general Carte d'empathie](./images/médecin-générale.png)


## Empathie avec service de rééducation (Orthoptiste)
Nous accueillons les bénéficiaires accompagnés de leur bon d’orientation émis par le médecin généraliste. Pour organiser leur prise en charge, nous utilisons un tableau de temps divisé en deux parties : une pour les bénéficiaires en visite libre sans rendez-vous, et une autre pour inscrire les nouveaux patients sur la liste d'attente et les faire appeler par le service social ultérieurement.


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