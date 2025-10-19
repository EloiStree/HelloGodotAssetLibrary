



My first validated asset was:
[https://github.com/EloiStree/2025_04_15_gdp_kid_toy_ovni_code](https://github.com/EloiStree/2025_04_15_gdp_kid_toy_ovni_code)

* [ ] Check that you installed the correct version of Godot: [https://godotengine.org/](https://godotengine.org/)
  * [ ] If on Pi, you can go in Pi-Apps.
* [ ] Check that you can see file extensions and hidden files (for git use).
* [ ] Create an empty GitHub repository with a simple `ReadMe.md`.
  * [ ] My format is `YYYY_MM_DD_gdp_name_of_package`.
* [ ] Clone the repository on your Pi in `Documents/Quarantine/Q_YYYY_MM_DD_gdp_name_of_package`.
  * [ ] The *Quarantine* folder is there to remind you that packages need to live by themselves.
  * [ ] `Q_` is there to remind you that it’s the quarantine folder.
* [ ] Create a new Godot project inside the repository.
* [ ] Create an `addons` folder.
* [ ] Create inside `addons` a folder with the name of your project.
  * [ ] `YYYY_MM_DD_gdp_name_of_package` for me.
  * [ ] Must be unique to you.
* [ ] Add a `LICENSE.md` to the GitHub root folder and in your addons folder.
  * [ ] The LICENSE must include your name and the date of the copyright (see documentation for more information if you are not the owner).
* [ ] Close the project and move the files to the git root.
* [ ] Reimport the project if you moved it.
* [ ] Create a `scenes/demo` folder.
* [ ] Create a `scenes/demo/main_demo.tscn` scene to welcome future users — and your future self — to the package.
* [ ] I like to create a `scenes/elements` folder to store my "prefab" nodes.
* [ ] Create a `scripts` folder to store your scripts.
* [ ] I like to create a `scripts/core` folder for scripts that are important to the package.
* [ ] Create an `assets/2D/` folder to store 2D assets.
* [ ] Create an `assets/Font/` folder to store font files.
* [ ] Create an `assets/Audio/` folder to store audio files.
* [ ] Create an `assets/3D/` folder to store `.stl`, `.obj`, and `.fbx` models.
* [ ] Create an `_addon_info` folder to store information about the addon.
* [ ] Create an `_addon_info/icons/icon.png` to store the icon used for the package.
  * [ ] Icon must be 128x128 in size.
* [ ] Create an `_addon_info/.gdignore` to tell Godot not to import it in the asset library.
  * [ ] With one character because git registers file changes.
* [ ] I like to create an `_addon_info/intend.md` with a small text describing the initial design of the tool.
  * [ ] Just to remind yourself later in case you get lost in the code.
* [ ] You can start to pre-fill the future asset library form.
  * [ ] Example of [pre-fill file](https://github.com/EloiStree/2025_04_15_gdp_kid_toy_ovni_code/blob/main/addons/2025_04_15_gdp_kid_toy_ovni_code/_addon_info/library_pre_fill.md)
  * [ ] **Asset Name:** Your asset name on the asset library.
  * [ ] **Description:** The text description that will be displayed in the asset library.
  * [ ] **Category:** `Script` if you are a developer.
  * [ ] **License:** `see LICENSE file` if you created a custom one.
  * [ ] **Repository URL:** The URL of your git repository.
  * [ ] **Issue URL:** The URL for users to report bugs in your repository.
  * [ ] **Minimum Godot Version:** The minimum Godot version you verified the code works with.
  * [ ] **Asset version:** `0.0.1`
    * [ ] I use the format `2025.12.31` because I don’t have time to manage all my packages.
  * [ ] **Commit URL:** When ready, include the commit URL of the git version you want to upload.
  * [ ] **Icon URL:** The icon URL in git with `?raw=true`.
* [ ] Add a `guides/ReadMe.md` with a welcome tutorial for online users.
* [ ] Add a `guides/.gdignore` to prevent the guide from being imported into the user’s project.
* [ ] I don’t like having screenshots in the project, but if you want:
  * [ ] Add a `screenshots/ReadMe.md` with a welcome note for online git.
  * [ ] Add a `screenshots/.gdignore` to prevent import into the project.
  * [ ] Add a `screenshots/main_screen_editor.png` for the asset library preview.
* [ ] Add a `tests/ReadMe.md` to store test scripts later.
* [ ] Create a `.editorconfig` ([See example](https://github.com/EloiStree/2025_04_15_gdp_kid_toy_ovni_code/blob/main/.editorconfig)) to set the charset and where the package should be.
* [ ] Modify the `.gitattributes` ([See example](https://github.com/EloiStree/2025_04_15_gdp_kid_toy_ovni_code/blob/main/.gitattributes)) to specify what to ignore in the WIP export (`guides`, `docs`, `screenshots`, `tests`, `.github`, `.gitignore`, `.gitattributes`).
* [ ] Add or modify the `.gitignore` from [gitignore.io](https://www.toptal.com/developers/gitignore/api/godot) ([See example](https://github.com/EloiStree/2025_04_15_gdp_kid_toy_ovni_code/blob/main/.gitignore)).
* [ ] Save everything with `git add`, `commit`, `pull`, and `push`.
* [ ] You can create a `scripts/hello_world.gd` node to say hello to your first package.
* [ ] Add a `addons/your_packaged/git_source.md` with the git source to have an alias easy access.


---

### Next Steps:

* [ ] Create what you intended to build.
* [ ] Check that your project is clean and respects code style.
* [ ] Check that you meet all asset library documentation requirements.
  * [ ] It’s a very long list.
* [ ] Verify that your demo nodes work properly before submitting.
* [ ] Test your asset without the asset library, in another project.
* [ ] Go to [https://godotengine.org/asset-library/asset](https://godotengine.org/asset-library/asset) and try to submit it with your account.
* [ ] Wait 1–5 days for validation.
* [ ] Test that it works properly once validated.
  * [ ] Correct and refactor your package if it’s refused.
