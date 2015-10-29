Centro de Proyecto Wiki Code
=======

este es el coigo para dar formato al precio


```//http://www.forosdelweb.com/f13/funcion-separacion-digitos-miles-decimales-233608/
//http://gmuro.blogspot.com/2011/09/separar-valores-con-comas-cada-tres.html
separadorDecimalesInicial="."; //Este dato entiende la separación decimal que trae el json
separadorDecimales=""; //Modifique este dato para poder obtener la nomenclatura que utilizamos en mi pais Arge aqui va ","
separadorMiles="."; //Modifique este dato para poder obtener la nomenclatura que utilizamos en mi pais
function punto(numero)
{ 
var agotado="<div class='agotado'><img  src='/static/content/pruebas/vtnAr/imagenes/agotado.png'/></div>"
var numeroo=""; 
var decimal=""; 
var deci=""; 
numero=""+numero; 
partes=numero.split(separadorDecimalesInicial);
entero=partes[0];
//document.getElementById(decimal).style.fontSize="7px";
 if(isNaN(numero )){
        return agotado;
 }
	

if(partes.length>1)
{ 
decimal=partes[1]

if(decimal.length===1)
  {
	decimal+="0";
	//decimal+=$(this).text().style.fontSize="7px";
//deci = "<span class='signoPeso'>" + decimal +"</span>"
 // deci = document.getElementById(decimal).style.fontSize="7px"
  
  }

} 
cifras=entero.length; 
cifras2=cifras 
for(a=0;a<cifras;a++)
{
cifras2-=1;
numeroo+=entero.charAt(a);
if(cifras2%3==0 &&cifras2!=0)
{
numeroo+=separadorMiles;
}
} 
if(partes.length>1)
{

numeroo+=separadorDecimales + "<span class='signoPeso'>" +decimal+"</span>";
}

return numeroo
}```
