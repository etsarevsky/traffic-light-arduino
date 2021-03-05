# traffic-light-arduino

//Evgeny Tsarevsky - Traffic Light

//Определяем на каких пинах находятся реле
#define RELAY_1 7
#define RELAY_2 6
#define RELAY_3 5
#define SENSOR_VCC 2
#define SENSOR_OUT 3 
 
void setup() {
  // Конфигурируем нужные пины на выход
  for (int i = 5; i <= 7; ++i)
  {
    pinMode(i, OUTPUT);
  }
}
 
void loop() {
 
  //Включаем реле 1 на N секунд
  digitalWrite(RELAY_1, HIGH);
  delay(1000);
  //Отключаем реле 1
  digitalWrite(RELAY_1, LOW);
 
  //через секунду включаем реле 2 на N секунд
  delay(500);
 
  digitalWrite(RELAY_2, HIGH);
  delay(1000);
  digitalWrite(RELAY_2, LOW);
 
  //Повторим с оставшимися реле то же самое
  delay(500);
 
  digitalWrite(RELAY_3, HIGH);
  delay(1000);
  digitalWrite(RELAY_3, LOW);
 
  delay(500);
 
}
