# AutoLogger-C3 ⚡

[🇩🇪 Deutsch](#-deutsch) | [🇺🇦 Українська](#-українська) | [🇬🇧 English](#-english) | [🇷🇺 Русский](#-русский)

A wireless battery voltage and leakage current logger based on ESP32-C3 with a non-invasive split-core current transformer (PZCT-02).

![Hardware Schematic](schematic.jpg) *(Replace with actual image path if needed)*

---

## 🇩🇪 Deutsch

### AutoLogger-C3
Kabelloser Datenlogger für Batteriespannung und Leckstrom basierend auf dem ESP32-C3. Das Gerät misst Ströme über einen berührungslosen Klappstromwandler (PZCT-02) und speichert die Daten in einem externen EEPROM, sodass Langzeitmessungen ohne ständige PC-Verbindung möglich sind.

### ✨ Funktionen
* **Berührungslose Strommessung:** Nutzt den PZCT-02 (100A/100mA) Transformator. Keine Kabel müssen durchtrennt werden!
* **Offline-Protokollierung:** Speichert Messwerte (Spannung, Strom, Uptime) in einem Ringpuffer auf dem EEPROM (z.B. 24C256).
* **Modernes Web-Interface:** Eingebautes Oszilloskop (Dark UI) zur Echtzeitüberwachung, interaktiver Zoom (X/Y) und Touch-Unterstützung.
* **CSV-Export:** Laden Sie aufgezeichnete Daten direkt über das Web-Interface herunter.
* **OLED-Display (128x32):** Drei Anzeigemodi (Normal, Große Spannung, Großer Strom), umschaltbar über die BOOT-Taste (GPIO9).
* **Nullkalibrierung:** Einfache Software-Kalibrierung für den Stromsensor.

### 🛠️ Hardware-Komponenten
* **Mikrocontroller:** ESP32-C3 MINI
* **Stromsensor:** PEACEFAIR PZCT-02 Split Current Transformer
* **ICs:** DRV8870 (Motortreiber), MAX999 (Komparator)
* **Speicher:** EEPROM 24Cxx (automatische Erkennung bis 64 KB, z.B. 24C256)
* **Display:** SSD1306 OLED 128x32 (I2C)
* **Spannungsmessung:** Spannungsteiler (470k / 100k) an GPIO1

### 🚀 Verwendung
1. Schalten Sie das Gerät ein.
2. Verbinden Sie sich mit dem WLAN-Access-Point:
   * **SSID:** `AutoLogger-C3`
   * **Passwort:** `12345678`
3. Öffnen Sie den Browser und navigieren Sie zu `http://192.168.4.1` (oder die entsprechende IP-Adresse).
4. Starten Sie die Aufzeichnung oder beobachten Sie die Live-Daten.

---

## 🇺🇦 Українська

### AutoLogger-C3
Бездротовий логер напруги та струму витоку акумуляторної батареї (АКБ) на базі ESP32-C3. Пристрій вимірює струми за допомогою безконтактного роз'ємного трансформатора струму (PZCT-02) і зберігає дані в зовнішній пам'яті EEPROM, що дозволяє проводити тривалі вимірювання без підключення до ПК.

### ✨ Основні можливості
* **Безконтактне вимірювання:** Використовує кліщі PZCT-02 (100A/100mA). Не потрібно розривати коло!
* **Автономний запис:** Збереження логів (напруга, струм, час) у кільцевий буфер EEPROM (напр. 24C256).
* **Сучасний Web-інтерфейс:** Вбудований осцилограф (Dark UI) для моніторингу в реальному часі, інтерактивний зум (X/Y) та підтримка сенсорних екранів.
* **Експорт у CSV:** Завантаження записаних даних безпосередньо через браузер.
* **OLED-дисплей (128x32):** Три режими відображення (Звичайний, Великий шрифт V, Великий шрифт I), перемикання кнопкою BOOT (GPIO9).
* **Калібрування нуля:** Просте програмне калібрування датчика струму.

### 🛠️ Апаратні компоненти
* **Мікроконтролер:** ESP32-C3 MINI
* **Датчик струму:** PEACEFAIR PZCT-02
* **Мікросхеми:** DRV8870 (драйвер), MAX999 (компаратор)
* **Пам'ять:** EEPROM 24Cxx (автовизначення об'єму, напр. 24C256)
* **Дисплей:** SSD1306 OLED 128x32 (I2C)
* **Вимірювання напруги:** Дільник напруги (470k / 100k) на GPIO1

