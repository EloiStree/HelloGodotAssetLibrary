Check List:
- [ ] Add a git_source.md 
  - Because when copy in the project you can easily forget form where it came
- [ ] Add a license in the git repository and in the addons/your_addon/LICEN?CS?E.md


----------

My first validated asset was:  
[https://github.com/EloiStree/2025_04_15_gdp_kid_toy_ovni_code](https://github.com/EloiStree/2025_04_15_gdp_kid_toy_ovni_code)  

- [ ] Check that you install the good version of Godot https://godotengine.org/
  - [ ] If on PI, you can go in Pi-Apps
- [ ] Check that you can see file extension and hidden files (for git use)
- [ ] Create a GitHub Repository empty with a simple ReadMe.md
  - [ ] My format is YYYY_MM_DD_gdp_name_of_package
- [ ] Clone the repository on you Pi in Document/Quarantine/Q_YYYY_MM_DD_gdp_name_of_package
  - [ ] Quarantine folder is there to remind that you need package to live by themself
  - [ ] Q_ is there to remind that is it the quarantine folder
- [ ] Create a new Godot project in the project
- [ ] Create an addons folder
- [ ] create in addons a folder with the name of your project
  - [ ] YYYY_MM_DD_gdp_name_of_package for me
  - [ ] Must be unique to you
- [ ] Add a LICENSE.md to the github root folder and in your addons folder
  - [ ] LICENSE must have Copyright you name and the date of the the copyright (see doc for more information if you are not property)
- [ ] Close the project and move the file to the git root.
- [ ] Reimport the project if you moved it
- [ ] Create a `scenes/demo` folder
- [ ] Create a `scenes/demo/main_demo.tscn` scene to welcome the package future user and yoursefl in future
- [ ] I like to create a `scenes/elements` folder where to store my "prefab" node to drop
- [ ] Create a `scripts` folder to drop your script
- [ ] I like to create a `scripts/core` folder to drop script that are important to the package
- [ ] Create a `assets/2D/` to store coming 2D items
- [ ] Create a `assets/Font/` to store coming Font items
- [ ] Create a `assets/Audio/` to store coming audio items
- [ ] Create a `assets/3D/` to store coming stl, obj and fbx
- [ ] Create a `_addon_info` to store information on the addons
- [ ] Create a `_addon_info/icons/icon.png` to store the icon to use for the package
  - [ ] Icon must be 128x128 size
- [ ] Create a `_addon_info/.gdignore` to request godot to not import that in the asset library
  - [ ] with one char because git register file change.
- [ ] I like to create a `_addon_info/intend.md` with a small text of the initial design of the tool
  - [ ]  Just to remind yourself later if you did not lost yourself in the code
- [ ] You can start to pre fill the future asset library form
  - [ ] Example of [pre fill file](https://github.com/EloiStree/2025_04_15_gdp_kid_toy_ovni_code/blob/main/addons/2025_04_15_gdp_kid_toy_ovni_code/_addon_info/library_pre_fill.md)
  - [ ] Asset Name: you asset name on the asset library
  - [ ] Description: The text description that is going to be display in the asset library
  - [ ] Category: `Script` if you are a developer
  - [ ] License: `see LICENSE file` if you created a custum one
  - [ ] Repository URL: the url of your git repository
  - [ ] Issue URL: the url of the issue to report bug in the git repository
  - [ ] Minimum Godot Version: the minimum godot version you verified the code worked
  - [ ] Asset version: `0.0.1`
    - [ ] I use a format 2025.12.31 format because I don t have time to deal with all my package.
  - [ ] Commit URL: When you are ready and all is ready in the package you will have to give the commit of the git you want to upload in users
  - [ ] The icon url in git with  `?raw=true`
- [ ] Add a `guides/ReadMe.md` with a welcome tutorial for the online git
- [ ] Add a `guides/.gdignore` to know have the guide in the projet of the user
- [ ] I dont like to have screenshot in the project but you want
  - [ ] Add a `screenshots/ReadMe.md` with a welcome tutorial for the online git
  - [ ] Add a `screenshot/.gdignore` to know have the guide in the projet of the user
- [ ] Add a `tests/ReadMe.md` to store some testing script later on in the project
- [ ] Create a `.editorconfig` ([See](https://github.com/EloiStree/2025_04_15_gdp_kid_toy_ovni_code/blob/main/.editorconfig)) to set the cahrset and the whre the package should be
- [ ] Modify the `.gitattributes` ([See](https://github.com/EloiStree/2025_04_15_gdp_kid_toy_ovni_code/blob/main/.gitattributes)) to notify what to ignore in the wip export (guides, docs , screenshot, tests , .github .gitignore .gitattributes
- [ ] Let save all that for now with a git add commit pull push
