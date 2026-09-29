# Apprendimento dei carichi

La funzione di apprendimento raccoglie informazioni sui carichi che non dispongono di un sensore di potenza dedicato.

## Concetto

Power Control calcola la quota di potenza non attribuita ai dispositivi già monitorati: **Altri consumi**.

Quando questa quota aumenta in modo significativo e rimane sufficientemente stabile, il Knob può chiedere:

1. **Cosa hai acceso?**
2. **Come lo stai usando?**

Una conferma associa l'aumento rilevato al dispositivo e alla modalità selezionata.

## Parametri

Nel file ESPHome sono presenti **learning_stability_w**, **learning_prompt_timeout_s** e **learning_cooldown_s**.

La soglia minima dell'aumento che attiva l'apprendimento è modificabile dal Knob nella pagina IMPOSTAZIONI.

## Profili locali

Il firmware conserva localmente profili composti da dispositivo, modalità, valore medio osservato e numero di conferme.

Sono previste più conferme prima che un profilo venga considerato significativo.

## Ambiguità

Due apparecchi possono avere assorbimenti simili e lo stesso apparecchio può cambiare consumo nel tempo. Il riconoscimento non va quindi interpretato come identificazione certa del carico.

## Importante

I profili appresi sono **solo diagnostici** e non vengono usati per comandare automaticamente il distacco.

Le decisioni di distacco rimangono legate ai dispositivi esplicitamente configurati e alle relative autorizzazioni e priorità.
