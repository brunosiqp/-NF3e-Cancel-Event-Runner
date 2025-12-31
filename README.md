# -NF3e-Cancel-Event-Runner
Python runner to batch cancel NF3e documents via Inventti API using Excel input, with per-record confirmation and full execution logging.

## 🇺🇸 English

This project is a Python runner that reads Excel files containing NF3e document keys and sends cancel events to the Inventti NF3e API. Each record is processed individually, with real-time console output and a persistent log file generated at the end of execution.

Features:
- Reads multiple `.xlsx` files
- Uses a fixed CNPJ as required by the API
- Sends cancel event (tpEvento = 110111)
- Confirms success or failure one by one
- Generates a `runner_log.txt` file

Requirements:
- Python 3.10 or higher
- pandas
- requests
- openpyxl

Installation:
pip install pandas requests openpyxl

File structure:
runner_cancelamento.py  
runner_log.txt  
Ticket 350481 - Solicitar cancelamento - EDP ES.xlsx  
Ticket 350481 - Solicitar cancelamento - EDP SP.xlsx  

How to run:
python runner_cancelamento.py

Or inside Python:
exec(open("runner_cancelamento.py", encoding="utf-8").read())

Expected Excel format:
The Excel file must contain a column named `Chave`.  
No CNPJ column is required.

Output:
- Console logs during execution
- `runner_log.txt` with the full execution history

---

## 🇧🇷 Português (Brasil)

Este projeto é um runner em Python que lê arquivos Excel contendo chaves de documentos NF3e e envia eventos de cancelamento para a API NF3e da Inventti. Cada registro é processado individualmente, com log no console e geração de um arquivo `.txt` com o histórico completo.

Funcionalidades:
- Leitura de múltiplos arquivos `.xlsx`
- Uso de CNPJ fixo conforme exigido pela API
- Envio de evento de cancelamento (tpEvento = 110111)
- Confirmação linha a linha
- Geração do arquivo `runner_log.txt`

Requisitos:
- Python 3.10 ou superior
- pandas
- requests
- openpyxl

Instalação:
pip install pandas requests openpyxl

Estrutura de arquivos:
runner_cancelamento.py  
runner_log.txt  
Ticket 350481 - Solicitar cancelamento - EDP ES.xlsx  
Ticket 350481 - Solicitar cancelamento - EDP SP.xlsx  

Execução:
python runner_cancelamento.py

Ou dentro do Python:
exec(open("runner_cancelamento.py", encoding="utf-8").read())

Formato esperado do Excel:
O arquivo deve conter a coluna `Chave`.  
Não é necessário informar CNPJ no Excel.

Saída:
- Logs no console
- Arquivo `runner_log.txt` com o histórico completo da execução

---

## 🇫🇷 Français

Ce projet est un runner Python qui lit des fichiers Excel contenant des clés de documents NF3e et envoie des événements d’annulation à l’API NF3e d’Inventti. Chaque ligne est traitée individuellement avec journalisation complète dans un fichier texte.

Fonctionnalités:
- Lecture de plusieurs fichiers `.xlsx`
- Utilisation d’un CNPJ fixe
- Envoi de l’événement d’annulation (tpEvento = 110111)
- Confirmation ligne par ligne
- Génération du fichier `runner_log.txt`

Prérequis:
- Python 3.10 ou supérieur
- pandas
- requests
- openpyxl

Installation:
pip install pandas requests openpyxl

Structure des fichiers:
runner_cancelamento.py  
runner_log.txt  
Ticket 350481 - Solicitar cancelamento - EDP ES.xlsx  
Ticket 350481 - Solicitar cancelamento - EDP SP.xlsx  

Exécution:
python runner_cancelamento.py

Ou depuis l’interpréteur Python:
exec(open("runner_cancelamento.py", encoding="utf-8").read())

Format attendu du fichier Excel:
Le fichier doit contenir la colonne `Chave`.  
Aucune colonne CNPJ n’est requise.

Résultat:
- Logs affichés en console
- Fichier `runner_log.txt` avec l’historique complet de l’exécution
