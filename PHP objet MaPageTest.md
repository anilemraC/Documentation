test.blade.php (liste message bdd)
 
 ```
test.blade.php

@extends('pages.template.menu') 

@section('titre') 
    Test
@endsection 

@section('contenu')

    <div class=" col-sm-offset-4 col-md-offset-3  col-lg-offset-2 contenue_Style">

    @foreach ($commentaires as $commentaire)

    	<p>This is commentaire {{ $commentaire->object }}</p>

	@endforeach
			
	</div>
@endsection
________________
web.php

...
Route::get('/test', 'TestController@index');
_________________
TestController.php

<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;
use Illuminate\Support\Facades\DB;

class TestController extends Controller
{
    /**
     * Display a listing of the resource.
     *
     * @return \Illuminate\Http\Response
     */
    public function index()
    {
        //
        $commentaires = DB::select('select * from message');
        // dd($commentaires);

        $data = array(
            'commentaires' => $commentaires
        );
        return view ('pages.test', $data);
    }      
    
    ```
