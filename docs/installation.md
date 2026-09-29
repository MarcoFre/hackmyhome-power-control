# Installazione

## Requisiti

- Home Assistant funzionante
- ESPHome
- Waveshare ESP32-S3 1.8" Knob Touch LCD
- un sensore Home Assistant con la potenza totale della casa in watt
- Wi-Fi 2.4 GHz raggiungibile dal Knob

Per il controllo dei singoli dispositivi servono anche sensori di potenza e, dove previsto, entità comandabili switch o climate.

## 1. Copia il firmware

Copia **esphome/hackmyhome_power_control.yaml** nella cartella ESPHome e aprilo dall'editor ESPHome.

## 2. Configura secrets.yaml

Il firmware legge tre segreti: wifi_ssid, wifi_password e api_encryption_key. Puoi partire da **secrets.example.yaml**.

Non pubblicare mai il tuo secrets.yaml.

## 3. Configura il sensore di potenza totale

Nella sezione substitutions modifica **power_sensor_entity** indicando un sensore Home Assistant espresso in watt.

## 4. Configura soglie e limiti

Adatta **power_limit_w**, **power_warning_w**, **power_critical_w** e **power_haptic_hysteresis_w** al tuo impianto e alla strategia di gestione che vuoi adottare.

## 5. Configura gli elettrodomestici

Sono disponibili fino a 14 slot. Per ogni slot puoi indicare nome visualizzato, sensore di potenza Home Assistant e entità comandabile associata.

Gli entity_id presenti nel file sono quelli dell'installazione HackMyHome e servono come esempio.

## 6. Valida

Da ESPHome usa **Validate** e correggi ogni errore prima del flash.

Il firmware scarica anche il componente esterno **github://RAR/esphome-drv2605**, necessario per il feedback aptico.

## 7. Primo avvio

Per la prima installazione è consigliato il flash via USB. Dopo il collegamento corretto a Home Assistant, gli aggiornamenti successivi possono essere eseguiti OTA.

## 8. Prima prova

Verifica nell'ordine: Wi-Fi, API Home Assistant, potenza totale, sensori dei dispositivi, touch, encoder, feedback aptico, comandi manuali e lista delle priorità.

Lascia il **distacco automatico disabilitato** durante i primi test.

## 9. Distacco automatico

Abilitalo solo dopo aver verificato che ogni comando agisca sul dispositivo corretto, che i carichi critici siano NO AUTO, che le priorità siano quelle desiderate e che le soglie siano adatte al tuo impianto.