### 🚀 Як використовувати
1. Увімкніть живлення пристрою.
2. Підключіться до точки доступу Wi-Fi:
   * **SSID:** `AutoLogger-C3`
   * **Пароль:** `12345678`
3. Відкрийте браузер і перейдіть за адресою `http://192.168.4.1` (або IP-адресою, виданою маршрутизатором, якщо змінено).
4. Керуйте логером через веб-інтерфейс.

---

## 🇬🇧 English

### AutoLogger-C3
A wireless battery voltage and leakage current data logger based on the ESP32-C3. The device measures currents using a non-invasive split-core current transformer (PZCT-02) and saves the data to external EEPROM, allowing for long-term monitoring without a permanent PC connection.

### ✨ Features
* **Non-invasive measurement:** Uses the PZCT-02 (100A/100mA) split-core transformer. No need to cut or modify existing wiring!
* **Standalone Logging:** Stores readings (voltage, current, uptime) in a circular buffer on the I2C EEPROM (e.g., 24C256).
* **Modern Web UI:** Built-in oscilloscope web interface (Dark Theme) for real-time monitoring, interactive zooming (X/Y), and touch gesture support.
* **CSV Export:** Download recorded logs directly via the web interface.
* **OLED Display (128x32):** Three view modes (Normal, Large V, Large I), toggled via the physical BOOT button (GPIO9).
* **Zero Calibration:** Easy software zero-offset calibration for the current sensor.

### 🛠️ Hardware Components
* **MCU:** ESP32-C3 MINI
* **Current Sensor:** PEACEFAIR PZCT-02 Split Current Transformer
* **ICs:** DRV8870 (motor driver), MAX999 (high-speed comparator)
* **Storage:** EEPROM 24Cxx (auto-detects size up to 64KB, e.g., 24C256)
* **Display:** SSD1306 OLED 128x32 (I2C)
* **Voltage Sensing:** Voltage divider (470k / 100k) on GPIO1

### 🚀 Usage
1. Power on the device.
2. Connect to the Wi-Fi Access Point:
   * **SSID:** `AutoLogger-C3`
   * **Password:** `12345678`
3. Open your web browser and go to `http://192.168.4.1`.
4. Use the interface to start logging or view live data.

---

## 🇷🇺 Русский

### AutoLogger-C3
Беспроводной логгер напряжения и тока утечки автомобильной (и не только) АКБ на базе ESP32-C3. Устройство измеряет ток с помощью бесконтактного разъемного трансформатора тока (PZCT-02) и сохраняет данные во внешнюю EEPROM память, что позволяет вести длительную запись без подключения к ПК.

### ✨ Основные возможности
* **Бесконтактное измерение:** Используется трансформатор-клипса PZCT-02 (100A/100mA). Не нужно разрезать провода!
* **Автономная запись:** Сохранение логов (напряжение, ток, время) в кольцевой буфер EEPROM (напр. 24C256).
* **Современный Web-интерфейс:** Встроенный осциллограф (Dark UI) для мониторинга в реальном времени, интерактивный зум (X/Y) и поддержка сенсорного управления.
* **Экспорт в CSV:** Скачивание накопленного лога напрямую через браузер.
* **OLED-дисплей (128x32):** Три режима отображения (Обычный, Крупно V, Крупно I), переключаются кнопкой BOOT (GPIO9).
* **Калибровка ноля:** Простая программная калибровка смещения (нуля) датчика тока.

### 🛠️ Аппаратные компоненты
* **Микроконтроллер:** ESP32-C3 MINI
* **Датчик тока:** PEACEFAIR PZCT-02
* **Микросхемы:** DRV8870 (драйвер катушки), MAX999 (компаратор)
* **Память:** EEPROM 24Cxx (автоопределение размера, напр. 24C256)
* **Дисплей:** SSD1306 OLED 128x32 (I2C)
* **Измерение напряжения:** Делитель напряжения (470k / 100k) на GPIO1

### 🚀 Использование
1. Подайте питание на устройство.
2. Подключитесь к Wi-Fi точке доступа:
   * **SSID:** `AutoLogger-C3`
   * **Пароль:** `12345678`
3. Откройте браузер и перейдите по адресу `http://192.168.4.1`.
4. Начните запись лога или наблюдайте за графиками в реальном времени.