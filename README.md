# Simple DDoS in Python

Программа запускает много потоков, которые постоянно отправляют HTTP-запросы на указанный IP-адрес. Это может "перегружать" сервер.

---

## Как использовать

1. Установи Python 3
2. Скачай проект и перейди в папку
3. Запусти команду:

```bash
python main.py --ip 127.0.0.1
```

Можно указать количество потоков:

```bash
python main.py --ip 127.0.0.1 --th 5000
```

Также можно указать URL вместо IP:

```bash
python main.py --url example.com
```

---

## Аргументы

- `--ip` — IP-адрес цели
- `--url` — адрес сайта (без http://)
- `--th` — количество потоков (по умолчанию 100000)

---

## Как работает

- Проверяет IP-адрес или получает его по URL
- Запускает потоки
- Каждый поток бесконечно отправляет HTTP-запросы
