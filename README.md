# PyInstaller usage example

Run

```bash
poetry env use 3.8  # whatever python version you want
poetry install -E installer
poetry run pyinstaller -F -p . --name app --clean app/__main__.py
```

This will create an standalone executable in `dist/app`

Run

```bash
$ ./dist/app
output of my executable: cool string
```
