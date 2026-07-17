# IKOS Aria — Wine Stock & Allocation dashboard

Single self-contained file **`index.html`** (HTML+CSS+JS+data, ~3900 lines) served from GitHub Pages `main`. No build step, no backend.

## Always-on rules
1. **ASK THE USER FOR TODAY'S DATE** before setting `Last Updated:` on any stock update. Never guess it.
2. **Work only in `index.html`** (single source). No new files unless asked.
3. **Test before every commit**: extract the main `<script>`, run `node --check`, then a Playwright smoke test (login `#lg-user`=`adam` / `#lg-pin`=`9001`, click the affected `#tab-*`, assert 0 JS errors — ignore `TUNNEL`/`qrserver`/`net::`/`Failed to load`).
4. **Commit to `main` and `git push -u origin main`** (Pages serves from main). One clean commit per change; batch related edits.
5. Edit the big single-line data arrays by parsing → mutating → re-serializing (compact JSON), never fragile regex. Validate parse + count after.

## For non-trivial work, use the specialist agent
For stock updates, new tabs/features, bots, guest/QR menus, or bug fixes, use the **`wine-dashboard`** subagent (`.claude/agents/wine-dashboard.md`) — it has the full data-model, the Excel→HTML update workflow, and the test/commit procedure.

## Quick data map
`STOCK_DATA` (377 wines, single source of truth) · `MASTER`/`SPECIAL` (curated, derive from STOCK_DATA at load) · `CONSUMPTION_2026` (+`CONS_MONTHS`) · `BEVERAGES` (non-wine, ~430) · `PAIRING_DATA` (menus/dishes/pairings) · `STATIC_NOTES` · `SOMM_*`/`COCKTAILS` (bot knowledge). App logic is the `D` (Dash) class; tabs via `switchTab()`. Guest pages: `#menu[/OUTLET]` (wines) and `#food/OUTLET` (menu), no login.
