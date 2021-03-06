# Зависимости

Для генерации сообщений используется утилита zcm-gen входящая в состав ZCM. <br/>
Подробная инструкция описана [здесь][zcm]. <br/>
Для сборки генератора zcm-gen необходим только python >= 2.7 <br/>
```sh
$ git clone https://github.com/ZeroCM/zcm
$ cd zcm
$ ./waf configure
$ ./waf build
$ sudo ./waf install
```

Для генерации документации используется [Doxyden][dx] версии 1.8.15.

# zcm_gen.sh
Скрипт находит все zcm файлы, если они изменились перегенерирует С и С++ код и собирает динамическую библиотеку,
которая используется утилитами ZCM.

# doxy_gen.sh
Скрипт находит все zcm файлы и генерирует документацию в формате doxygen.<br/>
Doxyfile.config - файл конфигурации doxygen.<br/>
Документация генерируется для zcm файлов, синтаксис которых похож на C, с тем отличием что при описании структуры после закрывающей скобки '}' не ставится ';'. Для корректной генерации документации скрипт doxy_gen.sh добавляет ';' перед созданием документации и удаляет после.

Правила именования структур и пример оформления комментариев описаны [здесь][rl]


   [zcm]: <https://vniias.atlassian.net/wiki/spaces/ShareDoc/pages/321847297/ZeroCM>
   [dx]: <https://www.stack.nl/~dimitri/doxygen/manual/starting.html>
   [rl]:<https://vniias.atlassian.net/wiki/spaces/ShareDoc/pages/325419031/->


