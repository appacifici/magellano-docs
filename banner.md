:arrow_left: [Index](index.md)

- Documento accessi
    - https://docs.google.com/spreadsheets/d/1qSJYJhltG38TM3WdLlQwlhOTPjgdwzNXsBK6RQ-jcec/edit#gid=1131407773

# Banner HB - NoHB 

- Se il sito si apre in nonHB e poi lo integro in BH
- NonHB 
    - ha solo AdSense
- HB 
    - ha google AD Manager
- Installare estensione
    - Prebid
    - Headerbid expert

# Posizionamenti
    - Top 
    - Middle
        - mapping anche MP_ARTICLE_L
        - aggiungere dimension separate da virgola
    - Bottom 
    - Sidebar 
    - StikyAMP   

# Procedura
- Creare una branch con la url del task assegnato
    - Vedi guida git
- Modificare: scripts/clear/magellano_hb_min.js ( centralizzato )
    - aggiungere nel primo switch:
        - teads_placement_id
        - teads_page_id
        - seedtag_placement
    - Secondo switch
        - Copiare da magellano_nobh_min.js
        - Incollare su magellano_hb_min.js
        - Fine
- Committare e fare push su server Contabo
- Verificare da browser che venga caricata correttamente questa url:
    - https://unifiedads.magellanotech.it/ads/configuration?mapping=rsnews

- Aspetto - Editor tema
    - Header.php
        - scrpt inizializzazione google tag dopo <?php wp_head(); ?>        
	    ```javascript
	    <script>var googletag = googletag || {}; googletag.cmd = googletag.cmd || [];</script>
	    ``` 

- WP QUADS PRO
    - Copia il contenuto es TOP da lineadiretta
    - Devi modificare il contenuto interno al div 
    - Poi midificare versione AMP
    - AppNexsus è relativo adAsta
    - Criteo c'è sempre

- WP Aspetto
    - WIDGET - Sidebar
        - Trovo 2 HTML personalizzati ( se non so che fare vedo linea diretta )
        - Modificare il placement-id in base a quelli attivi
        - GLi id non devono essere uguali ma sequenziali
        - NON HO AD ASTA TOGLIERE
        
- AMP 
    - Setup - Settings  - ADVANCED
        - Enter HTML Body
            - Copiare da lineadiretta contenuto <amp-sticky-ad-layout>
- Salvare js 
    - Copiare
    - Incollare su Javascript Obfuscator
        - FIle ricavato incollare su 
            - script magellano_hb_min.js (no /Clear) 
- Aspetto
    - Editor del tema
        - Footer 
            - cambiare puntamento noHb a hb.js
- Cancellare cache
- Controllare funzionamento con ext Chrome Predid
