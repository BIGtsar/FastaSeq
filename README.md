# FastaSeq

Python библиотека для чтения и анализа файлов в формате FASTA.

## Возможности

- Чтение FASTA файлов 
- Определение типа последовательности
- Получение информации о последовательностях

## Установка

```bash

# Клонируйте репозиторий
git clone https://github.com/BIGtsar/FastaSeq.git
cd FastaSeq
```

## Быстрый старт

```python
from fasta_reader import FastaReader

# Создайте объект для чтения FASTA файла
reader = FastaReader("example.fna")

# Проверьте формат файла
if reader.is_fasta():
    # Читайте записи последовательностей
    for i, seq_record in enumerate(reader.read_records(), 1):
        print(f"Запись #{i}:")
        print(seq_record)
        print("-" * 50)
else:
    print("Файл не является корректным FASTA файлом")
```

## Пример вывода
```text
Запись #1:
Заголовок fasta: sequence_1 description
Длина последовательности: 150
Алфавит последовательности: ДНК
Первые 50 символов последовательности: ATGCTAGCTAGCTAGCTAGCTAGCTAGCTAGCTAGCTAGCTAGCTAGCTA

--------------------------------------------------
```

## Структура проекта

```text
FastaSeq/
├── fasta_reader.py  # Основной класс для чтения FASTA
├── seq.py           # Класс для работы с последовательностью нуклеотидов
├── main.py          # Пример использования программы
├── docs/            # Документация
├── tests/           # Тесты последовательностей
└── examples/        # Примеры файлов
```


## Разработка

### Запуск тестов

```bash

python -m pytest tests/


```
## Лицензия
Этот проект распространяется под лицензией MIT. См. файл `LICENSE` для подробностей.
