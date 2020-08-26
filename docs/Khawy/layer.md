# Layers

Layers are simply a display object(IDraw) container. The main use of them is to orginize draw order and to easly transform many objects at the same time.

## Special layers
### StaticLayer 
StaticLayer is a layer that will not be afected by the camera transforms. The main use of this kind of layers is to create the HUD.
### BakeLayer 
BakeLayer enables you to bake the content of a layer into a single image, this can be use in some cases to improve performance when you have many objects that are static.