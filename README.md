<div align="center">
<img 
  src="https://media.discordapp.net/attachments/1361521614751142080/1363654364446720162/Structur_Pz_Discord.png?ex=6806d197&is=68058017&hm=e8192d852a31bc4b630b48a2c431175e0360500e3768f387cc9d81f62a77d777&=&format=webp&quality=lossless&width=886&height=443" 
/>
</div>

## `📌` Proposito del npm
<div align="center">
<p align="center">El proposito del npm esta enfocado a que los usuarios como nuevos o ya experimentados que puedan hacer una
simplificación de los embeds o otros componentes dentro de su bot de discord sin necesidad de andar adaptando
su código o agregado mas proporciones.</p>


</div>


## `📥` Instalacion en NPM
```cli
npm i struc-pz
```

## `💻` Soporte de ayuda
### Soporte de la comunidad
<a href="https://discord.gg/"><img src="https://discord.com/api/guilds/833309512412299276/widget.png" alt="Coding support server"/></a>



# `🤖` Configuracion

`Como llamariamos al npm`
```js
const { *TODAS SU VARIANTES* } = require("struc-pz");
```

`Todas las variantes existentes del npm para tu bot`
```js

/// EMBEDS ///
  pzEmbed // Crea una nueva forma para los embeds
  pzInteractionEmbeds // Enviara la cantidad de embeds especificados a la interaccion

/// BOTONES ///
  pzbuttons // Crea una nueva forma para los botones
  pzInteractionButtons // Enviara la cantidad de botones especificados a la interaccion
  pzButtonsMsg // Crea la interaccion de los botones en otra forma, como activarlos y desactivarlos
  pzButtonsMsgAc // Edita el mensaje de desactivacion de los botones

```

# `🗂` Configuracion y ejemplos
<p align="center">Como vamos a crear cada una de las variantes del npm</p>

### pzEmbed


```js
/// EJEMPLO 1 ///
const { pzEmbed } = require("struc-pz");

    const EmbedEjemplo_1 = pzEmbed({
      ejemplo1: {
        titulo: "",
        descripcion: "", // Tienes la ventaja de poner y usar && para hacer saltos de linea mas rapidos
        color: "",
        url: "",
        author: {
          name: "",
          iconURL: "",
          url: ""
        },
        thumbnail: "",
        fields: [
          { name: "", value: "" },
          { name: "", value: "" },
          { name: "", value: "", inline: true },
        ],
        url_img: "",
        timestamp: true, // Tienes 2 opciones true y false
        footer: { text: "" }
      }
    });

    interaction.reply({
      embeds: EmbedEjemplo_1 //No es necitas esto [] para enviarlo
    });

/// EJEMPLO 2 ///

    const EmbedEjemplo_2 = pzEmbed({
      ejemplo2: {
        titulo: "",
        descripcion: "", // Tienes la ventaja de poner y usar && para hacer saltos de linea mas rapidos
        color: "",
        url: "",
        author: {
          name: "",
          iconURL: "",
          url: ""
        },
        thumbnail: "",
        fields: [
          { name: "", value: "" },
          { name: "", value: "" },
          { name: "", value: "", inline: true },
        ],
        url_img: "",
        timestamp: true, // Tienes 2 opciones true y false
        footer: { text: "" }
      },
      ejemplo_2: {
        titulo: "",
        descripcion: "", // Tienes la ventaja de poner y usar && para hacer saltos de linea mas rapidos
        color: "",
        url: "",
        author: {
          name: "",
          iconURL: "",
          url: ""
        },
        thumbnail: "",
        fields: [
          { name: "", value: "" },
          { name: "", value: "" },
          { name: "", value: "", inline: true },
        ],
        url_img: "",
        timestamp: true, // Tienes 2 opciones true y false
        footer: { text: "" }
      },
    });

    interaction.reply({
      embeds: EmbedEjemplo_2 //No es necitas esto [] para enviarlo
    });
```

### pzInteractionEmbeds


