# HackMyHome Power Control v0.22.4

Prima release pubblica di **HackMyHome Power Control** per Waveshare ESP32-S3 1.8" Knob Touch LCD, Home Assistant ed ESPHome.

## Funzioni principali

- dashboard del consumo totale della casa;
- monitoraggio fino a 14 elettrodomestici;
- visualizzazione della quota **Altri consumi**;
- gestione e riordino delle priorità di distacco;
- esclusione **NO AUTO** per i carichi che non devono essere spenti automaticamente;
- controllo dei dispositivi supportati tramite Home Assistant;
- soglie di attenzione e zona critica;
- feedback aptico tramite DRV2605;
- personalizzazione dei colori;
- pagina impostazioni;
- aggiornamenti OTA con stato sul display;
- stato Wi-Fi e stima batteria;
- apprendimento locale dei carichi non monitorati direttamente.

## Sicurezza

Il distacco automatico è inizialmente **disabilitato**.

Prima di abilitarlo verifica con attenzione:
- entity_id e comandi associati;
- ordine delle priorità;
- dispositivi marcati NO AUTO;
- soglie di potenza;
- comportamento reale dei carichi.

Non utilizzare il distacco automatico per dispositivi essenziali, critici, medicali, di sicurezza o non interrompibili.

## Installazione

Scarica il firmware:

**esphome/hackmyhome_power_control.yaml**

e segui la documentazione nel README e nella cartella **docs**.

## Feedback

Questa è una versione beta e può richiedere adattamenti alla propria installazione Home Assistant.

Bug, suggerimenti e idee sono benvenuti tramite le **Issues** del repository.
