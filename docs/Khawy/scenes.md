# Scenes
Scenes in khawy are responsible of loading resources updating entities and rendering the content inside of them. Khawy runs one main scene and you may add sub scenes to it. For example you could have a class that inherits from scene that represents a level (you load the the game assets and manage them there) and another class that also inherits from scene that represents the pause menu that is added as a sub scene to the main level scene. 

## The important functions:

### `override public function init() `
here is were you init all your stuff, avoid using new because you may find  uninitialized attributes. No need to call super.init();

### `override public function update(dt:Float)`
this function is call each update with the delta time(elapsed time) since the last call. It's important to call super.update(dt); or the scene children won't be updated.

### `override function load(resources:Resources)`
in this function you need to tell khawy what assets you are going to use in the scene. You do that by adding loaders to resources. 

For example:

    override function load(resources:Resources) {
        resources.add(new DataLoader(room+"_tmx"));
        var atlas=new JoinAtlas(2048,2048);
        atlas.add(new TilesheetLoader("tiles", 10,10,1));
        atlas.add(new SparrowLoader("skins", "skins_xml"));
        resources.add(atlas);
    }


