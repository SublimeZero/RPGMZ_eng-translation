[Class Tree](index.md)

# Class: [Tilemap](Tilemap.md).Renderer

## Superclass: [PIXI.ObjectRenderer](http://pixijs.download/v5.3.12/docs/PIXI.ObjectRenderer.html)

Renderer.

Changes made in version 1.2.1.

Related Classes: [RPG.Map](RPG.Map.md), [RPG.Tileset](RPG.Tileset.md), [Game_Map](Game_Map.md), [Spriteset_Map](Spriteset_Map.md), [Tilemap.Layer](Tilemap.Layer.md)

### new Tilemap.Renderer ()

---

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_shader` | [PIXI.Shader](http://pixijs.download/v5.3.12/docs/PIXI.Shader.html) | Shader |
| `_images` | [Array](Array.md)&lt;[image](image.md)&gt; | Array of images |
| `_internalTextures` | [Array](Array.md)&lt;[PIXI.BaseRenderTexture](http://pixijs.download/v5.3.12/docs/PIXI.BaseRenderTexture.html)&gt; | Textures |
| `_clearBuffer` | [Uint8Array](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array) | Buffer |

---

### Methods Inherited from Superclass

#### [PIXI.ObjectRenderer](http://pixijs.download/v5.3.12/docs/PIXI.ObjectRenderer.html)

* [flush ()](http://pixijs.download/v5.3.12/docs/PIXI.ObjectRenderer.html#flush)
* [render (object)](http://pixijs.download/v5.3.12/docs/PIXI.ObjectRenderer.html#render)
* [start ()](http://pixijs.download/v5.3.12/docs/PIXI.ObjectRenderer.html#start)
* [stop ()](http://pixijs.download/v5.3.12/docs/PIXI.ObjectRenderer.html#stop)

---

### Methods

### _createVao ()
Generates the VAO.

---

### _createShader () → {[PIXI.Shader](PIXI.Shader.md)}
Generates the shader.

---

### _createInternalTextures ()
Generates internal textures.

---

### _destroyInternalTextures()
Destroys internal textures.

---

### bindTextures (renderer)
Binds the textures.

##### Arguments:

| Identifier | Type | Description |
| --- | --- | --- |
| `renderer` |  [PIXI.Renderer](http://pixijs.download/v5.3.12/docs/PIXI.Renderer.html) | Renderer |

---

#### destroy ()
Override: [PIXI.ObjectRenderer](http://pixijs.download/v5.3.12/docs/PIXI.ObjectRenderer.html#destroy)

---

#### initialize ()
Override: [PIXI.ObjectRenderer](http://pixijs.download/v5.3.12/docs/PIXI.ObjectRenderer.html#initialize)

---

### getShader () → {[PIXI.Shader](PIXI.Shader.md)}
Gets the shader.

---

### contextChange ()
Changes the context.

---

### updateTextures (renderer, images) 
Updates the textures.

##### Arguments:

| Identifier | Type | Description |
| --- | --- | --- |
| `renderer` |  [PIXI.Renderer](http://pixijs.download/v5.3.12/docs/PIXI.Renderer.html) | Renderer |
| `images` | [Array](Array.md)&lt;[Bitmap](Bitmap.md)&gt; | Array of images |
