## Laboratory work II

Данная лабораторная работа посвещена изучению утилит для разработки проектов

## Tasks

- [ ] 1. Ознакомиться со ссылками учебного материала
- [ ] 2. Выполнить инструкцию учебного материала
- [ ] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**
 
## Tutorial

```bash
$ export GITHUB_USERNAME=<имя_пользователя>
$ export GIST_TOKEN=<сохраненный_токен>
$ alias edit=<nano|vi|vim|subl>
```

```ShellSession
$ mkdir -p ${GITHUB_USERNAME}/workspace
$ cd ${GITHUB_USERNAME}/workspace
$ pwd
$ cd ..
$ pwd
```

```ShellSession
$ mkdir -p workspace/tasks/
$ mkdir -p workspace/projects/
$ mkdir -p workspace/reports/
$ cd workspace
```

```ShellSession
# Debian
$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
$ tar -xf node-v6.11.5-linux-x64.tar.xz
$ rm -rf node-v6.11.5-linux-x64.tar.xz
$ mv node-v6.11.5-linux-x64 node
```

```ShellSession
$ ls node/bin 
$ echo ${PATH}
$ export PATH=${PATH}:`pwd`/node/bin
$ echo ${PATH}
$ mkdir scripts
$ cat > scripts/activate<<EOF
export PATH=\${PATH}:`pwd`/node/bin
EOF
$ source scripts/activate
```

```ShellSession
$ npm install -g gistup
$ ls node/bin
```

```ShellSession
$ cat > ~/.gistup.json <<EOF
{
  "token": "${GIST_TOKEN}"
}
EOF
```

## Report

```ShellSession
$ export LAB_NUMBER=02
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gistup -m "lab${LAB_NUMBER}" # enter: yes↵
```

## Links

### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix))-архиватор
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix))-выводит содержимое файлов в единый поток
- [cd](https://en.wikipedia.org/wiki/Cd_(command))-смена рабочей директории
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix))-копирование файла или каталога
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix))-выбирает нужную часть из каждой строки файла
- [echo](https://en.wikipedia.org/wiki/Echo_(command))-выводит текстовую строку в терминал
- [env](https://en.wikipedia.org/wiki/Env_(shell))-печать списка переменных среды
- [ex](https://en.wikipedia.org/wiki/Ex_(editor))-онлайн-редактор
- [file](https://en.wikipedia.org/wiki/File_(command))-отображает тип данных в файле
- [find](https://en.wikipedia.org/wiki/Find)-поиск файлов в директории
- [ls](https://en.wikipedia.org/wiki/Ls)-вывод всех каталогов и файлов текущей директории
- [man](https://en.wikipedia.org/wiki/Man_page)-отображение информации о команде и др.
- [mkdir](https://en.wikipedia.org/wiki/Mkdir)-создание нового каталога
- [mv](https://en.wikipedia.org/wiki/Mv)-перемещение файла или каталога
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix))-проверка файлов и отображение их содержимого
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix))-вывод активных процессов
- [pwd](https://en.wikipedia.org/wiki/Pwd)-отображение текущей рабочей директории
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix))-удаление файла/каталога
- [sed](https://en.wikipedia.org/wiki/Sed)-редактор потока данных для автоматического редактирования текстов
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix))-изменяет дату доступа и изменения файла

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software)) | [yum](https://fedoraproject.org/wiki/Yum/ru)- установка и управление программными пакетами
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh)-(brew-Mac,linuxbrew-Linux)-установка нужных пользователю пакетов
- [npm](https://docs.npmjs.com)-пакетный менеджер для nodejs

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details)-утилита для работы с URL страницами и передачи файлов
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf)-загружает файлы 
- [clang](https://clang.llvm.org)-компилятор
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html)-компилятор
- [make](https://en.wikipedia.org/wiki/Make_(software))-создание программ из исходного кода
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html)-открывает файл
- [openssl](https://www.openssl.org)-криптографическая библиотека
- [nano](https://www.nano-editor.org)-текстовый редактор(консольный)
- [tree](https://linux.die.net/man/1/tree)графическое представление структуры папок(в виде дерева)
- [vim](http://www.vim.org)-текстовый редактор

```
Copyright (c) 2017 Братья Вершинины
```
