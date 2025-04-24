<div align="center">
<img 
  src="https://media.discordapp.net/attachments/1361521614751142080/1363654364446720162/Structur_Pz_Discord.png?ex=6806d197&is=68058017&hm=e8192d852a31bc4b630b48a2c431175e0360500e3768f387cc9d81f62a77d777&=&format=webp&quality=lossless&width=886&height=443" 
/>
</div>

# `🗂` Configuracion y ejemplos
<p align="center">Como vamos a crear cada una de las variantes del npm</p>

### pzbuttons


```js
/// Ejemplo 1 ///
const { pzbuttons } = require("struc-pz");

    const botones = pzbuttons({
      btn1: {
        label: "Botón 1",
        style: 1,
        emoji: "📌"
      }
    });

    interaction.reply({
      content: "¡Botones de interaction!",
      components: botones
    });

/// Ejemplo 2 ///
const { pzbuttons } = require("struc-pz");

    const botones = pzbuttons({
      btn1: {
        label: "Botón 1",
        style: 1,
        emoji: "📌"
      },
      btn2: {
        label: "Botón 2",
        style: 2,
        emoji: "📌"
      },
      btn3: {
        label: "Botón 3",
        style: 3,
        emoji: "📌"
      },
      btn4: {
        label: "Botón 4",
        style: 4,
        emoji: "📌"
      }
    });

    interaction.reply({
      content: "¡Botones de interaction!",
      components: botones
    });
```

### pzInteractionButtons


```js

/// Ejemplo 1 ///
const { pzbuttons, pzInteractionButtons } = require("struc-pz");

    const botonesParte1 = pzbuttons({
      btn1: {
        label: "Botón 1",
        style: 1,
        emoji: "📌"
      },
      btn2: {
        label: "Botón 2",
        style: 2,
        emoji: "📌"
      },
      btn3: {
        label: "Botón 3",
        style: 3,
        emoji: "📌"
      },
      btn4: {
        label: "Botón 4",
        style: 4,
        emoji: "📌"
      }
    });

    const botonesParte2 = pzbuttons({
      btn5: {
        label: "Botón 5",
        style: 1,
        emoji: "📌"
      },
      btn6: {
        label: "Botón 6",
        style: 2,
        emoji: "📌"
      },
      btn7: {
        label: "Botón 7",
        style: 3,
        emoji: "📌"
      },
      btn8: {
        label: "Botón 8",
        style: 4,
        emoji: "📌"
      },
      btn9: {
        label: "Botón 9",
        style: 1,
        emoji: "📌"
      },
      btn10: {
        label: "Botón 10",
        style: 2,
        emoji: "📌"
      },
      btnLink: {
        label: "Enlace",
        style: 5,
        emoji: "📌",
        url: "https://www.tu-enlace.com"
      }
    });

    const TodosBotones = pzInteractionButtons(botonesParte1, botonesParte2);

    await interaction.reply({
      content: "¡Botones de interaction!",
      components: TodosBotones
    });
 
```


### pzButtonsMsg

Nueva forma interaccion de botones

```js
/// Ejemplo 1 ///
const { pzButtonsMsg } = require("struc-pz");

    const mensajes = pzButtonsMsg(interaction);

    if (await mensajes.id("ID-BOTON")) {
      return interaction.reply({
        content: "Hola, que tal"
      });
    }

/// Otro ejemplo //
const { pzButtonsMsg } = require("struc-pz");

module.exports = (client) => {
  client.on("interactionCreate", async (interaction) => {

    const mensajes = pzButtonsMsg(interaction);

    if (await mensajes.id("ID-BOTON")) {
      return interaction.reply({
        content: "Hola, que tal"
      });
    }

  });
};

////////////// FUNCION DE ACTIVIDAD DEL BOTON ////////////////
/*
Esta funcion te la da el mismo npm para una nueva funcion que
es la actividad un ejemplo, si tu quieres desactivar un boton si
necidad de apagar el bot tu podras conectar a una base de datos
para darle la activacion de desactivacio del boton especificado
*/

/// Ejemplo 2 ///

const { pzButtonsMsg } = require("struc-pz");

    const mensajes = pzButtonsMsg(interaction);

    // Define aquí cuáles botones están activos o desactivados, por default los botones estan en true, pero si los quieres desactivar solo usa esta funcion
    mensajes.activarLista = {
      "btn-1": true,   // Activo /// Tienes que poner la id del boton asi para que el boton mande el mensaje que trae por default el npm
      "btn-2": false,    // Desactivado
    };

    // Verificar interaccion del 'btn-1' (botón Activo)
    if (await mensajes.id("btne")) {
      return interaction.reply({
        content: "Hola, este boton esta activo."
      });
    }

    // Verificar interaccion del 'btn-2' (botón desactivado)
    if (await mensajes.id("btn1")) {
      return interaction.reply({
        content: "Hola, como andas." // No tiene que mandar este mensaje porque esta desactivado
      });
    }

  }
};

```

### pzButtonsMsgAc

parte.2 / Edita el mensaje que trae por deault el npm de los botones desactivados

```js

const { pzButtonsMsg, pzButtonsMsgAc } = require("struc-pz");

    //Configuramos el mensaje embed de los botones desactivados, este embed tiene las misma funciones de *pzEmbed*  
    pzButtonsMsgAc({
      titulo: "🚫 / Botón desactivado", timestamp: true,
      descripcion: "Este botón fue desactivado por mantenimiento.&&&&Por favor para activar este boton tiene que activar el dueño del boton",
      color: "Yellow"  
    });

    const mensajes = pzButtonsMsg(interaction);

    // Define aquí cuáles botones están activos o desactivados, por default los botones estan en true, pero si los quieres desactivar solo usa esta funcion
    mensajes.activarLista = {
      "btn-1": true,   // Activo /// Tienes que poner la id del boton asi para que el boton mande el mensaje que trae por default el npm
      "btn-2": false,    // Desactivado
    };

    // Verificar interaccion del 'btn-1' (botón Activo)
    if (await mensajes.id("btne")) {
      return interaction.reply({
        content: "Hola, este boton esta activo."
      });
    }

    // Verificar interaccion del 'btn-2' (botón desactivado)
    if (await mensajes.id("btn1")) {
      return interaction.reply({
        content: "Hola, como andas." // No tiene que mandar este mensaje porque esta desactivado
      });
    }

  }
};

```
