# opencoesione2postgresql.py
Importa file CSV di [OPENCOESIONE](https://opencoesione.gov.it/it/) in una tabella [postgresql](https://www.postgresql.org/).

Lo schema di tabella deriva dai [metadati](https://opencoesione.gov.it/media/opendata/metadati_progetti_tracciato_esteso.xlsx) di opencoesione. 

## Richiede
* [Python 3.x](https://www.python.org/downloads/)
* [psycopg](https://www.psycopg.org/)

## Quickstart

Installa le dipendenze, crea un nuovo database (es. `opencoesione`), e usa lo script `opencoesione2postgresql.py`:

``` console
$ pip install -r requirements.txt
...
Successfully installed psycopg-3.3.2 psycopg-binary-3.3.2
$ createdb opencoesione
$ python opencoesione2postgresql.py file_col_dataset.csv opencoesione
```

In questo modo verrà create la tabella `opencoesione` nel db che conterrà i dati provenienti dal file `file_col_dataset.csv` scaricato dalla sezione [Dati](https://opencoesione.gov.it/it/dati/).

## Installazione

``` console

$ pip install -r requirements.txt
...
Successfully installed argparse-1.2.1 libarchive-c-2.9 lxml-4.5.2 psycopg2-binary-2.8.4 six-1.10.0
$ createdb beerSO
$ python load_into_pg.py -s beer -d beerSO
```


### Opzioni aggiuntive
    usage: opencoesione2postgresql.py [-h] [-H DBHOST] [-P PORT] [-u USER] [-p] [-t TABLE] [-d] csvfile dbname

	positional arguments:
		csvfile              File csv ottenuto da Opencoesione
  		dbname               Database in cui importare i dati

	options:
  		-h, --help           show this help message and exit
	  	-H, --dbhost DBHOST  Host postgresql
  		-P, --port PORT      Porta, default=5432
  		-u, --user USER      Username postgresql
  		-p, --password       Password postgresql richiesta
  		-t, --table TABLE    Tabella in cui inserire i dati
  		-d, --delete         Elimina e ricrea la tabella

## Aiuto
Se hai qualche domanda o richieta, apri una [issue su GitHub](https://github.com/gianluca-saba/opencoesione2postgresql.py/issues).
