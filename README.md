# Dashboard аналитики инцидентов

Ваша задача реализовать аналитическую систему для мониторинга инцидентов кибербезопасности.

---

# Сценарий

Команда ежедневно получает:

- алерты SIEM;
- инциденты ИБ;
- события от EDR/NDR;
- обращения от сотрудников;
- задачи расследования;
- данные об активах.

Нужно собрать систему, которая:

- агрегирует данные;
- рассчитывает SOC-метрики;
- показывает динамику угроз;
- выявляет проблемные зоны;
- анализирует SLA;
- показывает нагрузку аналитиков;
- строит dashboard для руководителя SOC.

---

# Что нужно сделать

## MVP

Система должна:

1. Загрузить CSV/XLSX/SQLite.
2. Очистить данные.
3. Нормализовать даты.
4. Обработать дубли.
5. Рассчитать SOC-метрики.
6. Построить dashboard.
7. Сравнить текущую неделю с baseline.
8. Выделить проблемные зоны.

---

# Обязательные метрики

## Инциденты

- количество инцидентов;
- MTTR;
- MTTD;
- SLA breach rate;
- false positive rate;
- incidents by severity;
- incidents by attack vector;
- incidents by business unit;
- incidents by analyst;
- escalation rate;
- reopen rate.

---

## Аналитики

- текущая загрузка;
- incidents per analyst;
- overtime risk;
- blocked tasks;
- unresolved critical incidents.

---

## Активы

- топ критичных активов;
- internet-exposed assets;
- incidents per asset;
- повторяющиеся атаки по активу.

---

# Обязательные визуализации

Минимум:

- incidents trend;
- SLA breach heatmap;
- severity distribution;
- analyst workload;
- attack vectors;
- top affected assets;
- timeline инцидентов.

---

# Проблемные зоны

Система должна автоматически выявлять:

- перегруженных аналитиков;
- аномальный рост инцидентов;
- высокий false positive;
- систематические SLA breach;
- критичные активы с повторяющимися атаками;
- ночные всплески активности;
- backlog расследований.

---

# Формат результата

Один из вариантов:

- Streamlit dashboard;
- HTML dashboard;
- PPTX;
- PDF.

Рекомендуемый вариант:

```
streamlit run app.py
```

---

# Структура dashboard

## Overview

- ключевые KPI;
- общая динамика.

## Incidents

- распределения;
- тренды;
- SLA.

## Analysts

- workload;
- capacity;
- overtime.

## Assets

- критичные системы;
- heatmap атак.

## Operational Risks

- backlog;
- SLA breach;
- escalation hotspots.

---

# Что нужно сдать

```
solution/
  app.py
  requirements.txt
  README.md
  data/
  output/
```

---

# README должен содержать

```
1. Как запускать
2. Какие файлы нужны
3. Где лежит dashboard
4. Какие библиотеки используются
5. Какие проверки качества данных реализованы
```
