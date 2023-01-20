# PetCare

¡Impresionante trabajo, equipo Winnipeg! Ya habéis descubierto una parte muy importante: vuestra app se llamará *PetCare*, y será una app en la cual los usuarios puedan añadir sus mascotas y otros miembros puedan ofrecerles ayuda para cuidar o pasearlas.

![](pets.webp)

Cada una de las mascotas tendrá la siguiente estructura:

```js
{
  name: String, 
  gender: String, 
  age: Number, 
  type: String, // del tipo "dog", "cat", "rabbit"
  image: String,
  needsMedicine: Boolean, 
  description: String,
  owner: ObjectId de User, //¿quién está loguinado en el momento de añadir la mascota?
}
```

Con esta información, debéis:
- Crear el modelo Pet
- Crear un archivo con un array de 10 mascotas
- Hacer un seed de la base de datos

Como habéis visto, en el modelo hay una relación. Sin embargo, en el archivo del seed no tenemos acceso a los objetos *request*, *response* y *next* para acceder a req.session.currentUser, así que, en el apartado "owner", podéis copiar y pegar `_id` de usuarios que hayáis creado previamente mediante el `signup`. 

Los `_id` los podéis copiar y pegar de la base de datos mediante Mongo Compass. Así, en el array, cada mascota tendrá un campo así:

```js
{
  ...,
  owner: '63c6f21b0629c422f95e0a7f'
}
```

Estas mascotas iniciales pueden tener todos el mismo owner o podéis coger _ids de diferentes usuarios, pero todos tienen que ser usuarios reales que existan en la base de datos.

> 📍 Cuando acabéis, debéis presentar vuestros avances en el punto de control para recibir las siguientes pistas.


