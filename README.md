
## Gestione dati

Nel progetto sono stati implementati 2 file json, uno a livello globale e uno locale.
Il file locale ha uno schema preciso per contenere i dati temporanei o comunque a livello
locale, utili per esempio alla voce _remember me_ presente sia nella login che nella register page.

Mentre il file data contiene vari valori legati agli utenti, funziona da auth e da gestione
dell'utente stesso per l'intero programma, vengono salvate informazioni, specifiche e molto altro.
Nel seguente codice verranno mostrati gli schemi da noi realizzati per la gestione di questi dati.

* Esempio di file `local.json`:

  ```json
  {
    "logged": true,
    "userLog":{
        "role": "admin",
        "user": "campomatteo2005@gmail.com"
    }
  }
  ```

* Esempio di file `data.json`, sezione utenti:

  ```json
  "user":{
        "campomatteo2005@gmail.com":{
            "username": "NotMatte",
            "nome": "Matteo",
            "cognome": "Campo",
            "password": "prova123",
            "role": "admin",
            "info":{
                "logged": "10/05/2023 12:00",
                "ordinatiTotali": "10",
                "preferiti": ["h1","h3","b8"]
            },
            "carrello":{
                "vuoto": false,
                "prodotti":{
                    "bibite":{
                        "b1":{ "quantita": 2, "prezzoSingolo": 1.5, "prezzoTotale ": 3 }
                    },
                    "hamburger":{
                        "h1":{ "quantita": 1, "prezzoSingolo": 5.2, "prezzoTotale ": 10.4 },
                        "h3":{ "quantita": 1, "prezzoSingolo": 6, "prezzoTotale ": 12 }
                    }
                },
                "items": 3,
                "prezzoCarrello": 25.4
            },
            "hystory":{
                "ordinati": {
                    "totHamburger": 5,
                    "hamburger":{
                        "h1": 1,
                        "h3": 3,
                        "h4": 1
                    },
                    "totBibite": 10,
                    "bibite":{
                        "b8": 8,
                        "b1": 2
                    }
                }
            },
            "datiGenerati": {
                "categoriaPreferita": "bibite",
                "prodottoPreferito": "b8"
            }
        }
    },
  ```

* Esempio di file `data.json`, sezione prodotti:

  ```json
  "product":{
        "hamburger":{
            "h1":{
                "nome": "Big Burger",
                "descrizione": "Hamburger di carne di manzo",
                "immagine": "",
                "prezzo": 5.2,
                "categoria": "hamburger",
                "ingredienti": ["pane","carne di manzo","lattuga","pomodoro","formaggio","salsa"]
            },
            "h2":{
                "nome": "Chicken Burger",
                "descrizione": "Hamburger di carne di pollo",
                "immagine": "",
                "prezzo": 4.5,
                "categoria": "hamburger",
                "ingredienti": ["pane","carne di pollo","lattuga","pomodoro","formaggio","salsa"]
            },
            "h3":{
                "nome": "Hot Burger",
                "descrizione": "Hamburger di carne di maiale",
                "immagine": "",
                "prezzo": 6,
                "categoria": "hamburger",
                "ingredienti": ["pane","carne di maiale","lattuga","pomodoro","formaggio","salsa"]
            }
        },
        "bibite":{
            "b1":{
                "nome": "Coca Cola",
                "descrizione": "Bibita gassata",
                "immagine": "",
                "prezzo": 1.5,
                "litri": 0.5,
                "categoria": "bibite",
                "ingredienti": ["acqua","zucchero","colorante","aromi"]
            },
            "b2":{
                "nome": "Fanta",
                "descrizione": "Bibita gassata",
                "immagine": "",
                "prezzo": 1.5,
                "litri": 0.5,
                "categoria": "bibite",
                "ingredienti": ["acqua","zucchero","colorante","aromi"]
            },
            "b3":{
                "nome": "Sprite",
                "descrizione": "Bibita gassata",
                "immagine": "",
                "prezzo": 1.5,
                "litri": 0.5,
                "categoria": "bibite",
                "ingredienti": ["acqua","zucchero","colorante","aromi"]
            },
            "b4":{
                "nome": "Coca Cola Zero",
                "descrizione": "Bibita gassata",
                "immagine": "",
                "prezzo": 1.5,
                "litri": 0.5,
                "categoria": "bibite",
                "ingredienti": ["acqua","zucchero","colorante","aromi"]
            }
        }
        
    }
  ```

