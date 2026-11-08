# Bank Reconciliation Tool

Browser tool that reconciles a bank statement with accounting records (CSV). It finds matched, missing and date-mismatched transactions. It runs locally in the browser, and no data is sent anywhere.

**Инструмент для сверки банковской выписки с учётом (CSV). Работает в браузере, данные никуда не отправляются.**

## What it does

- Takes two CSV inputs: a bank statement and accounting records (for example, an export from 1C or Excel).
- Recognises Russian and English headers (date / дата, amount / сумма, or debit / credit), several date formats and decimal commas.
- Matches transactions by amount and date, with an adjustable tolerance in days.
- Shows four groups: matched, only in the bank, only in the accounting records, and same amount but the date is outside the tolerance. It also shows the difference between the totals.

## How to use

1. Open `index.html` in a browser (or the GitHub Pages link, if enabled).
2. Paste or upload both CSV files, or click **Пример данных** to try the sample.
3. Set the date tolerance and click **Сверить**.

Expected columns: date, amount (or debit and credit), and optionally a description.

```
Дата;Описание;Сумма
02.10.2026;Оплата поставщику;-150000,00
```

## Limitations

- No saving or export of results yet.
- One currency per file; one-to-one matching only (no split payments).
- It is a helper for an accountant, not an audit conclusion. Check every difference against the source documents.

## Privacy

All processing happens in your browser. Please do not publish real bank statements in this repository; use fictional data for demos.

## Author

Nurdaulet Amirali
