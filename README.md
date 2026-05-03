# Simple Flask App

Autor: Maciek (2024_L_I_S_INF_K1)

Aplikacja Dydaktyczna wyświetlająca imię i wiadomość w różnych formatach dla zajęć
o Continuous Integration, Continuous Delivery i Continuous Deployment.

- W projekcie wykorzystamy virtual environment, dla utworzenia hermetycznego środowisko dla aplikacji:

  ```
  # tworzymy hermetyczne środowisko dla bibliotek aplikacji:
  $ python -m venv .venv

  # aktywowanie hermetycznego środowiska
  $ source .venv/Source/activate
  $ pip install -r requirements.txt
  $ pip install -r test_requirements.txt

  # zobacz
  $ pip list
  ```

  Sprawdź: [tutorial venv](https://docs.python.org/3/tutorial/venv.html) oraz [biblioteki flask](http://flask.pocoo.org).

- Uruchamianie applikacji:

  ```
  # jako zwykły program
  $ python main.py

  # albo:
  $ PYTHONPATH=. FLASK_APP=hello_world flask run
  
  * **Uruchamianie za pomocą Docker i Make:**
  $ make docker_build
  $ make docker_run
  
  ```

- Uruchamianie testów (see: http://doc.pytest.org/en/latest/capture.html):

  ```
  $ PYTHONPATH=. py.test
  $ PYTHONPATH=. py.test --verbose -s
  ```

- Kontynuując pracę z projektem, aktywowanie hermetycznego środowiska dla aplikacji py:

  ```
  # deaktywacja
  $ deactivate
  ```

  ```
  ...

  # aktywacja 
  $ source .venv/Source/activate
  ```

- Integracja z CircleCI:

  ```
  # Projekt wykorzystuje CircleCI do automatycznego budowania obrazu Docker i przesyłania go na Docker Hub po każdym pushu do gałęzi master.
  ```

