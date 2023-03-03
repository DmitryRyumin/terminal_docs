# Работа в терминале

![GitHub top language](https://img.shields.io/github/languages/top/DmitryRyumin/terminal_docs)
![GitHub repo size](https://img.shields.io/github/repo-size/DmitryRyumin/terminal_docs)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/DmitryRyumin/terminal_docs)
![GitHub last commit](https://img.shields.io/github/last-commit/DmitryRyumin/terminal_docs)

## Команды Linux

| Команда | Описание |
| ------- | -------- |
| `cd ~`<br>`cd` | Переход в домашний каталог |
| `pwd` | Текущий каталог |
| `open .` | Открыть текущий каталог |
| `which python` | Путь к директории Python |
| `which -a python` | Пути ко всем директориям Python |
| `which pip` | Путь к директории установщика пакетов Python |
| `ls` | Список файлов в текущей директории |
| `ls -l` | Список файлов в текущей директории с подробной информацией |
| `ls -a` | Список файлов включая скрытые в текущей директории |

## Установщик пакетов Python (`pip`)

> [Официальная документация](https://pip.pypa.io/en/stable/reference/)

> Обновление всех пакетов - `pip list --outdated --format=freeze | grep -v '^\-e' | cut -d = -f 1  | xargs -n1 pip install -U`

| Команда | Описание |
| ------- | -------- |
| `pip list` | Список установленных пакетов |
| `pip list --outdated` | Список пакетов, которые необходимо обновить |
| `pip list --uptodate` | Список пакетов, которые имеют последнюю версию |
| `pip show название_пакета_1 название_пакета_2` | Сокращенная информация об пакете или пакетах |
| `pip show --verbose название_пакета_1 название_пакета_2` | Полная информация об пакете или пакетах |
| `pip search название_пакета` | Поиск пакета в https://pypi.org/pypi |
| `pip check` | Проверка на то, что установленные пакеты имеют совместимые зависимости |
| `pip freeze` | Список пакетов, которые будут сохранены |
| `pip freeze > requirements.txt` | Сохранение текущих пакетов в файл |
| `pip install -r requirements.txt` | Установка пакетов из файла |
| `pip install название_пакета` | Установка пакета из кэша если он там имеется или из https://pypi.org/pypi |
| `pip install --no-cache-dir название_пакета` | Установка пакета всегда из https://pypi.org/pypi |
| `pip uninstall название_пакета` | Удаление пакета |
| `python3 -m pip install --upgrade pip setuptools wheel` | Обновление `pip`, `setuptools`, `wheel` |

## Менеджер проектов и установщик пакетов Poetry (`poetry`)

> [Официальная документация](https://python-poetry.org/docs/)

> [Как включить завершение табуляции для Bash, Fish или Zsh в Poetry](https://python-poetry.org/docs/#enable-tab-completion-for-bash-fish-or-zsh)

> Обновление всех установленных пакетов до последней версии - `poetry update`

| Команда | Описание |
| ------- | -------- |
| `poetry config --list` | Просмотр текущей конфигурации Poetry |
| `poetry config virtualenvs.in-project true` | Включение создания виртуальной среды в корневом каталоге проекта |
| `poetry new название_проекта` | Создание нового проекта с poetry |
| `poetry init` | Установка poetry в существующий проект |
| `poetry install` | Установка зависимостей проекта, а также создание виртуальной среды |
| `poetry install --no-root` | Установка только зависимостей |
| `poetry env use` | Активация или создание виртуальной среды для текущего проекта |
| `poetry env use необходимый_интепретатор` | Активация или создание виртуальной среды для текущего проекта с интерпретатором конкретной версии |
| `poetry env info` | Показать информацию о  текущей виртуальной среде |
| `poetry env list` | Отображение всех виртуальных сред, ассоциирующихся с текущим проектом |
| `poetry env remove` | Удаление виртуальных сред, относящихся к текущему проекту |
| `poetry shell` | Активация созданной виртуальной среды. `exit` или `deactivate` выход из виртуальной среды |
| `poetry deactivate` | Активация созданной виртуальной среды |
| `poetry add название_пакета` | Установка пакета из https://pypi.org/pypi |
| `poetry add --dev название_пакета` | Установка пакета из https://pypi.org/pypi в dev-dependencies |
| `poetry remove название_пакета` | Удаление выбранного пакета |
| `poetry show --tree` | Отображение всего дерева зависимостей установленных пакетов |
| `poetry show --latest` | Отображение для установленных зависимостей их последних версий, представленных на PyPI |
| `poetry run python your_script.py` | Запуск скрипта (executable программы) из вирутальной среды, созданной для текущего проекта |
| `poetry run black` | Запуск проекта с помощью инструментов командной строки (black, pytest и т.д.) |
| `poetry build` | Создание пакета |
| `poetry publish` | Публикация созданного пакета на PyPI |
| `poetry self update` | Обновление Poetry до последней версии |
| `poetry self update версия_poetry` | Установка конкретной версии Poetry (с указанием версии) |

## Создание пакетов Python (`Setuptools`)

> [Официальная документация](https://setuptools.readthedocs.io/en/latest/setuptools.html)

| Команда | Описание |
| ------- | -------- |
| `python setup.py sdist bdist_wheel` | Создание установочного пакета |
| `twine upload dist/*` | Загрузка установочного пакета на https://pypi.org/pypi |

## Инструмент для создания изолированных сред Python (`virtualenv`)

> [Официальная документация](https://virtualenv.pypa.io/en/latest/)

| Команда | Описание |
| ------- | -------- |
| `pip install virtualenv` | Установка пакета для создания изолированных сред |
| `virtualenv название_каталога` | Размещение новой виртуальной среды в указанном каталоге |
| `virtualenv --python=путь_к_python название_каталога` | Размещение новой виртуальной среды в указанном каталоге с указанной версией Python |
| `source название_каталога/bin/activate` | Активация вирдуальной среды в указанном каталоге `Linux` |
| `название_каталога\Scripts\activate.bat` | Активация вирдуальной среды в указанном каталоге `Windows` |
| `deactivate` | Деактивация вирдуальной среды |

## Установщик пакетов для MacOS (`brew`)

> [Официальная документация](https://brew.sh/index_ru)

| Команда | Описание |
| ------- | -------- |
| `brew --version` | Получение версии `brew` |
| `brew update` | Обновление `brew` |
| `brew install название_пакета` | Установка пакета |
| `brew list` | Список установленных пакетов |
| `brew outdated` | Список пакетов, которые необходимо обновить |
| `brew upgrade` | Обновление всех пакетов |
| `brew cleanup -n` | Список старых пакетов, которые необходимо удалить |
| `brew cleanup` | Удаление старых пакетов |

## Управление пакетами, зависимостями и средой (`Conda`)

> [Официальная документация](https://docs.conda.io/projects/conda/en/latest/index.html)

| Команда | Описание |
| ------- | -------- |
| `conda --version` | Получение версии `conda` |
| `conda config --set auto_activate_base False` | Отключение автоматического запуска  `conda` при запуске терминала |
| `conda activate` | Активация вирдуальной среды `conda` |
| `conda deactivate` | Деактивация вирдуальной среды `conda` |

## Веб-интерфейс `JupyterLab` для записных книжек Jupyter

| Команда | Описание |
| ------- | -------- |
| `jupyter nbconvert --to pdf название_файла.ipynb --template classic` | Конвертация из `ipynb` в `PDF` |

## Платформа, для управления конфигурацией Zsh (`Oh My Zsh`)

> [Официальная документация](https://ohmyz.sh/)

| Команда | Описание |
| ------- | -------- |
| `sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"` | Установка |
| `code ~/.zshrc` | Открытие конфигурационных настроек |
| `source ~/.zshrc` | Обновление конфигурационных настроек |
| `echo $ZSH_VERSION` | Версия |
| `upgrade_oh_my_zsh` | Обновление |

## Просмотр подробной информации об аудио/видео файле (`media-info`)

> [Официальная документация](https://formulae.brew.sh/formula/media-info#default)

| Команда | Описание |
| ------- | -------- |
| `brew install mediainfo` | Установка |
| `mediainfo путь_к_файлу` | Просмотр подробной информации об аудио/видео файле |
