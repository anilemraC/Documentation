#PHP objet
##PHP objet 10.2
```
<title>Class and Object Methods</title>
  </head>
  <body>
    <p>
      <?php
        class Person {
          public $isAlive = true;
          
          function __construct($name) {
              $this->name = $name;
          }
          
          public function dance() {
            return "I'm dancing!";
          }
        }
        
        $me = new Person("Shane");
        if (is_a($me, "Person")) {
          echo "I'm a person, ";
        }
        if (property_exists($me, "name")) {
          echo "I have a name, ";
        }
        if (method_exists($me, "dance")) {
          echo "and I know how to dance!";
        }
      ?>
    </p>
  </body>
</html>
```

 ##PHP objet 10.3
 
 ```
<html>
  <head>
    <title>The Shape of Things to Come</title>
  </head>
  <body>
    <p>
      <?php
        class Shape {
          public $hasSides = true;
        }
        
        class Square extends Shape {
        
        }
        
        $square = new Square();
        // Add your code below!
        if (property_exists($square, "hasSides") ) {
          echo "I have sides!";
        }
      ?>
    </p>
  </body>
</html>
```
 ##PHP objet 10.4
 ```
<html>
  <head>
    <title>Override!</title>
  </head>
  <body>
    <p>
      <?php
        class Vehicle {
          public function honk() {
            return "HONK HONK!";
          }
        }
        // Add your code below!
        class Bicycle extends Vehicle{
            public function honk(){
                return "Beep beep!";
                }
            }
            
            $bicycle = new Bicycle();
            echo $bicycle->honk();
        
        
      ?>
    </p>
  </body>
</html>
Raw
 PHP objet 10.5
<html>
  <head>
    <title>Override!</title>
  </head>
  <body>
    <p>
      <?php
        class Vehicle {
          final public function honk() {
            return "HONK HONK!";
          }
        }
        // Add your code below!
        class Bicycle extends Vehicle{
            public function honk(){
                return "Beep beep!";
                }
            }
            
            $bicycle = new Bicycle();
            echo $bicycle->honk();
        
        
      ?>
    </p>
  </body>
</html>
Raw
 PHP objet 10.6
<html>
  <head>
    <title>Scope it Out!</title>
  </head>
  <body>
    <p>
      <?php
      class Person {
          
      }
      class Ninja extends Person {
        // Add your code here...
        const stealth = "MAXIMUM";
      }
      // ...and here!
      if (Ninja::stealth){
          echo "MAXIMUM";
          }
      
      ?>
    </p>
  </body>
</html>
Raw
 PHP objet 10.7
<html>
  <head>
    <title></title>
  </head>
  <body>
    <p>
      <?php
        class King {
          // Modify the code on line 10...
          public static function proclaim() {
            echo "A kingly proclamation!";
          }
        }
        // ...and call the method below!
        echo King::proclaim();
      ?>
    </p>
  </body>
</html>
Raw
 PHP objet 10.8
<html>
  <head>
    <title></title>
  </head>
  <body>
    <p>
      <?php
      class Person{
      
      public function __say(){
          
          }
          
      }   
        echo "Here are my thoughts! "; 
      class Blogger extends Person{
          const cats = 50;
          static public $cats = 50;
          public static function say(){
              }
        }
        
        Blogger::$cats;
        Blogger::say();
        echo 50;
      ?>
    </p>
  </body>
</html>
Raw
 PHP objet 9.7
<!DOCTYPE html>
<html>
	<head>
	  <title> Practice makes perfect! </title>
      <link type='text/css' rel='stylesheet' href='style.css'/>
	</head>
	<body>
      <p>
        <!-- Your code here --><?php
        class Dog {
            public $numLegs = 4;
            public $name;
            
            public function __construct($name){
                $this->name = $name;
                }
            }
        ?>
      </p>
    </body>
</html>
Raw
 PHP objet 9.8
<!DOCTYPE html>
<html>
	<head>
	  <title> Practice makes perfect! </title>
      <link type='text/css' rel='stylesheet' href='style.css'/>
	</head>
	<body>
      <p>
        <!-- Your code here --><?php
        class Dog {
            public $numLegs = 4;
            public $name;
            
            public function __construct($name){
                $this->name = $name;
                }
            public function bark(){
                return "Woof!";
                }
                public function greet(){
                return " Hello, my name is " . $this->name ;    
                }
            }
                $dog1 = new Dog ("Barker");
                $dog2 = new Dog ("Amigo");
                echo $dog1->bark();
                echo $dog2->greet();
                
            
        ?>
      </p>
    </body>
</html>
Raw
 PHP objet 9.9
<!DOCTYPE html>
<html>
    <head>
	  <title> Challenge Time! </title>
      <link type='text/css' rel='stylesheet' href='style.css'/>
	</head>
	<body>
      <p>
        <?php
          // Your code here
          class Cat{
              public $isAlive = true;
              public $numLegs = 4;
              public $name;
              
              public function __construct($name){
                  $this->name = $name;
                  }
              public function meow(){
                  return "Meow meow";
                  }
              }
              $cat1 = new Cat("CodeCat");
              echo $cat1->meow();
        ?>
      </p>
    </body>
</html>
Raw
 test.blade.php (liste message bdd)
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
