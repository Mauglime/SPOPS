# SPOPS
Smart Predictive Охрано-Пожарная Система — это открытая аппаратно-программная экосистема безопасности нового поколения. Проект переводит индустрию пультовой охраны от реактивного контроля («констатация обрыва») к предиктивному анализу трендов физических параметров с помощью распределенного ИИ.


# 🛡️ SPOPS — Smart Predictive Open-Source Security System

[![License: GPL v3](https://shields.io)](https://gnu.org)
[![License: AGPL v3](https://shields.io)](https://gnu.org)
[![Open Source](https://shields.io)]()
[![AI Powered](https://shields.io)]()

[🇬🇧 English](#-english) | [🇷🇺 Русский](#-русский)

---

## 🇬🇧 English

### 💡 What is SPOPS?
**SPOPS (Smart Predictive OPS)** is a next-generation open-source hardware and software security ecosystem. Traditional alarm systems are reactive and "blind" — they only trigger when a wire snaps or a sensor fails completely, forcing technicians to spend hours troubleshooting loops with a multimeter.

SPOPS changes the paradigm to **Predictive Maintenance**:
* **No SaaS, No Subscriptions, No Vendor Lock-in:** All software is 100% free and open-source forever.
* **AI-Driven Diagnostics:** High-speed ADCs continuously digitize the physical state of wire loops (exact Ohms, capacitance, high-frequency noise). Cloud AI detects wire oxidation, moisture, or even pests on warm PCBs weeks before a failure occurs.
* **Hybrid Fast-Deploy Sensors:** Deploy 1,500+ sites in days via wireless (LiFePO4 battery), then gradually wire them with copper. The wireless channel automatically switches to a **hot standby** (<50ms failover).
* **Mass-Market Silicon:** Built around affordable 8-core mobile SoCs (**MediaTek Helio**) paired with a heavily armored industrial Carrier Board (GDT surge arresters, TVS diodes, self-resetting PTC fuses).

### 🏗 System Architecture (Hub & Spoke)

```text
  [ Central AI Brain (API) ]  <--- Anonymized anomaly patterns --->  [ Client On-Premise Server (Docker) ]
                                                                                     ▲
                                                                          (MQTT / TLS / LTE)
                                                                                     ▼
  [ Hybrid UID Sensors ]  <--- 868MHz Radio + Addressable Bus --->  [ SPOPS Control Panel (MediaTek + ADC) ]
```

### 🤝 Looking for Contributors!
We are building the "Linux of the Security Industry" and looking for passionate developers to join our core open-source team:
1. **Embedded Linux Engineers:** Building lightweight Yocto/Buildroot images for MediaTek SoMs and writing C/C++ daemons for high-speed ADC data collection and edge filtering.
2. **AI / Data Science Engineers:** Training time-series anomaly detection models (Python/PyTorch) to separate natural temperature shifts from terminal oxidation and electrical noise.
3. **Backend & Frontend Developers:** Expanding our Dockerized On-Premise server (AGPLv3) and building an intuitive mobile UI for field technicians.

### 📜 Licensing & Patent Pledge
* **Device Firmware:** Licensed under **GNU GPLv3**.
* **Server Software:** Licensed under **GNU AGPLv3**.
* **Patent Pledge (Tesla Model):** Core hardware and predictive diagnostic methods are patent-pending to protect the community from patent trolls. We pledge never to assert our patents against anyone using, modifying, or distributing SPOPS within the open-source ecosystem.

---

## 🇷🇺 Русский

### 💡 Что такое SPOPS?
**SPOPS (Smart Predictive Охрано-Пожарная Система)** — это открытая аппаратно-программная экосистема безопасности нового тысячелетия. Классические ОПС слепы и реактивны: они молчат до последнего, а при обрыве заставляют техника часами ползать со стремянкой и мультиметром, прозванивая глухие шлейфы.

SPOPS переводит индустрию в эпоху **предиктивной аналитики**:
* **Никаких подписок и платных лицензий:** Весь софт полностью открыт и бесплатен навсегда.
* **ИИ вместо мультиметра:** Высокоскоростные АЦП непрерывно оцифровывают физику шлейфов (точные Омы, емкость, ВЧ-шумы). Облачный ИИ вычисляет окисление скруток, конденсат и даже нашествие тараканов на теплые платы за недели до реальной аварии.
* **Гибридный экспресс-монтаж:** Объекты сдаются за час по радиоканалу (на АКБ LiFePO4), а затем планово «окукливаются» медью. Радиоканал уходит в **горячий резерв** и подхватывает связь за <50 мс при перебитии кабеля. Каждый датчик имеет уникальный цифровой ID.
* **Доступное и неубиваемое железо:** В качестве ядра используются массовые 8-ядерные чипы **MediaTek Helio**, установленные на нашу бронированную материнскую плату (газоразрядники GDT, TVS-диоды, самовосстанавливающиеся PTC-предохранители).

### 🏗 Архитектура системы (Мозг и Узлы)

```text
  [ Центральный ИИ-Мозг (API) ] <--- Обезличенные слепки аномалий ---> [ Сервер ЧОПа / Клиента (Docker) ]
                                                                                     ▲
                                                                          (MQTT / TLS / LTE)
                                                                                     ▼
  [ Гибридные ID-датчики ]    <--- Радио 868 МГц + Адресная шина ---> [ Прибор SPOPS (MediaTek + АЦП) ]
```

### 🤝 Присоединяйтесь к разработке!
Мы создаем «Linux в мире систем безопасности» и ищем единомышленников в команду Open Source:
1. **Embedded Linux разработчики:** Сборка легких образов (Yocto / Buildroot) под модули MediaTek, написание демонов опроса АЦП и сжатия телеметрии на краю (Edge Pre-processing).
2. **ML / Data Science инженеры:** Обучение моделей анализа временных рядов (Python) для отсечения суточных температурных колебаний и точной классификации неисправностей.
3. **Fullstack / Mobile разработчики:** Развитие серверной части (Docker, AGPLv3) и создание удобного приложения для техников с интерактивной картой объектов.

### 📜 Лицензии и Патентная защита
* **Прошивка прибора:** Распространяется под копилефтной лицензией **GNU GPLv3**.
* **Серверное ПО:** Распространяется под лицензией **GNU AGPLv3** (запрещает закрывать облачные доработки кода).
* **Патентное соглашение (Модель Tesla):** Ключевые инженерные решения защищаются патентами для защиты сообщества от патентных троллей. Правообладатель гарантирует свободное и бесплатное использование патентов для всех участников открытой экосистемы SPOPS.

