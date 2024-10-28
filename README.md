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
![image](https://github.com/user-attachments/assets/976789b5-2dda-4be0-8af6-cd1e86666da0)
6. Повторите запуск playbook на окружении prod.yml. Убедитесь, что выдаются корректные значения для всех хостов.
![image](https://github.com/user-attachments/assets/60f35778-d146-4e4a-bd83-fe1220110d2f)
7. При помощи ansible-vault зашифруйте факты в group_vars/deb и group_vars/el с паролем netology.
![image](https://github.com/user-attachments/assets/b34981f2-8414-45ed-85b9-bd58d137196f)
8. Запустите playbook на окружении prod.yml. При запуске ansible должен запросить у вас пароль. Убедитесь в работоспособности.
![image](https://github.com/user-attachments/assets/6b2d1ef6-a117-44cf-aac7-6d6bae8b8180)
9. Посмотрите при помощи ansible-doc список плагинов для подключения. Выберите подходящий для работы на control node.
![image](https://github.com/user-attachments/assets/78db2b38-d4d9-4077-9ab6-98a3ff474d00)
10. В prod.yml добавьте новую группу хостов с именем local, в ней разместите localhost с необходимым типом подключения.
![image](https://github.com/user-attachments/assets/67e688f3-756f-4d07-a6ee-6444736d009a)
11. Запустите playbook на окружении prod.yml. При запуске ansible должен запросить у вас пароль. Убедитесь, что факты some_fact для каждого из хостов определены из верных group_vars.
![image](https://github.com/user-attachments/assets/796f731c-2dd6-4b13-a076-222579536bc9)
12. Заполните README.md ответами на вопросы. Сделайте git push в ветку master. В ответе отправьте ссылку на ваш открытый репозиторий с изменённым playbook и заполненным README.md.
13. Предоставьте скриншоты результатов запуска команд.
