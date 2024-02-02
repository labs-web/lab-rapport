---
layout : default
---

# lap rapport

## Définir le problème

Le problème est que le centre CNMH manque un système efficace de gestion des données, ce qui entraîne des difficultés dans la génération de rapports précis et complets. Chaque département du centre utilise des méthodes traditionnelles de tenue de registres sur papier et à la plume, et seuls quelques-uns utilisent des feuilles de calcul Excel. Cela rend difficile et chronophage pour la directrice de rassembler les données dont elle a besoin périodiquement. Par conséquent, les rapports générés peuvent ne pas refléter avec précision le travail effectué par le centre et ne pas mettre en valeur leurs réalisations.
Le centre CNMH manque d'un système efficace de gestion des données, ce qui entraîne des difficultés dans la génération de rapports précis et complets.


![medecine general Carte d'empathie](./images/médecin-générale.png)

## médecin spécialiste Interne

Cela rend difficile et chronophage pour la directrice de rassembler les données dont elle a besoin périodiquement. Par conséquent, les rapports générés peuvent ne pas refléter avec précision le travail effectué par le centre et ne pas mettre en valeur leurs réalisations.
Le centre CNMH manque d'un système efficace de gestion des données, ce qui entraîne des difficultés dans la génération de rapports précis et complets.


```
    // ======== Index Function ========
    public function index(Request $request)
    {
        $query = $request->input('query');
        $projects = $this->projectRepository->paginate($query);
    
        if ($request->ajax()) {
            return view('projects.projectTablePartial')->with('projects', $projects);
        } 
        return view('projects.index')->with('projects', $projects);
    }



//  =========== Create Function ====
     public function create()
     {
         return view('projects.create');
     }


     // ===== store ==========
    public function store(CreateProjectRequest $request)
    {
        $input = $request->all();
        $this->projectRepository->create($input);
        return redirect()->route('projects.index')->with('success', 'projet ajouté avec succès');
    }


```