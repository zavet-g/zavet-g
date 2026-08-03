# Artem

Backend developer. Moscow.

Four years on production systems: document pipelines, integrations with external registries and messengers, message queues, highload Telegram bots/apps. Two tracks — Python services and 1C-Bitrix / PHP portals with CRM integrations. Most of that work is closed source, so the repositories below are side projects: they show how I structure code, not what I shipped at work.

The exception is the first one — a tool I built because I needed it at work and nothing like it existed.

Currently open to backend roles.

## Main stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![1C-Bitrix](https://img.shields.io/badge/1C--Bitrix-EE2B24?style=flat-square&logo=1c&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

## Also work with

![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![GitLab CI](https://img.shields.io/badge/GitLab%20CI-FC6D26?style=flat-square&logo=gitlab&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)

## For fun

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)

## phpstan-bitrix

[**phpstan-bitrix**](https://github.com/zavet-g/phpstan-bitrix) — a PHPStan extension for 1C-Bitrix projects. Sixteen rules that find legacy kernel API, uncached queries, N+1 over infoblock properties, SQL built by concatenation and blocking calls inside event handlers.

Generic PHPStan knows nothing about the platform: to it, `CIBlockElement::GetList()` inside a `foreach` is just a static call, not the thing that takes down the database on a list of a thousand elements. No such extension exists on packagist, and Bitrix's own quality monitor solves a different problem — taint analysis for XSS and injections.

Written against a real project: 1072 files, 201 legacy API findings. That run is also why the legacy rules are split into five identifiers instead of one — 95 of those findings were mechanical `CModule::IncludeModule()` replacements, and without the split you would have to choose between that noise and the rule itself.

PHP 8.2+, tested on 8.2 through 8.5.

## Other repositories

| project | what it is | worth a look for |
|---|---|---|
| [passenger-flow](https://github.com/zavet-g/passenger-flow) | quarterly passenger flow forecasting for Moscow Metro | clean architecture with real layer boundaries, six forecasting models behind two protocols |
| [finans-nova](https://github.com/zavet-g/finans-nova) | Telegram bot for expense tracking, voice input | circuit breaker, rate limiting, health probes, metrics |
| [nginx_log_analyzer](https://github.com/zavet-g/nginx_log_analyzer) | streaming parser for nginx access logs with analytics API | layered FastAPI service, CRUD over SQLAlchemy, 67 tests |
| [HabrDigest](https://github.com/zavet-g/HabrDigest) | article digests from Habr, summarised by an LLM | Celery scheduling, scraping, error handling split by layer |
| [LogiFlow](https://github.com/zavet-g/LogiFlow) | Django app for delivery accounting with reports | Django + DRF, admin, 56 tests at 86% coverage |
| [DotaTicketWatch](https://github.com/zavet-g/DotaTicketWatch) | Go service that watches ticket drops and reports to Telegram | concurrency, Cloudflare bypass via TLS fingerprinting, caching |

Each README explains the problem, the reasoning behind the design and — separately — what the project does not do.

## Contact

- Telegram: [@bcdbcddd](https://t.me/bcdbcddd)

