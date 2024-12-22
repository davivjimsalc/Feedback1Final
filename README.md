La aplicacion es un Inventario de Productos como los sugeridos en la descripcion del Feedback.
He usado ScrollViews con LinearLayouts dinamicos para hacer la aplicacion algo mas "amigable".
He decidio usar una BBDD interna Room ya que me parece mas facil de usar, es parecido a lo que usamos en Programacion Concurrente. Tenemos una Entidad Producto, una AppDatabase y un DAO como vimos en clase

Descripcion de las actividades de la aplicacion:
1. ActivityMain:

![image](https://github.com/user-attachments/assets/7bd30717-0225-43cf-bd0a-782059be613e)

En esta actividad se muestra la lista de productos que tenemos (he considerado poner dos productos por defecto)
Cada producto tiene un boton de Detalles que nos enviara a la actividad de Detalles pasando por un Intent su imagen (todas las imagenes son Drawable), el nombre y la descripcion.
Como vemos cada producto tiene su LinearLayout el cual es dinamico, cada vez que añadimos un producto se añade un LinearLayout con su Imagen seleccionada, nombre y boton.

Arriba tenemos el action bar con un boton para ir a la actividad de EditarLista la cual nos permitira realizar acciones sobre la lista de productos del ActivityMain
Ademas hay un boton de Acerca de que muestra informacion basica sobre la aplicacion

2. EditarListaActivity:

![image](https://github.com/user-attachments/assets/37396910-4797-4989-a725-db5e35ee8586)

![image](https://github.com/user-attachments/assets/bb16a8a1-fc00-4a5e-b927-bbfc78bd7c4d)


En esta actividad nos podemos mover hacia abajo gracias al ScrollView
Se divide en 3 funciones:
  -  Añadir producto: se especifica el nombre, descripcion e imagen drawable y al darle al boton de añadir se envia al activitymain para posteriormente en el metodo onActivityResult se guarde en BBDD y se añada a la lista
  -  Editar producto: este modifica la descripcion e imagen de un producto existente aportando su nombre
  -  Eliminar producto: elimina un producto existente aportando su nombre
Esots dos ultimos en cuanto a la BBDD hacen algo parecido al de añadir pero modificando el contenido de la BBDD o eliminandolo. Lo mismo con la lista

En el action bar tenemos ahora un boton de atras y el boton de Acerca de

3. DetallesActivity:

![image](https://github.com/user-attachments/assets/6584bf25-0bc7-42ff-9e0f-15eb6dc1d02f)

Por ultimo la actividad detalles la cual muestra los datos del producto desde el cual se ha accedido
En el action bar ahora tenemos un boton de atras y el boton de Acerca de
