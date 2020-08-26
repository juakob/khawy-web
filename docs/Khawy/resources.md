# Resources

All resources or assets need to be loaded before using them. We load them in a state, more specifically by overriding 
override function load(resources:Resources)
We tell khawy we want to load somthing by adding a loader to resources. For example if we want to load an image call "myImage" we would add 
resources.add(new ImageLoader("myImage"));
if we would like to load a sound we would call 
resources.add(new SoundLoader("mySound"));

When we change the state all the resources will be unloaded. 

You can disable loading objects and manually do it by setting  Simulation.i.manualLoad = true;
*JoinAtlas will still be created in each load