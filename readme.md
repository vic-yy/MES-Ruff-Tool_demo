$env:PATH = [Environment]::GetEnvironmentVariable("PATH","Machine") + ";" + [Environment]::GetEnvironmentVariable("PATH","User")


- Como checar os erros:
ruff check to_diagnostic.py

- Como checar todos os erros:
python -m ruff check --select ALL to_diagnostic.py


- Como corrigir os erros detectados:
python -m ruff check --fix to_fix.py
python -m ruff check --diff to_fix.py


- Como corrigir a maioria dos erros:
python -m ruff check --unsafe-fixes --fix to_fix.py

- Como forçar a aplicação de mais regras:
python -m ruff check --select ALL --unsafe-fixes --fix .\to_fix.py
    