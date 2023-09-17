:arrow_left: [Script Globali](/globalScripts.md)

# Append Banner Google (appendBanner.js)

- Per utilizzare questo script basta includere con il tag html <script ...></script> all'interno del tag <head> o <body> a seconda delle esigente
- Lo script fatto ha una sua classe all'interno che viene automaticamente autoinstanziata.
- Cerca con un intervallo di 2000 ms (2sec), la presenza del posizionamento dei banner di Nativery, qualora venga trovato interrompe l'intervallo e avvia l'inserimento dei banner di google, ogni tot posizionamenti 
```js
let positions = {};
    jQuery('*[id*=nat_]').find('.nat-items').find('*[id*=nat_]').each(function(key, value) {
        if( key % 5 == 0 ) {        
            let bPosition = Math.round(jQuery(this).offset().top);        
            positions[bPosition] = jQuery(this);        
        }
    });
```