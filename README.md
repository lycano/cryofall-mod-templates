# cryofall-mod-templates
Inofficial CryoFall mod-templates that can be used as a mod-starter-package using the power of maven.

## Getting started

The idea behind this github repository is to provide a collection of pre-defined starter packages to save you - the CryoFall Mod Developer - the time creating a mod from scratch. I hope that this might become useful to you and that Mod Developers share their templates and contribute to this repository.

### Goal

The following listing shall display how this repository could evolve over time.

#### Example
The following command would generate you a mod called MyMod from mod-archetype-template or if archetypeArtifactId is changed using a different starter-package given you have installed them locally. A how-to will be included in the wiki. As for now checkout README in branch [mvn-archetypes](https://github.com/lycano/cryofall-mod-templates/tree/mvn-archetypes).

Make sure you don't execute this command in your checked out repository or MyMod will be added as submodule to mod-archetype-parent which you do not want. I recommend checking out the repo in a subfolder.

I.e. create:

mod-templates \
|--> repo \
|--> playground

In playground you can generate a new mod safely. Make sure you installed the archetypes first by running `mvn clean install archetype:update-local-catalog` in repo dir after cloning having mvn-archetype as active branch.

```
mvn archetype:generate \
  -DarchetypeCatalog=local \
  -DarchetypeGroupId=com.github.lycano.cryofall-mod-templates \
  -DarchetypeArtifactId=mod-archetype-template \
  -DarchetypeVersion=1.0 \
  -DgroupId=CryoFall.Data.Mods.MyMod \
  -DartifactId=MyMod
```

#### mod-archetype-template
Basic mod structure without any functionality. No UI, no scripts just directory structure. In fact this the equivalent of [AtomicTorchStuid](https://github.com/AtomicTorchStudio/) CryoFall VSIX extension as of now. And shall be used as base for all archetypes that yet has to come.

#### mod-archetype-quickstart
A simplistic functional mod for your daily needs. Inspired by [Automaton Mod by Djekke](http://forums.atomictorch.com/index.php?topic=1097.0) this template shall provide a Simple Settings Menu with predefined keybindings to open Settings Menu of your future mod. 

#### mod-archetype-complex
A starter package that has a more complex UI - LeftPanel, MainPanel, Header and Bottom - optionally adding a HUDButton. The MainPanel changes context depending on which item in LeftPanel is selected. I.e. there could be an ItemList entry called "Items" in LeftPanel and the MainPanel would display a List of said items. Second entry could be user settings which would provide you with customizable options in MainPanel.

This idea is also inspired by [CNEI Mod by Djekke](http://forums.atomictorch.com/index.php?topic=1108.0). Which mainly motivated me to build this repository to save others the work of starting from scratch.

#### mod-archetype-....
\<Add description here>

## Concept

This repository consists of three branches.

| Branch | Description |
| --- | --- |
| mvn-archetypes | This is where all maven archetypes (templates for your mod) are stored. |
| mvn-repo | maven repository that contains all packed mod-templates. |

mvn-archetypes branch does already contain an empty mod that you can create with the official VSIX extension for VS2017. The main difference here is that you can generate your mod through `mvn archetype:generate` - as seen in example - by providing a set of properties.

mvn-repo branch currently is just a github powered mvn-repo that i used to test if its possible to deploy the  artifacts into a github branch. That branch can be used later to combine archetypes and bundle them together in an extensible manner. As of now this system is not yet in place and needs more thinking since combining those may be a difficult task as this requires to keep each artifact compatible to each other which may or may not possible.

## Built With

* [Maven](https://maven.apache.org/) - Dependency Management

## Contributing

Please read [CONTRIBUTING.md](https://github.com/lycano/cryofall-mod-templates/blob/master/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests.

## Authors

* **Lycano** - *Initial work* - [Lycano](https://github.com/lycano)

See also the list of [contributors](https://github.com/lycano/cryofall-mod-templates/contributors) who participated in this project.

## Acknowledgments

This project is provided as is and by no means an offical repository for CryoFall mods. As I was coding my first mod for CryoFall I felt the need to create a set of quick-start templates since building from scratch consumes much time which you can save now in the future.
 

---
My special thanks go to [**ai_enabled**](https://github.com/aienabled) from [**AtomicTorch Studio**](http://atomictorch.com/) who helped me a lot with understanding the 'behind the scenes' and [**Djekke**](https://github.com/Djekke) with his Mods [CNEI](https://github.com/Djekke/CNEI) and [Automaton](https://github.com/Djekke/Automaton) which greatly inspired my to create a mod for CryoFall.
