
```bash

lanak@ASUS-ROG-BEAST MINGW64 ~/documents/PsyCharm/projects/demo-app-2
$
mkdir projects
cd projects
mkdir demo-app
cd demo-app
touch demo.py

python -m venv env
source env/Scripts/activate

(env)
lanak@ASUS-ROG-BEAST MINGW64 ~/documents/PsyCharm/projects/demo-app-2
$

pip freeze
[NOTHING]

deactivate

lanak@ASUS-ROG-BEAST MINGW64 ~/documents/PsyCharm/projects/demo-app-2
$

```

Create an environment
```python
python -m venv env
```

Activate the environment
```python
source env/Scripts/activate
```

Install the requirements from a .txt
```python
pip intall -r requirements.txt
```

Check installed packages
```python
pip freeze
```

```python
pip list
```

Remove an environment
```python
rm -r env/
```
