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



```js
Proximamente

```
