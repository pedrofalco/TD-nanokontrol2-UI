## TD nanoKontrol2 UI 🕹

`ES`
Esta es una herramienta para comunicar y mapear automáticamente valores MIDI controlados por el controlador [Korg nanoKontrol2](https://www.korg.com/ar/products/computergear/nanokontrol2/) y [TouchDesigner](https://derivative.ca/).
El repositorio contiene dos componentes `.tox` los cuales son ambos necesarios. `midiIn_nanoKontrol2.tox` se encarga de reconocer el dispositivo MIDI, normalizar los valores entre 0-1 y exportar esa data a `nanoKontrol2.tox` -interfaz gráfica.
El componente `nanoKontrol2.tox` funciona de manera bidireccional y en tiempo real.

### Como linkear el componente al dispositivo MIDI en TouchDesigner 🎛
Antes de conectar el contraldor MIDI via USB y de abrir los archivos  `.tox` es necesario detectar el dispositivo.

```
# en la esquina superior izquiera de TouchDesigner
DIALOGS -> MIDI DEVICE MAPPER -> seleccionar nanoKONTROL en las tres opciones
```

Al usar tu controlador MIDI ya deberías ver que los valores se actualizan
> 💡 Nota: Si aún seteado sigue sin reconocer el dispositivo, cerrar el proyecto y volver a abrirlo con el controlador MIDI conectado.

### Rápida implementación 🚩 

Simplemente arrastrar los archivos `.tox` en el proyecto en el que estes trabajando tu instalación o tus visuales.

### Como utilizar la interfaz gráfica 🎚

El componente `nanoKontrol2` (un nivel arriba de donde se encuentra este README) recibe la data MIDI ya mapeada del componente `midiIn_nanoKontrol2`. Esos valores están mapeados a los parámetros de `nanoKontrol2` y se comunica de manera bidireccional con el componente `UI` -interfaz gráfica.
Los valores MIDI entran y salen a los parámentros custom del componente `nanoKontrol2` por lo que es útil tener separado la interfaz gráfica del contenido. De esta manera se puede dividir por que canal sale cada output.
> 💡 Nota: el componente `UI` se puede eliminar y el sistema no se romperá. Esto puede ser útil en el caso de que se quiera
ahorrar recursos gráficos pero seguir utilizando los parámetros custom del componente `nanoKontrol2`.

El componente se puede utilizar indistintamente de múltiples maneras:
- Mover los knobs, botones y sliders del controlador KORG nanoKontrol2 conectado via USB.
- Activar la vista del componente `nanoKontrol2` o `UI` para interactuar con los widgets (perillas, sliders y botones).
- Mover los parámetros custom del componente `nanoKontrol2`.
> 💡 Nota: siempre los valores MIDI estarán actualizandose en tiempo real, no importa si se utiliza más de una via.

### Importante 🚧
Es importante no tocar el componente `basicWidgets`.

---

`EN`

This is a tool to automatically communicate and map MIDI values controlled by the [Korg nanoKontrol2](https://www.korg.com/ar/products/computergear/nanokontrol2/) controller and [TouchDesigner](https://derivative.ca/).
The repo contains two `.tox` components which are both necessary. `midiIn_nanoKontrol2.tox` takes care of recognizing the MIDI device, normalizing the values between 0-1 and exporting that data to `nanoKontrol2.tox` -graphical interface.
The `nanoKontrol2.tox` component works bidirectionally and in real time.

### How to link the component to the MIDI device in TouchDesigner 🎛
it's necessary to detect and link the device before connecting the MIDI controller via USB and dragging the `.tox` files.

```
# In the top left corner of TouchDesigner
DIALOGS -> MIDI DEVICE MAPPER -> select nanoKONTROL in the three options
```

When using your MIDI controller you should already see that the values are updated.
> 💡 Note: If the device is still not recognized, close the project and reopen the project with the MIDI controller already connected.

### Quick implementation 🚩 

Simply drag the `.tox` files into the project where you're working on your installation or your visuals.

### How to use the graphical interface 🎚

The `nanoKontrol2` component (one level above where this README is placed) receives the already mapped MIDI data from the `midiIn_nanoKontrol2`component.
Those values are mapped to the parameters of `nanoKontrol2` and it communicates bi-directionally with the `nanoKontrol2` component.
bidirectionally with the `UI` (graphical interface) component.
The MIDI values are mapped in and out to the custom parameters of the `nanoKontrol2` component so it is useful to have separate the graphical interface from the content. This way it's possible to divide by which channel each output goes out.
> Note: the `UI` component can be removed and the system will not break. This can be useful in case you want to save graphic resources but still use the custom parameters of the `nanoKontrol2` component.

The component can be used interchangeably in multiple ways:
- Move the knobs, buttons and sliders of the KORG nanoKontrol2 controller connected via USB.
- Activate the `nanoKontrol2` or `UI` component view to interact with the widgets (knobs, sliders and buttons).
- Move the custom parameters of the `nanoKontrol2` component.
> 💡 Note: always the MIDI values will be updated in real time, no matter if you use more than one way.

### Important 🚧
It is important not to touch the `basicWidgets` component.

🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴🛴