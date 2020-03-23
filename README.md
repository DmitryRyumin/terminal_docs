# Работа в терминале

![GitHub top language](https://img.shields.io/github/languages/top/DmitryRyumin/docs_terminal)
![GitHub repo size](https://img.shields.io/github/repo-size/DmitryRyumin/docs_terminal)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/DmitryRyumin/docs_terminal)
![GitHub last commit](https://img.shields.io/github/last-commit/DmitryRyumin/docs_terminal)

## Команды Linux

| Команды | Описания |
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

| Команды | Описания |
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
| `pip list --outdated --format=freeze | grep -v '^\-e' | cut -d = -f 1  | xargs -n1 pip install -U` | Обновление всех пакетов |

## Создание пакетов Python (`Setuptools`)

> [Официальная документация](https://setuptools.readthedocs.io/en/latest/setuptools.html)

| Команды | Описания |
| ------- | -------- |
| `python setup.py sdist bdist_wheel` | Создание установочного пакета |
| `twine upload dist/*` | Загрузка установочного пакета на https://pypi.org/pypi |

## Инструмент для создания изолированных сред Python (`virtualenv`)

> [Официальная документация](https://virtualenv.pypa.io/en/latest/)

| Команды | Описания |
| ------- | -------- |
| `pip install virtualenv` | Установка пакета для создания изолированных сред |
| `virtualenv название_каталога` | Размещение новой виртуальной среды в указанном каталоге |
| `virtualenv --python=путь_к_python название_каталога` | Размещение новой виртуальной среды в указанном каталоге с указанной версией Python |
| `source название_каталога/bin/activate` | Активация вирдуальной среды в указанном каталоге `Linux` |
| `название_каталога\Scripts\activate.bat` | Активация вирдуальной среды в указанном каталоге `Windows` |
| `deactivate` | Деактивация вирдуальной среды |

## Установщик пакетов для MacOS (`brew`)

> [Официальная документация](https://brew.sh/index_ru)

| Команды | Описания |
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

| Команды | Описания |
| ------- | -------- |
| `conda --version` | Получение версии `conda` |
| `conda config --set auto_activate_base False` | Отключение автоматического запуска  `conda` при запуске терминала |
| `conda activate` | Активация вирдуальной среды `conda` |
| `conda deactivate` | Деактивация вирдуальной среды `conda` |

## Платформа, для управления конфигурацией Zsh (`Oh My Zsh`)

> [Официальная документация](https://ohmyz.sh/)

| Команды | Описания |
| ------- | -------- |
| `sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"` | Установка |
| `code ~/.zshrc` | Открытие конфигурационных настроек |
| `source ~/.zshrc` | Обновление конфигурационных настроек |
| `echo $ZSH_VERSION` | Версия |
| `upgrade_oh_my_zsh` | Обновление |

## Просмотр подробной информации об аудио/видео файле (`media-info`)

> [Официальная документация](https://formulae.brew.sh/formula/media-info#default)

| Команды | Описания |
| ------- | -------- |
| `brew install mediainfo` | Установка |
| `mediainfo путь_к_файлу` | Просмотр подробной информации об аудио/видео файле |
