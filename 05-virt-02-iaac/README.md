# Домашнее задание к занятию "5.2. Применение принципов IaaC в работе с виртуальными машинами"

## Задача 1
Опишите своими словами основные преимущества применения на практике IaaC паттернов.

Преимущества IaaC:

- Скорость.Автоматизация рутинных задач, удобство, конфигурирование инфраструктуры занимает меньше времени.
- Масштабируемость. Развертывание конфигурации на большом количестве сред.
- Безопасность. Аудит безопасности можно проводить на файлах конфигурации, а не в ручную на различных системах.
- Возможность отката на предыдущую версию. В случае ошибок, файлы конфигурации хранятся в системе контроля версии, при желании возможно откатить до последней рабочей версии.
- Возможность быстрого восстановления инфраструктуры. В аварийных ситуациях не нужно тратить время на ручной разворот инфраструктуры. Это сокращает время простоя и экономит деньги для бизнеса
- Документация. Описанный код легко может понять новый сотрудник, в результате чего время адаптации уменьшается. Также описанный код делает инфраструктуру прозрачной как для команды администрирования, так и для разработчиков
- Идентичность инфраструктуры. IaaC гарантирует, что в различных средах конфигурация будет одинаковой. Это минимизирует вероятность возникновения ошибок, когда в одной среде код работает и проходит все тесты, а в другой нет.

Какой из принципов IaaC является основополагающим?

- Идемпотетность. Получаем одинаковый результат при повторных выполнениях операций.




## Задача 2
Чем Ansible выгодно отличается от других систем управление конфигурациями?

- Использование существующей инфраструктуры SSH. Нет необходимости установки дополнительных агентов.
- Легкость при описывания конфигурации, легкочитаемый файл конфигурации YAML.
- Большое количество готовых модулей, которые можно использовать из коробки. Ansible написан на Python, поэтому написание новых модулей гораздо легче, чем на других системах.

Какой, на ваш взгляд, метод работы систем конфигурации более надёжный push или pull?
- На мой взгляд наиболее надежный метод - Push. При этом методе есть централизованная точка распространения, из который можно следить за ходом выполнения доставки. Нет необходимости мониторить состояние агентов на удаленных серверах.



## Задача 3
Установить на личный компьютер:

- VirtualBox
- Vagrant
- Ansible

Приложить вывод команд установленных версий каждой из программ, оформленный в markdown.

```bash
 ~ VBoxManage -v                             
7.0.8r156879
```

```bash
~ vagrant -v                                       
Vagrant 2.3.4
```

```bash
~ ansible --version                              
ansible [core 2.14.5]
  config file = None
  configured module search path = ['/Users/admin/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/local/Cellar/ansible/7.5.0/libexec/lib/python3.11/site-packages/ansible
  ansible collection location = /Users/admin/.ansible/collections:/usr/share/ansible/collections
  executable location = /usr/local/bin/ansible
  python version = 3.11.3 (main, Apr  7 2023, 19:29:16) [Clang 14.0.0 (clang-1400.0.29.202)] (/usr/local/Cellar/ansible/7.5.0/libexec/bin/python3.11)
  jinja version = 3.1.2
  libyaml = True
```

## Задача 4
Воспроизвести практическую часть лекции самостоятельно.

- Создать виртуальную машину.
- Зайти внутрь ВМ, убедиться, что Docker установлен с помощью команды

```bash
docker ps
```

```bash
vagrant@server1:~$ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```