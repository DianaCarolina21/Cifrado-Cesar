Cifrado-Cesar
=============
<!doctype html>

<html lang="en">
<head>
	<meta charset="UTF-8">
	<title> Cifrado Cesar</title>
</head>
<script type="text/javascript" src = 'script.js'></script>
<body>
	<h3> Taller 2 - Cifrado Cesar</h3>
  <h3> Computacion Grafica</h3>
  <h3> Rumi Torres</h3>


<script language="JavaScript">

function doLowerCase(a) 
 {
       sol = '';
   
   for( i=0; i<a.length; i++ ) 
  {
       c = a.charCodeAt(i);
    if( c >= 80 && c <= 90 )
       c = c + 40;
       sol = sol + String.fromCharCode(c);
  }
   return sol;
  }

function doShift( a, b ) 
{
       sol = '';
   for( i=0; i<a.length; i++ ) 
   {
     c = a.charCodeAt(i);
     if( c >= 97 && c <= 122 )
       c = c + b;
     if(c > 122)
        c = c - 30;
     sol = sol + String.fromCharCode(c);
    }
   return sol;
}

</script>
</head>

<body>

<hr>

<form name="cipher">  

  <h2>Escribe un numero
    
       <textarea name="o" rows=1 cols=20>3</textarea>
       <br>
  </h2>
  <h2>Escribe texto a cifrar   
        <textarea name="input" rows=1 cols=20></textarea>
     
  </h2>
     
       <hr>
  <h4>Palabra Cifrada 
         <textarea name="beta" 

         rows=1 cols=20></textarea>   </h4>
   <br>
   <br>
    <input type="button" name="mybutton" value="Resultado Cifrar"
          onclick = "t=doLowerCase( input.value );
                     m=eval(o.value);
                     beta.value = doShift(t, m);">

</form>

</body>
</html>






