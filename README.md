# Домашнее задание к занятию 1 «Введение в Ansible» - Скрыпников Илья
1. Попробуйте запустить playbook на окружении из test.yml, зафиксируйте значение, которое имеет факт some_fact для указанного хоста при выполнении playbook.
![image](https://github.com/user-attachments/assets/65377855-10e2-419b-8683-e2be5293b9fb)
2. Найдите файл с переменными (group_vars), в котором задаётся найденное в первом пункте значение, и поменяйте его на all default fact.
![image](https://github.com/user-attachments/assets/bbc84e41-6ab4-42b9-b4f7-45720bb0350b)
3. Воспользуйтесь подготовленным (используется docker) или создайте собственное окружение для проведения дальнейших испытаний.
sudo docker run -d -i --name ubuntu ubuntu:latest /bin/bash
sudo docker run -d -i --name centos7 centos:7 /bin/bash
4. Проведите запуск playbook на окружении из prod.yml. Зафиксируйте полученные значения some_fact для каждого из managed host.
![image](https://github.com/user-attachments/assets/2d2fb2b3-e6c8-4d7d-93ad-7540fdf05428)
5. Добавьте факты в group_vars каждой из групп хостов так, чтобы для some_fact получились значения: для deb — deb default fact, для el — el default fact.
6. Повторите запуск playbook на окружении prod.yml. Убедитесь, что выдаются корректные значения для всех хостов.
7. При помощи ansible-vault зашифруйте факты в group_vars/deb и group_vars/el с паролем netology.
8. Запустите playbook на окружении prod.yml. При запуске ansible должен запросить у вас пароль. Убедитесь в работоспособности.
9. Посмотрите при помощи ansible-doc список плагинов для подключения. Выберите подходящий для работы на control node.
10. В prod.yml добавьте новую группу хостов с именем local, в ней разместите localhost с необходимым типом подключения.
11. Запустите playbook на окружении prod.yml. При запуске ansible должен запросить у вас пароль. Убедитесь, что факты some_fact для каждого из хостов определены из верных group_vars.
12. Заполните README.md ответами на вопросы. Сделайте git push в ветку master. В ответе отправьте ссылку на ваш открытый репозиторий с изменённым playbook и заполненным README.md.
13. Предоставьте скриншоты результатов запуска команд.
