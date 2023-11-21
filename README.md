# TOIB-PR4-Kuzina-Anastasia-Sergeevna-BBMO-02-23

1. Создадим 2 виртуальные машины на базе ОС Debian 12 и обеспечим между ними сетевой обмен посредством сетевого моста

   ![image](Screenshots/1.png)

   ![image](Screenshots/2.png)

   ![image](Screenshots/3.png)
   
2. Включим на 1-ой (сервере) ВМ передачу логов по протоколу rsyslog на 2-ую ВМ (клиент)
   
   **2.1 Устанавим и настраим rsyslog на сервере и клиенте**

   ![image](Screenshots/4.png)

   **2.2 Проверим работоспособность rsyslog на сервере и клиенте**

   ![image](Screenshots/5.png)

   **2.3 Включим UDP и TCP соединения**

   ![image](Screenshots/6.png)

   **2.4 Установим правила на сервере**
   
   ![image](Screenshots/7.png)

   **2.5 Установим правила на клиенте**
   
   ![image](Screenshots/8.png)

   **2.6 Проверим получения логов на сервере**
   
   ![image](Screenshots/9.png)

   ![image](Screenshots/10.png)

3. Установим и настроим получение логов на сервер с использованием Loki
   
   **3.1 Установим и отредактируем docker compose файл на сервере**
 
   ![image](Screenshots/11.png)
   
   ![image](Screenshots/12.png)
   
   **3.2 Запустим Loki**
 
   ![image](Screenshots/13.png)
 
   **3.3 Отредактируем promtail-config на клиенте**
 
   ![image](Screenshots/14.png)

   **3.4 Отредактируем docker compose файл для promtail**
 
   ![image](Screenshots/15.png)
  
   **3.5 Запустим promtail на клиенте**
 
   ![image](Screenshots/16.png)

   **3.6 Просмотрим логи клиента в Grafana**
 
   ![image](Screenshots/17.png)

   ![image](Screenshots/18.png)
 
 4. Установим и настроим получение логов на сервере с использованием Signoz

   _Установка Signoz по инструкции с сайта: https://signoz.io/docs/install/docker/#install-signoz-using-docker-compose_

   **4.1 Запустим Signoz**
   
   ![image](Screenshots/19.png)
   
   ![image](Screenshots/20.png)
   
   ![image](Screenshots/21.png)
   
   **4.2 Отредактируем конфигурации на клиенте для отправки данных в Signoz**
   
   _Устнаовка приложения sample-nodejs-app согласно инструкции с сайта: https://github.com/SigNoz/sample-nodejs-app/_
   
   ![image](Screenshots/22.png)

   **4.3 Запустим клиентское приложение sample-nodejs-app**
   
   ![image](Screenshots/23.png)
   
   **4.4 Проверим получение логов в Signoz**
   
   ![image](Screenshots/24.png)
   
   ![image](Screenshots/25.png)
