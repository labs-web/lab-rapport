# Rapport besoin 
## Idéation 
 Créer une application conviviale pour le centre CNMH en utilisant Laravel, Bootstrap et AdminLTE. Cette application permettra une gestion plus efficace des données et une génération améliorée de rapports, avec une interface facile à utiliser pour les employés.
 ![Idéation](./images/Introduction.jpg)
## exemple  code utilisé sur la réalisation 
```<?php

namespace App\Http\Controllers;


use Illuminate\Http\Request;
use App\Repository\LikeRepository;
// Remove the line below since the Request class is already imported in the namespace
// use Illuminate\Http\Request;
use App\Models\Like;

class LikeController extends Controller
{

public function index(Request $request){
    $likes = Like::all();
    return view('Likes.index', ['likes' => $likes]);
}
}
```