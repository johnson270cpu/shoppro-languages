# ShopPro languages

Translation files for the ShopPro app. The app downloads a language file once (when the user taps
"Download more languages") and then works offline.

## Files
- `languages.json` - list of available languages and their version numbers
- `sw.json` - Kiswahili

## File format
```json
{
  "_meta": { "code": "sw", "name": "Kiswahili", "version": 1 },
  "Sell": "Uza",
  "Low stock": "Bidhaa zinaisha"
}
```
The **key is the English text** used in the app. If a key is missing the app shows English.

## Rules for translators
1. Never change the keys (left side). Only translate the values (right side).
2. Keep placeholders exactly: `%s`, `%d`, `%.0f`. Same number of them, same order.
   Example: `"Only %d in stock": "Zipo %d tu"`.
3. Keep `\n` line breaks.
4. To publish a fix: edit the file, then raise `version` in BOTH the file's `_meta` and `languages.json`.
   Phones will show "Update available".

## Adding a language
1. Copy `sw.json` to e.g. `fr.json`, translate the values, change `_meta`.
2. Add an entry to `languages.json`:
   `{ "code": "fr", "name": "Francais", "version": 1, "file": "fr.json" }`

## Please review (money words)
Credit = Mkopo, Charge = Lipisha, Void sale = Futa mauzo, Balance = Salio, "ana deni la" (owes),
Expense = Gharama, Stock = Bidhaa, General = Kawaida.
