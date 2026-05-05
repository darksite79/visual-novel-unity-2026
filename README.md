# Tutorial Básico de NaniNovel en Unity 

(Se recomienda usar la versión 2023.2.20f https://unity.com/es/releases/editor/whats-new/2023.2.20f1#installs

Este proyecto es un ejemplo introductorio para crear una **novela visual en Unity** utilizando el framework **NaniNovel**.

El objetivo es que puedas entender rápidamente cómo:
- Organizar recursos (fondos, personajes y audio)
- Configurar elementos dentro de NaniNovel
- Crear una escena interactiva
- Implementar decisiones en una historia

---

## Estructura del proyecto

Los recursos principales se encuentran en:

Assets/Recursos/


Dentro de esta carpeta encontrarás:
- `Backgrounds/` → Fondos
- `Characters/` → Personajes
- `Audio/` → Música y efectos

Puedes reemplazar estos archivos por los tuyos propios.

---

##  Personajes

Cada personaje debe cumplir con:

- Imágenes en formato `.png`
- Fondo transparente
- Diferentes expresiones (estados)

Ejemplo de estados:
- Normal
- Happy
- Sad
- Angry

Recomendación:
Usa nombres claros y consistentes (ej: `Ana_Happy`, `Luis_Sad`).

---

## Fondos (Backgrounds)

- Guarda los fondos en la carpeta correspondiente
- Evita espacios en los nombres
- Usa nombres descriptivos

Ejemplo:
aula
patio
cancha


---

## Configuración en NaniNovel

### 1. Registrar Backgrounds

Ir a: Naninovel → Resources → Backgrounds

- Agregar cada fondo
- Arrastrar la imagen en el campo **Object**
- Usar nombres simples y sin espacios

---

### 2. Registrar Personajes

Ir a: Naninovel → Resources → Characters

Pasos:
1. Crear personaje (ej: Ana, Luis)
2. Agregar estados (Normal, Happy, etc.)
3. Asignar imágenes a cada estado

---

### 3. Registrar Audio

Ir a: Naninovel → Resources → Audio

- Agregar música o efectos
- Asignar archivos previamente importados

---

## Personalizar el menú inicial

Puedes cambiar la imagen de portada del juego:

Ruta: Assets/Naninovel/DefaultUI/TitleUI

Pasos:
1. Abrir `TitleUI`
2. En la jerarquía, seleccionar `Background`
3. En el inspector, cambiar **Source Image**

---

## Script básico

Los scripts se encuentran en: Assets/Scripts/

Ejemplo:

```nani
@back Aula
@bgm SchoolMemories

@char Ana.Normal
Ana: Hola, bienvenido a la clase.

@char Luis.Normal
Luis: Este es un ejemplo de novela visual.

@choice "Ir al patio" goto:Patio
@choice "Ir a la cancha" goto:Cancha
``` 
Recomendaciones

Mantén nombres consistentes entre recursos y scripts
Evita espacios en nombres de archivos
Usa PNG con transparencia para personajes
Organiza bien tus carpetas
Prueba constantemente los cambios
