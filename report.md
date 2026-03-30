# Звіт: Визначення рівнів переносимості програмних систем

## Етап 1. Аналіз продуктів

### 1. Telegram
**Платформи:** Android (+), iOS (+), Web (+), Windows (+), macOS (+)  
**Тип:** нативний + частково крос-платформний  
**Backend:** більшість логіки на сервері (повідомлення, синхронізація)

### 2. Spotify
**Платформи:** Android (+), iOS (+), Web (+), Windows (+), macOS (+), Smart TV (+)  
**Тип:** крос-платформний + нативні елементи  
**Backend:** рекомендації, обробка музики — на сервері

### 3. Gmail
**Платформи:** Web (+), Android (+), iOS (+)  
**Тип:** веб + мобільні клієнти  
**Backend:** майже вся логіка на сервері (email, фільтри)

### 4. Uber
**Платформи:** Android (+), iOS (+), Web (+)  
**Тип:** нативний + web  
**Backend:** ключова логіка (пошук водія, маршрути) на сервері

### 5. Netflix
**Платформи:** Android (+), iOS (+), Web (+), Smart TV (+), Windows (+)  
**Тип:** крос-платформний  
**Backend:** стрімінг, рекомендації — на сервері

## Етап 2. Рівень переносимості

- **Telegram** → Рівень 2 (Shared architecture)  
- **Spotify** → Рівень 3 (Shared core logic)  
- **Gmail** → Рівень 5 (Web portability)  
- **Uber** → Рівень 2 (Shared architecture)  
- **Netflix** → Рівень 2–3 (мікс)

## Етап 3. Shared компоненти

- Backend логіка  
- Обробка даних  
- Авторизація  
- Синхронізація  
- Алгоритми рекомендацій (Spotify, Netflix)

## Етап 4. Platform компоненти

- UI (інтерфейс)  
- Push-повідомлення  
- Інтеграція з ОС  
- Робота з камерою, GPS, аудіо  

## Етап 5. Порівняльна таблиця

| Продукт   | Платформи                  | Рівень переносимості     | Shared компоненти                  | Platform компоненти        |
|----------|---------------------------|--------------------------|-----------------------------------|----------------------------|
| Telegram | Mobile, Web, Desktop      | Shared architecture      | messaging, backend                | UI, notifications          |
| Spotify  | Mobile, Web, Desktop, TV  | Shared core logic        | recommendations, backend          | audio, UI                  |
| Gmail    | Web, Mobile               | Web portability          | email processing                  | mobile UI                  |
| Uber     | Mobile, Web               | Shared architecture      | ride matching, backend            | maps, GPS                  |
| Netflix  | Mobile, TV, Web           | Shared architecture/core | streaming, recommendations        | player UI                  |

## Етап 6. Висновки

1. **Які продукти мають найвищий рівень переносимості?**  
Gmail, бо веб-застосунок працює у будь-якому браузері.

2. **Які частини залишаються платформними?**  
UI, push-повідомлення, інтеграція з пристроєм (камера, GPS, звук).

3. **Роль backend архітектури**  
Backend забезпечує основну логіку і дозволяє використовувати один функціонал на всіх платформах.

4. **Чому комбінують підходи?**  
Щоб отримати баланс між переносимістю, продуктивністю та доступом до можливостей пристрою.
