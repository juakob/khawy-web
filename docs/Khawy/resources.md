# Resources

All resources or assets need to be loaded before using them. We load them in a state, more specifically by overriding 
override function load(resources:Resources)
We tell khawy we want to load assets by adding loaders to resources. For example if we want to load an image call "myImage.png" we would add 
resources.add(new ImageLoader("myImage"));
if we would like to load a sound we would call 
resources.add(new SoundLoader("mySound"));

Notice that we don't set the type of the asset, thats because basic resources get optimize by kha and might be transform into another format.
We do specify the format when we load raw data. We replace points in the name with underscores.
myData.xml will be loaded using resources.add(new DataLoader("myData_xml"));

When we change the state all the resources will be unloaded by default. 

You can disable loading objects and manually do it by setting  Simulation.i.manualLoad = true;
*JoinAtlas will still be created in each load

# Loaders
## Image

## SpriteSheet

atlas.add(new SpriteSheetLoader("hero", 45, 60, 0, [
			new Sequence("fall", [0]),
			new Sequence("slide", [0]),
			new Sequence("jump", [1]),
			new Sequence("run", [2, 3, 4, 5, 6, 7, 8, 9]),
			new Sequence("idle", [10]),
			new Sequence("wallGrab", [11])
		]));