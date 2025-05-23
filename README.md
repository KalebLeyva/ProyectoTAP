# Proyecto-Uso-Libreria
DESCRIPCION Y USO PARA LA LIBRERIA JSonidos
===========================================
¡Gracias por utilizar nuestra librería JSonidos!
A continuación, te explicamos cómo integrarla y aprovechar sus funcionalidades para agregar sonidos a tus componentes JText.
Una vez que hayas agregado el archivo .jar de JSonidos a tu proyecto, debes importar las siguientes clases:
import PaquetePrincipal.SonidoTecla;
import java.awt.event.KeyEvent;

//Como configurar un sonido a tus JtextField de nuestra librería//

Debes crear un método privado 
private void configurarSonidos()

![img1](Imagenes/1.png)

En el cual utilizaras los métodos para utlizar los sonidos introducidos por nosotros a tus JTextField
como por ejemplo:

SonidoTecla.configurarSonidoGeneral(txtBurbujas, "bubble");

![img2](Imagenes/2.png)

Dentro del método, usa SonidoTecla.configurarSonidoGeneral() para asignar sonidos.
El primer parámetro es el JTextField al que deseas aplicar el sonido.
El segundo parámetro es el nombre del sonido (entre comillas).
como ejemplo tenemos un txtBurbujas.

Después de la coma, introduces en forma de texto con las comillas, el nombre del tipo de sonido que desees vincularle, aquí estan ejemplos
con todos nuestros sonidos.

SonidoTecla.configurarSonidoGeneral(txtClick, "click");
SonidoTecla.configurarSonidoGeneral(txtSans, "sans");
SonidoTecla.configurarSonidoGeneral(txtGolpe, "golpe");
SonidoTecla.configurarSonidoGeneral(txtBip, "bip");
SonidoTecla.configurarSonidoGeneral(txtIphone, "iphone");
SonidoTecla.configurarSonidoGeneral(txtPs4, "ps4");
SonidoTecla.configurarSonidoGeneral(txtTip, "tip");
SonidoTecla.configurarSonidoGeneral(txtWik, "wik");

![img3](Imagenes/img3.png)

No olvides llamar al método debajo de initComponents
initComponents();
configurarSonidos();

![img4](Imagenes/4.png)
Con esto tendrás disponible el sonido deseado listo para usarse y agregado.

//Como Cargar y usar tus sonidos personalizados y también introducir un sonido para alguna tecla en especifico//

Primero debes crear el método privado
private void cargarSonidosPersonalizados() {

![img5](Imagenes/5.png)
En el cual debes utilizar el siguiente método
 SonidoTecla.agregarSonido

 ![img6](Imagenes/6.png)
Simplemente debes asignar un nombre y copiar la dirección de ruta del sonido deseado.
Ten en mente que los archivos .wav deben:

Tener máximo 1 segundo de duración

Estar en formato PCM estándar

No pesar más de 500KB

Antes de la primer coma, con comillas escribimos el nombre de nuestro sonido personalizado
En la segunda coma entre comillas debes anotar la dirección de ruta y el nombre del archivo .wav
Tal y como se muestra en el siguiente ejemplo.
SonidoTecla.agregarSonido("golpe_personalizado", "C:/Users/MSI/Downloads/Sonido-golpe.wav")
Con esto tendrás tu sonido personalizado listo para usarse
Asi que dentro de tu metodo configurarsonido puedes aplicarle el sonido a tu JText
SonidoTecla.configurarSonidoGeneral(txtPersonal1, "golpe_personalizado");

![img7](Imagenes/7.png)

No olvides agregar el método abajo de initComponents
initComponents();
         cargarSonidosPersonalizados();
        configurarSonidos();

Para asignar un sonido a una tecla en especifico dentro de tu JText, puedes aplicar lo siguiente
Por ejemplo aquí asigne un sonido personalizado a un JText
SonidoTecla.configurarSonidoGeneral(txtPersonal2, "bip_personalizado");
Pero agregando este método dentro de configurarSonidos
 SonidoTecla.asignarSonidoATecla(txtPersonal2, KeyEvent.VK_SPACE, "golpe_personalizado");

 ![img8](Imagenes/8.png)
Con ayuda de la librería KeyEvent, pude asignarle un evento a la tecla enter, el cual
cuando esta sea presionada, hará el sonido que se haya llamado, en este caso
un sonido de golpe que importe desde mis sonidos propios
Ahora con eso cuando presionemos cualquier tecla hará el sonido de bip que agregué pero
específicamente cuando presione la tecla espacio, reproducirá un sonido de golpe que también importé

Con esto ya estas listo para utilizar nuestra librería en tus proyectos, Gracias!

Para mejor explicación y mas detalles puedes mirar el siguiente video
https://youtu.be/0JCzn5Vf_gg

Por:
KALEB DANIEL LEYVA SOLIS,
EDUARDO YAEL MENDOZA MARTINEZ
