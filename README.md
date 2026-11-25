<div align="center">

# ⚡ ZapretBridge

**Единая панель для Windows: Flowseal Zapret + AmneziaWG / WARP + VLESS + Steer + Hosts / DoH**

[![Version](https://img.shields.io/badge/Версия-v1.0.2-2D5BFF?style=for-the-badge)](https://github.com/sakleam1414/ZapretBridge/releases)
[![Platform](https://img.shields.io/badge/Windows-10%20%2F%2011%20(x64)-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/sakleam1414/ZapretBridge)
[![Flowseal](https://img.shields.io/badge/Zapret%20Flowseal-v1.10.4-10B981?style=for-the-badge)](https://github.com/sakleam1414/ZapretBridge)

<br/>

[![Скачать установщик](https://img.shields.io/badge/⬇_Скачать_установщик-ZapretBridge__Setup.exe-2563EB?style=for-the-badge)](https://github.com/sakleam1414/ZapretBridge/releases/latest/download/ZapretBridge_Setup.exe)
[![Скачать обновление](https://img.shields.io/badge/📦_Portable_%2F_Обновление-ZapretBridge.exe-10B981?style=for-the-badge)](https://github.com/sakleam1414/ZapretBridge/releases/latest/download/ZapretBridge.exe)
[![Релизы](https://img.shields.io/badge/🚀_GitHub_Releases-v1.0.2-6B38FF?style=for-the-badge)](https://github.com/sakleam1414/ZapretBridge/releases)

</div>

---

## ✨ Возможности ZapretBridge

| Раздел | Что умеет |
| :--- | :--- |
| 🛡️ **Zapret (Flowseal v1.10.4)** | Встроенные 22 официальные стратегии, `GameFilter`, `IPSet Filter`, `TCP Timestamps`, диагностика системы и автотест стратегий. |
| 🌀 **AmneziaWG и WARP** | Безопасная активация (**Закрыто → Установка → Проверка 4/4 → Открыто**), генератор бесплатного Cloudflare WARP и импорт `.conf`. |
| ⚡ **VLESS и Подписки** | Поддержка `vless://`, `trojan://`, `hysteria2://`, `ss://`, `vmess://`, подписки и автовыбор самого быстрого сервера. |
| 🔀 **Steer (Раздельная маршрутизация)** | Умный выбор сайтов и программ (`.exe`), которые пойдут через туннель, и исключений, идущих напрямую. |
| 📶 **Монитор сети («Кто жрёт интернет»)** | Скорость по программам в реальном времени (ETW TCP+UDP), категории **Яндекс / Браузеры**, **Игры**, **Общение**, **Загрузки**. |
| 🌐 **Hosts и DoH** | Быстрые наборы для `hosts` (`GeoHide EU/US`, `malw.link`) и шифрованный DNS (DoH). |
| 🎨 **Оформление и Сервис** | 15 тем оформления, живой фон, размытие IP/ключей для скриншотов и бэкапы `.zmb`. |

---

## 🌀 Порядок запуска AmneziaWG

```mermaid
flowchart LR
    A["🔒 1. Закрыто<br/>WARP и туннели заблокированы"] --> B["⬇ 2. Установка AmneziaWG<br/>Загрузка и распаковка клиента"]
    B --> C{"🔍 3. Проверка 4/4<br/>amneziawg.exe · awg.exe --version<br/>tunnel.dll / wintun.dll · Права Админа"}
    C -- "Ошибка проверки" --> A
    C -- "Проверка успешна" --> D["🔓 4. Открыто<br/>Генератор WARP, .conf и туннели"]
```

---

## 📦 Файлы и установка (v1.0.2)

| Файл | Назначение |
| :--- | :--- |
| **[`ZapretBridge_Setup.exe`](https://github.com/sakleam1414/ZapretBridge/releases/latest/download/ZapretBridge_Setup.exe)** | Полноценный установщик для Windows **v1.0.2** (ярлыки, автозапуск, загрузка `sing-box`, удаление). |
| **[`ZapretBridge.exe`](https://github.com/sakleam1414/ZapretBridge/releases/latest/download/ZapretBridge.exe)** | Актуальная версия **v1.0.2** (портативный запуск или автообновление). |

### Что нового в v1.0.2
- В **Мониторе сети** внизу добавлен блок **«Кто жрёт интернет»**: показывает потребление трафика программами (Яндекс Браузер, игры, Steam, Discord, Telegram и др.) с фильтром по категориям.
- Включён точный замер **TCP + UDP** по процессам через Windows ETW (при правах Администратора) и резервный режим по сокетам/Steer.
