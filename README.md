# nomamap

## Инициализация карты
nomamap.init(Object)
### Параметры объекта:
mapId (string): ID HTML-элемента для отображения карты.
apiKey (string): API-ключ для Google Maps.
apiMapId (string): ID карты Google API.
mapCenter (Object): Координаты для центровки карты. Формат: { lng: Number, lat: Number }.
zoom (Number): Уровень зума при загрузке карты.
fontFamily (string): Шрифт для текста в маркере кластера.
fontWeight (string | number): Толщина шрифта для текста в маркере кластера.
### Пример использования:
nomamap.init({
  mapId: 'map',
  apiKey: 'YOUR_GOOGLE_MAPS_API_KEY',
  apiMapId: 'YOUR_MAP_ID',
  mapCenter: { lng: -80.243307, lat: 25.882813 },
  zoom: 12,
  fontFamily: 'Arial',
  fontWeight: 'bold'
});



## Добавление маркеров на карту
nomamap.setMarkers(Array, Object)
### Параметры:
Array: Массив объектов с координатами и названиями маркеров. Формат: { lng: Number, lat: Number, name: String }.
Object (необязательный): Координаты для пина карты на заданное место. Формат: { lng: Number, lat: Number }.
### Пример использования:
nomamap.setMarkers([
  { lng: -80.306441, lat: 25.875859, name: 'Marker 1' },
  { lng: -80.283287, lat: 25.885322, name: 'Marker 2' }
], {
  lat: 25.882813,
  lng: -80.243307
});



## Переход к координатам
nomamap.mapPanTo(Object)
### Параметры:
Object: Объект с координатами для перемещения карты. Формат: { lng: Number, lat: Number }.
### Пример использования:
nomamap.mapPanTo({ lng: -80.243307, lat: 25.882813 });



## Уничтожение карты
nomamap.destroy()
Очищает карту, удаляет все маркеры и кластеры.



