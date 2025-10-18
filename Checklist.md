Check List:
- [ ] Add a git_source.md 
  - Because when copy in the project you can easily forget form where it came
- [ ] Add a license in the git repository and in the addons/your_addon/LICEN?CS?E.md


----------

My first validated asset was:  
[https://github.com/EloiStree/2025_04_15_gdp_kid_toy_ovni_code](https://github.com/EloiStree/2025_04_15_gdp_kid_toy_ovni_code)  

- [ ] Check that you install the good version of Godot https://godotengine.org/
  - [ ] If on PI, you can go in Pi-Apps
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
- [ ] I lkecreate a `assets/2D/` to store coming 2D items
- [ ] I create a `assets/3D/` to store coming stl, obj and fbx
  
