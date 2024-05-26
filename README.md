# Тесты на проверку параметра firstName при создании пользователя в Яндекс.Прилавок с помощью API Яндекс.Прилавок.
- Для запуска тестов должны быть установлены пакеты pytest и requests
- Запуск всех тестов выполянется командой pytest

1.SELECT c.login, COUNT(o.id) AS "deliveryCount"
FROM "Couriers" AS c
LEFT JOIN "Orders" AS o ON c.id = o."courierId"
WHERE o."inDelivery" = TRUE
GROUP BY c.login;

2.
SELECT 
    track, 
    CASE 
        WHEN finished = true THEN 2 
        WHEN cancelled = true THEN -1 
        WHEN "inDelivery" = true THEN 1 
        ELSE 0 
    END AS status 
FROM "Orders";
