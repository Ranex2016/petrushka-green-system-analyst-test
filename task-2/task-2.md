# Задание 2: Проектирование API

### 1)	Запрос GET
GET https://api.petrushka-green.ru/api/v1/partners

### 2)	Пример ответа REST API

```json
{
	"status": "success",
	"partners": [
		{
			"id": 1,
			"name": "METRO",
			"logo_url": "https://petrushka-green.ru/logos/metro.png",
			"title": "Ближайшая доставка",
			"description": "сегодня 21:00-23:00",
			"external_url": "https://metro-cc.ru",
			"is_active": true,
			"display_order": 1
		},
		{
			"id": 2,
			"name": "Ашан",
			"logo_url": "https://petrushka-green.ru/logos/auchan.png",
			"title": "Ближайшая доставка",
			"description": "сегодня 18:00-20:00",
			"external_url": "https://auchan.ru",
			"is_active": true,
			"display_order": 2
		},
		{
			"id": 3,
			"name": "ВкусВилл",
			"logo_url": "https://petrushka-green.ru/logos/vkusvill.png",
			"title": "Быстрая доставка",
			"description": "от 20 до 60 мин",
			"external_url": "https://vkusvill.ru",
			"is_active": true,
			"display_order": 3
		},
		{
			"id": 4,
			"name": "ВИКТОРИЯ",
			"logo_url": "https://petrushka-green.ru/logos/victoria.png",
			"title": "Ближайшая доставка",
			"description": "сегодня 17:00-19:00",
			"external_url": "https://victoria-group.ru",
			"is_active": true,
			"display_order": 4
		}
	]
}
```
Если сервер не сможет вернуть список партнеров, то лучше всего добавить обработку оши-бок:
```json
{
	"status": "error",
	"error_code": "PARTNERS_NOT_FOUND",
	"message": "Список партнеров временно недоступен"
}
```
