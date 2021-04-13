---
title: Отключение поддержки 32-разрядных Linux
author: felixrieseberg
date: '2019-03-04'
---

Команда Electron прекратит поддержку 32-разрядных Linux (ia32 / i386), начиная с Electron v4.0. Последней версией Electron, поддерживающей 32-битные установки Linux, является Electron v3.1, которая будет получать поддержку до выхода Electron v6. Поддержка 64-битных Linux и `armv7l` будет продолжена без изменений.

---

## Что именно Electron больше не поддерживает?

Возможно, вы видели описание "64-бит" и "32-бит" в качестве стикеров на вашем компьютере или в качестве опции скачивания программного обеспечения. Термин используется для описания конкретной компьютерной архитектуры. Большинство компьютеров, сделанных в 1990-е и начале 2000-х годов, были созданы с использованием процессоров, основанных на 32-разрядной архитектуре, В то время как большинство компьютеров, сделанных позже, были основаны на новой и более мощной 64-битной архитектуре. Nintendo 64 (получится? и PlayStation 2 были первыми широко доступными потребительскими устройствами с новой архитектурой, компьютеры продавались после 2010 года содержали почти исключительно 64-битные процессоры. В результате была уменьшена поддержка: Google перестал выпускать Chrome для 32-битных Linux в марте 2016 года, Canonical перестал предоставлять 32-битные изображения для рабочего стола в 2017 году и не поддерживает 32-битную версию с Ubuntu 18.10. Arch Linux, elementary OS и другие известные дистрибутивы Linux уже прекратили поддержку архитектуры старения процессоров.

До сих пор Electron предоставлял и поддерживал сборки, которые запускаются на старой 32-битной архитектуре. После выхода версии 4.0 команда Electron больше не сможет предоставлять бинарные файлы или поддерживать 32-разрядную версию Linux.

Electron всегда был активным проектом с открытым исходным кодом, и мы продолжаем поддерживать и поощрять разработчиков, заинтересованных в построении Electron для экзотических архитектур.

## Что это значит для разработчиков?

Если вы в настоящее время не предоставляете 32-разрядных дистрибутивов вашего приложения для Linux, никаких действий не требуется.

Проекты, поставляющие 32-разрядные приложения Linux Electron, должны решить, как их продолжить. 32-битный Linux будет поддерживаться на Electron 3 [до](https://electronjs.org/docs/tutorial/support#supported-versions) выпуска Electron 6, что дает некоторое время для принятия решений и планов.

## Что это значит для пользователей?

Если вы являетесь пользователем Linux и не уверены в том, что вы используете 64-разрядную систему, скорее всего вы запускаете на 64-битной архитектуре. Чтобы убедиться, вы можете запустить команды `lscpu` или `uname -m` в терминале. Кто-то будет распечатать вашу текущую архитектуру.

Если вы используете Linux на 32-разрядном процессоре, то вы, скорее всего, столкнулись с трудностями при поиске недавно выпущенного программного обеспечения для вашей операционной системы. Команда Electron присоединяется к другим выдающимся членам сообщества Linux, рекомендовав вам перейти на 64-битную архитектуру.