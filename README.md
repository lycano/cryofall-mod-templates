# cryofall-mod-archetype-templates

A poor mans inofficial maven archetype source repository for CryoFall Starter Mods (checkout mvn-repo for actual usage).

## Getting Started

In this branch you will find the source archetypes - blueprints - used to boostrap your new mod.

### Prerequisites

You need to have `maven 3.x` and `Java Runtime 8` installed. Please make sure that you can run the command `mvn -v` from your favorite terminal.

### Quick-Start for local testing

1) Clone repo somewhere
2) Run inside cloned repo `mvn -f mod-archetype-template/pom.xml clean install archetype:update-local-catalog` \
This will build the archetype and update your local catalog which we will need in the next step
3) Go to your Project Folder - preferably your GameRoot of CryoFall Editor - and generate a new mod using previously installed archetype
```
mvn archetype:generate \
  -DarchetypeCatalog=local \
  -DarchetypeGroupId=com.github.lycano.cryofall-mod-templates \
  -DarchetypeArtifactId=mod-archetype-template \
  -DarchetypeVersion=1.0 \
  -DgroupId=CryoFall.Data.Mods.MyMod \
  -DartifactId=MyMod
```

If you run maven interactive you can change the provided default values to your liking. For testing i recommend just accepting them and press Enter when prompted.

The directory Structure will be generated from groupdId and your mod folder will be named after artifactId.
In this case you should now have a Folder structure like so: MyMod/CryoFall/Data/Mods/MyMod

Navigate down to the last folder and you will find your templated mod. \
All values you could have changed during generation of the project will be replaced recursivly. I.e. your mod is ready to use.

This is just an example to test an archetype. There will be more templates added and those might or might not use values entered during generation.

## Building your package

All future templates will use this archetype-template as a base so you should choose your groupId accordingly to match your directory structure or building your package won't work.

To build your package just run `mvn clean package`. This will create an uncompressed zip file in your root folder where you pom.xml is. This requires that directory structure matches chosen groupdId. Play around with the example command until you feel comfortable.

## Building your own archetype

Grab the mod-archetype-template and modify contents of `<your-archetype-name>/src/main/resources/archetype-resources/__artifactId__/`. Run Step 2 from `Quick-Start for local testing` section and generate your project using the command from Step 3.

## Contributing

See [master](https://github.com/lycano/cryofall-mod-templates/tree/master) branch [CONTRIBUTING.md](https://github.com/lycano/cryofall-mod-templates/tree/master/CONTRIBUTING.md)