```js
/// EJEMPLO 1 ///
const { pzEmbed, pzInteractionEmbeds } = require("struc-pz");

    const EmbedEjemplo_1 = pzEmbed({
      ejemplo1: {
        titulo: "",
        descripcion: "", // Tienes la ventaja de poner y usar && para hacer saltos de linea mas rapidos
        color: "",
        url: "",
        author: {
          name: "",
          iconURL: "",
          url: ""
        },
        thumbnail: "",
        fields: [
          { name: "", value: "" },
          { name: "", value: "" },
          { name: "", value: "", inline: true },
        ],
        url_img: "",
        timestamp: true, // Tienes 2 opciones true y false
        footer: { text: "" }
      }
    });

    const EmbedEjemplo_2 = pzEmbed({
      ejemplo1: {
        titulo: "",
        descripcion: "", // Tienes la ventaja de poner y usar && para hacer saltos de linea mas rapidos
        color: "",
        url: "",
        author: {
          name: "",
          iconURL: "",
          url: ""
        },
        thumbnail: "",
        fields: [
          { name: "", value: "" },
          { name: "", value: "" },
          { name: "", value: "", inline: true },
        ],
        url_img: "",
        timestamp: true, // Tienes 2 opciones true y false
        footer: { text: "" }
      }
    });

    const EmbedsTodos = pzInteractionEmbeds(EmbedEjemplo_1, EmbedEjemplo_2)

    interaction.reply({
      embeds: EmbedsTodos //No es necitas esto [] para enviarlo
    });

/// EJEMPLO 2 ///

    const EmbedEjemplo_2 = pzEmbed({
      ejemplo2: {
        titulo: "",
        descripcion: "", // Tienes la ventaja de poner y usar && para hacer saltos de linea mas rapidos
        color: "",
        url: "",
        author: {
          name: "",
          iconURL: "",
          url: ""
        },
        thumbnail: "",
        fields: [
          { name: "", value: "" },
          { name: "", value: "" },
          { name: "", value: "", inline: true },
        ],
        url_img: "",
        timestamp: true, // Tienes 2 opciones true y false
        footer: { text: "" }
      },
      ejemplo_2: {
        titulo: "",
        descripcion: "", // Tienes la ventaja de poner y usar && para hacer saltos de linea mas rapidos
        color: "",
        url: "",
        author: {
          name: "",
          iconURL: "",
          url: ""
        },
        thumbnail: "",
        fields: [
          { name: "", value: "" },
          { name: "", value: "" },
          { name: "", value: "", inline: true },
        ],
        url_img: "",
        timestamp: true, // Tienes 2 opciones true y false
        footer: { text: "" }
      },
    });

    const EmbedEjemplo_3 = pzEmbed({
      ejemplo3: {
        titulo: "",
        descripcion: "", // Tienes la ventaja de poner y usar && para hacer saltos de linea mas rapidos
        color: "",
        url: "",
        author: {
          name: "",
          iconURL: "",
          url: ""
        },
        thumbnail: "",
        fields: [
          { name: "", value: "" },
          { name: "", value: "" },
          { name: "", value: "", inline: true },
        ],
        url_img: "",
        timestamp: true, // Tienes 2 opciones true y false
        footer: { text: "" }
      },
      ejemplo_3: {
        titulo: "",
        descripcion: "", // Tienes la ventaja de poner y usar && para hacer saltos de linea mas rapidos
        color: "",
        url: "",
        author: {
          name: "",
          iconURL: "",
          url: ""
        },
        thumbnail: "",
        fields: [
          { name: "", value: "" },
          { name: "", value: "" },
          { name: "", value: "", inline: true },
        ],
        url_img: "",
        timestamp: true, // Tienes 2 opciones true y false
        footer: { text: "" }
      },
    });

    const EmbedsCompletos = pzInteractionEmbeds(EmbedEjemplo_2, EmbedEjemplo_3)

    interaction.reply({
      embeds: EmbedsCompletos //No es necitas esto [] para enviarlo
    });
```

# `🧰` Para mas informacion y ayuda
<p align="center">si quieres los ejemplos de botones puedes ir a la guia oficial del npm
aqui te dejo un acceso directo a la guia</p>

<div align="center">
  <h2><a href="https://github.com/Miu-klipsCoding2/Structur-Pz-Discord-Guide">Structur-Pz Discord Guide</a></h2>
</div>
