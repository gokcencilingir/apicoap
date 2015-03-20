**Note:** pathToApicoAp in this command should be replaced by the path ApicoAP\_GUI.py resides. This command will prepare a spec file, and the path/name of the prepared spec file will be printed to the screen, this path/name should be provided to the next command

  * Before running the next command, add the following lines at the end of the spec file prepared with the previous command:

```
import sys
if sys.platform.startswith("darwin"):
    app = BUNDLE(exe,
                 name=os.path.join('dist', 'NAME.app'),
                 version=version)
```

and run the following command:

> python Build.py pathToSpecfile/specfile

**Note:** pathToSpecfile/specfile in this command should be replaced by the path/name of the spec file prepared by the last command. These commands should create a folder under "pyinstaller-1.5" folder named "apicoAp". Under "apicoAp/dist" folder, apicoAp.app should reside. Copy this file under the folder "apicoAp" (in which apicoAP\_GUI.py resides) and launch it from there.