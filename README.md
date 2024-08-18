# EsercizioInventario

### Esercizio: Gestione di un Inventario

#### Obiettivo:
Implementare un programma che utilizzi le classi Merce e Inventario per simulare la gestione di un inventario di un negozio. Il programma dovrà creare diversi oggetti Merce, aggiungerli all'inventario e poi visualizzare lo stato dell'inventario.

#### Passaggi:

1. *Creazione delle merci:*
   - Crea almeno tre oggetti Merce con nome, quantità iniziale e tipo di merce differente.
   - Ad esempio, puoi creare oggetti come "Pane", "Latte" e "Uova".

2. *Creazione di un inventario:*
   - Crea un oggetto Inventario associandolo a un nome di negozio a tua scelta.
   - Aggiungi le merci create all'inventario utilizzando il metodo AggiungiMerceAdInventario.

3. *Modifica delle quantità:*
   - Simula l'arrivo di una nuova spedizione per alcune delle merci. Usa il metodo AggiungiQuantitaAMerce per aggiungere quantità alle merci esistenti.
   - Ad esempio, aggiungi 20 unità di "Pane" e 15 unità di "Latte".

4. *Visualizzazione dell'inventario:*
   - Chiama il metodo MostraMerce per visualizzare lo stato attuale dell'inventario.
   - Verifica che le quantità siano state aggiornate correttamente e che tutte le informazioni delle merci siano visualizzate correttamente.

#### Codice di esempio:

csharp
using System;
using System.Collections.Generic;
using InventoryExercise;

namespace InventoryApp
{
    class Program
    {
        static void Main(string[] args)
        {
            // Creazione delle merci
            Merce pane = new Merce { Nome = "Pane", Quantita = 50, TipodiMerce = "Alimentare" };
            Merce latte = new Merce { Nome = "Latte", Quantita = 30, TipodiMerce = "Alimentare" };
            Merce uova = new Merce { Nome = "Uova", Quantita = 100, TipodiMerce = "Alimentare" };

            // Creazione dell'inventario
            Inventario inventario = new Inventario { NomeNegozio = "Supermercato XYZ" };

            // Aggiunta delle merci all'inventario
            inventario.AggiungiMerceAdInventario(pane);
            inventario.AggiungiMerceAdInventario(latte);
            inventario.AggiungiMerceAdInventario(uova);

            // Modifica delle quantità
            inventario.AggiungiQuantitaAMerce("Pane", 20); // Aggiunge 20 unità di Pane
            inventario.AggiungiQuantitaAMerce("Latte", 15); // Aggiunge 15 unità di Latte

            // Visualizzazione dell'inventario
            inventario.MostraMerce();
        }
    }
}


#### Obiettivo finale:
Il programma dovrebbe stampare le seguenti informazioni (esempio):


Merce: Pane
Quantita': 70
Tipo di merce': Alimentare

Merce: Latte
Quantita': 45
Tipo di merce': Alimentare

Merce: Uova
Quantita': 100
Tipo di merce': Alimentare
