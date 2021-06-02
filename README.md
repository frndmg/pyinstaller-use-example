# PyInstaller usage example

Run

```bash
poetry env use 3.8  # whatever python version you want
poetry install -E installer
```

The first time you will not have the `app.spec`, `pyinstaller` will add one for you when you run

```bash
poetry run pyinstaller -F -p . --name app app/__main__.py
```

You can remove the `pathex` argument as long as the `.spec` file is in the root of your project.

After that, you can simply use

```bash
poetry run pyinstaller app.spec
```

This will create an standalone executable in `dist/app`

Run

```bash
$ ./dist/app
output of my executable: cool string
```
