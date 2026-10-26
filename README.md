[README.md](https://github.com/user-attachments/files/33991529/README.md)
# Panel MRF LED

Mobilny panel do sterowania ESP32-WROOM-32 i 8 diodami WS2812B przez BLE.

## Uruchomienie na iPhonie

1. Zapisz `index.html` na hostingu, który udostępnia stronę przez **HTTPS** (np. GitHub Pages).
2. Zainstaluj i uruchom **Bluefy – Web BLE Browser** na iPhonie, włącz Bluetooth.
3. Otwórz w Bluefy bezpieczny adres panelu i naciśnij **Połącz z lampą**.
4. Wybierz `MRF_LED_BLE` z listy urządzeń. ESP32 musi być włączone i reklamować BLE.

Zwykłe Safari na iPhonie nie udostępnia stronie Web Bluetooth GATT. Do tego panelu na iPhonie użyj Bluefy. Nie otwieraj pliku jako `file://`: Web Bluetooth wymaga bezpiecznego kontekstu HTTPS.

## Obsługiwane komendy

Panel wysyła bez dodatkowego znaku końca linii: `RED`, `GREEN`, `BLUE`, `WHITE`, `PURPLE`, `ORANGE`, `RAINBOW`, `BRIGHTNESS:0`–`BRIGHTNESS:255`, `OFF`.

Animacje ograniczają się do `RAINBOW`, ponieważ tylko ta animacja jest obsługiwana przez podany firmware. „Stały kolor” wybiera się przyciskiem koloru.

UUID usługi: `4fafc201-1fb5-459e-8fcc-c5c9c331914b`  
UUID charakterystyki zapisywalnej: `beb5483e-36e1-4688-b7f5-ea07361b26a8`
