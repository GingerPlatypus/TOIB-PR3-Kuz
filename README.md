# TOIB-PR4-Kuzina-Anastasia-Sergeevna-BBMO-02-23

1. Создадим 2 виртуальные машины на базе ОС Debian 12 и обеспечим между ними сетевой обмен посредством сетевого моста

   ![image](Screenshots/1.png)

   ![image](Screenshots/2.png)

   ![image](Screenshots/3.png)
   
2. Включим на 1-ой (сервере) ВМ передачу логов по протоколу rsyslog на 2-ую ВМ (клиент)
   
   **Устанавим и настраим rsyslog на сервере и клиенте**

   ![image](Screenshots/4.png)

   **Проверим работоспособность rsyslog на сервере и клиенте**

   ![image](Screenshots/5.png)

   **Включим UDP и TCP соединения**

   ![image](Screenshots/6.png)

   **Устанавливим правила на сервере**
   
   ![image](Screenshots/7.png)

   **Установливим правила на клиенте**
   
   ![image](Screenshots/8.png)

   **Проверим получения логов на сервере**
   
   ![image](Screenshots/9.png)

   ![image](Screenshots/10.png)

4. Установим и настроим получение логов на сервер с использованием Loki
   
   **Установим и отредактируем docker compose файл на сервере**
 
   ![image](Screenshots/11.png)
   
   ![image](Screenshots/12.png)
   
   **Запустим Loki**
 
   ![image](Screenshots/13.png)
 
   **Отредактируем promtail-config на клиенте**
 
   ![image](Screenshots/14.png)

   **Отредактируем docker compose файл для promtail**
 
   ![image](Screenshots/15.png)
  
   **Запустим promtail на клиенте**
 
   ![image](Screenshots/16.png)

   **Просматрим логи клиента в Grafana**
 
   ![image](Screenshots/17.png)

   ![image](Screenshots/18.png)
 
 5. Устанавливим и настроим получение логов на сервере с использованием Signoz

   _Установка Signoz по инструкции с сайта: https://signoz.io/docs/install/docker/#install-signoz-using-docker-compose_

   **Запустим Signoz**
   
   ![image](Screenshots/19.png)
   
   ![image](Screenshots/20.png)
   
   ![image](Screenshots/21.png)
   
   **Отредактируем конфигурации на клиенте для отправки данных в Signoz**
   
   _Устнаовка приложения sample-nodejs-app согласно инструкции с сайта: https://github.com/SigNoz/sample-nodejs-app/_
   
   ![image](Screenshots/22.png)

   **Запустим клиентское приложение sample-nodejs-app**
   
   ![image](Screenshots/23.png)
   
   **Проверим получение логов в Signoz**
   
   ![image](Screenshots/24.png)
   
   ![image](Screenshots/25.png)
