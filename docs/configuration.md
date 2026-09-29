# Configurazione

La maggior parte della personalizzazione avviene nella sezione **substitutions** all'inizio del file ESPHome.

## Rete e API

Le credenziali sono lette da secrets.yaml tramite !secret. Non inserirle nel repository.

## Sensore totale della casa

**power_sensor_entity** deve indicare un sensore Home Assistant espresso in watt.

## Soglie

- **power_limit_w**: riferimento massimo usato dall'interfaccia
- **power_warning_w**: ingresso nella zona di attenzione
- **power_critical_w**: zona critica
- **power_haptic_hysteresis_w**: rientro richiesto prima di riarmare l'avviso aptico

## Elettrodomestici

Power Control supporta 14 slot. Ogni slot ha un nome, un sensore di potenza e un comando associato.

Il comando può essere uno **switch** oppure, per i dispositivi gestiti dal firmware, un'entità **climate**.

## Priorità di distacco

L'ordine stabilisce quale carico viene considerato per primo quando Power Control deve ridurre l'assorbimento.

**Priorità non significa consumo.** Un dispositivo da 300 W può essere prima di uno da 1.500 W se preferisci che sia lui il primo candidato al distacco.

La pagina DISTACCO permette di riordinare i dispositivi direttamente dal Knob.

## NO AUTO

Ogni dispositivo può essere escluso dal distacco automatico. Usa questa funzione per tutti i carichi che non vuoi interrompere automaticamente.

Il firmware parte con la gestione automatica disabilitata.

## Colori

La pagina COLORI permette di associare un colore ai dispositivi mostrati nella dashboard.

## Hardware e pin

I pin inclusi nel file sono configurati per il Waveshare ESP32-S3 1.8" Knob Touch LCD usato nel progetto HackMyHome.

## Batteria

La percentuale batteria è una stima derivata dalla tensione della LiPo 1S e non è una misura precisa dello stato di carica.
