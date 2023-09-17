:arrow_left: [Script Globali](/globalScripts.md)

# Service Worker (sw.js)

- Questo script una volta inserito sul sito web, genera la registrazione del service worker sul client dell'utente
- Quando un evento gestito nel codice, viene ricevuto viene inviato su GA4 il tracciamento dell'evento
- Per tracciare l'evento su GA4 tramite fetch alla url https://www.google-analytics.com/mp/collect è necessario avere il clientID del personale dell'utente che visita il sito. 
- Questo dato non è possibile ricavarlo da sw, per cuiè stato utilizzato un trick, sfruttando il sistema di cache dei sw, nel codice <head> del sito al caricamento della pagina viene recuperato e salvato su cache con il nome const CACHE_NAME = 'clienIdGM4'; cosi facendo è possibile recuperarlo dal sw.js