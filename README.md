# On Save Hook Plug-in for Eclipse

This plug-in can execute your commands every time you save (including change, create, delete) something in Eclipse editor. 

## How To Install
1. Download [OnSaveHookPlugin-0.1.8.zip](https://github.com/ktommyk/eclipse-on-save-hook-plugin/releases/download/0.1/OnSaveHookPlugin-0.1.8.zip). 
1. Start Eclipse, and select `Help`->`Install New Software...` from the menu bar. 
1. Install this archive file according to following instruction: 

*Select the archive file:*

![eclipse-plugin-installation](https://user-images.githubusercontent.com/13780300/34488010-155e8e50-f01a-11e7-81ab-a4782675ab41.png)


*Progress installation procedures as usual:*

![eclipse-plugin-installation2](https://user-images.githubusercontent.com/13780300/34488049-3d1969b0-f01a-11e7-8e5f-255ea64eafa4.png)


4. Restart your Eclipse IDE.


## How To Configure
You can configure this plug-in per project. 

1. Create a config file with a name `on_save_hook.conf` on the top directory of your target project.  
2. In that file, you must set `exec` item as below: 
`exec=C:/Users/test_user/workspace/TestProject/execute_file.bat`

3. Optionally, you can add two items,  `include` and `exclude` which are used for filtering target files by their names. 

## How To Execute
This plug-in will run the `exec` each time when a file's changed, created and deleted, I suppose. 

1. Change ( or create, delete ) any file in the project.
2. Then you can see some output on the console view from this plug-in.
 ( If you can't find any output on the view, make sure that the plug-in is installed correctly into your Eclipse. )
3. You will also see output out there if you echo ( or print ) something in the `exec` file, 
