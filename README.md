# GradleHax

This module is specifically derived from the modular gradle system employed by Darkhax in the library mod, [Bookshelf](https://github.com/Darkhax-Minecraft/Bookshelf).

It is modified in some aspects to provide specific support for systems that are regularly used in my mods and in the mods of Mystic Modding for 1.16.5.

Some of the additional features include:

- A shadow module to handle [Registrate](https://github.com/tterrag1098/Registrate/) and [Noobutil](https://github.com/noobanidus/NoobUtil/) integration.
- Optional modules for the following mods, if the relevant `version` variable is defined in `gradle.properties`:
  - Dynamic Trees
  - Mystical World
  - Patchouli
  - Just Enough Items
- Additionally it provides a data generator default run task.
- It additionally provides a simple `api` task that is defined through `gradle.properties`: simply create an api variable that contains the path to your `api` module. This may not be appropriate for all circumstances.
- It adds the capacity to per-project disable Patreon integration (define `patreon_disabled=true` in your `gradle.properties`)
- It allows you to specify the `previous_commit` using `gradle.properties`. Warning: failing to set this to a valid commit (or failing to unset it) will result in IDE imports failing almost immediately. This may be removed in future.

Individual modules that you don't require can be removed from the `build.gradle` file.

## Setup

For a full setup, you will need the appropriate `build.gradle` and `gradle.properties` file. **See the [wiki](https://github.com/noobanidus/gradlehax/wiki) for examples of these.**

Additionally, you will most likely need to delete your current `gradle` folder. Once you have committed the removal of the folder, you can then instantiate the submodule.

Through the command-line, this is done thus: `git submodule add https://github.com/noobanidus/gradlewhax gradle`. You will want to use `git submodule init` to initialise the submodule in a new checkout of an existing project, and `git submodule update` if the submodule has been changed remotely, after pulling. To update the submodule to the latest HEAD of this repository, run `git submodule update --remote` and then commit the changes.

Finally, you will need and replace your `gradlew` and `gradlew.bat` files with the versions from this repository. 
