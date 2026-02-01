---
name: heading-converter
description: Automates the mapping of raw CSV headers (typically Chinese) to standardized internal field names for the option trading record system.
---

# Heading Converter Logic
You are an expert at data normalization and Taiwan-based brokerage CSV formats.

## Objective
Use this skill to generate the correct mapping.

## Standard Internal Keys
<!-- - `action_raw`: For "買賣別" (maps to Long/Short) -->
- `action`: For "買賣別" (maps to Long/Short)
<!-- - `order_status`: For "倉別" (Open/Close/新倉/平倉) -->
- `order_type`: For "倉別" (Open/Close/新倉/平倉)
<!-- - `input_raw`: For "商品名稱" (e.g., 台指選02 P 29500) -->
- `item_name`: For "商品名稱" (strip strip '台指選', '台指選02' -> '02')

- `price`: For "均價" or "單價"
- `qty`: For "留倉總口數" or "成交口數"
- `current`: For "市值"
- `profit_loss`: For "未平倉損益" or "P/L"
- `delta`: For "Delta"
- `gamma`: For "Gamma"
- `buy_pwr`: For "所需保證金" or "BP"
- 'days': days to expiery.
- 'current': (profit_loss - price*50)/50

## Procedure
1. **Header Identification**: Read the first line of the new data file and strip any BOM or invisible characters.
2. **Auto-Mapping**:
   - Match headers based on keywords (e.g., "損益" -> "profit_loss", "保證金" -> "buy_pwr").
   - Handle variations like "市場價格" vs "均價".
3. **YAML Generation**: Create a new group in `trading_reocrd_cfg.yaml` using the file's prefix or source name.
4. **Validation**: Run the parser preview (`--parse`) to ensure `Long/Short` mapping and contract extraction work correctly.

## Constraints
- **Preserve Logic**: Never drop `order_status` during normalization as it's required for trade alignment.
- **Encoding**: Default to `utf-8-sig` for detection, but fallback to `cp950` if Chinese characters are garbled.
