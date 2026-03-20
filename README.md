# Angola Bank Codes

Open dataset of Angolan commercial banks — codes, names, SWIFT/BIC, websites.

Useful for developers integrating banking or payment services in Angola.

## Install

```bash
npm install angola-bank-codes
```

Or just download [`banks.json`](./banks.json) directly.

## Usage

### JavaScript / TypeScript

```js
const banks = require('angola-bank-codes');

// Get all banks
console.log(banks.banks);

// Find a bank by code
const bai = banks.banks.find(b => b.code === 'BAI');
console.log(bai.name); // "Banco Angolano de Investimentos"
console.log(bai.swift_bic); // "BAIAAOLU"

// Get all active banks
const active = banks.banks.filter(b => b.active);
console.log(`${active.length} active banks`);
```

### Python

```python
import json

with open('banks.json') as f:
    data = json.load(f)

for bank in data['banks']:
    print(f"{bank['code']}: {bank['name']} ({bank['website']})")
```

## Banks

| Code | Name | Website | SWIFT/BIC |
|------|------|---------|-----------|
| BAI | Banco Angolano de Investimentos | [bancobai.ao](https://bancobai.ao) | `BAIAAOLU` |
| BCA | Banco Comercial Angolano | [bca.ao](https://www.bca.ao) | — |
| BCH | Banco Comercial do Huambo | [bch.ao](https://www.bch.ao) | — |
| BCGA | Banco Caixa Geral Angola | [bcga.ao](https://www.bcga.ao) | — |
| BCS | BCS - Banco de Credito do Sul, S.A. | [bcs.ao](https://www.bcs.ao) | — |
| BDA | Banco de Desenvolvimento de Angola | [bda.ao](https://www.bda.ao) | — |
| BE | Banco Economico | [bancoeconomico.ao](https://www.bancoeconomico.ao) | `BESCAOLU` |
| BFA | Banco de Fomento Angola | [bfa.ao](https://www.bfa.ao) | `BFMXAOLU` |
| BIC | Banco BIC | [bancobic.ao](https://www.bancobic.ao) | `BICXAOLU` |
| BIR | Banco de Investimento Rural | [bir.ao](https://www.bir.ao) | — |
| BMA | Banco Millennium Atlantico | [atlantico.ao](https://www.atlantico.ao) | `ATLAAOLU` |
| BMF | Banco BAI Micro Financas | [bmf.ao](https://www.bmf.ao) | — |
| BNI | Banco de Negocios Internacional | [bni.ao](https://www.bni.ao) | — |
| BPC | Banco de Poupanca e Credito | [bpc.ao](https://www.bpc.ao) | `BPCXAOLU` |
| BPG | Banco Postal | [bancopostal.ao](https://www.bancopostal.ao) | — |
| BTN | Banco Terra Nova | [btn.ao](https://www.btn.ao) | — |
| BV | Banco Valor | [bancovalor.ao](https://www.bancovalor.ao) | — |
| FNB | First National Bank Angola | [fnb.ao](https://www.fnb.ao) | — |
| KEVE | Banco Keve | [bancokeve.ao](https://www.bancokeve.ao) | — |
| SBA | Standard Bank Angola | [standardbank.co.ao](https://www.standardbank.co.ao) | `SBICAOLU` |
| SOL | Banco Sol | [bancosol.ao](https://www.bancosol.ao) | `BSOLAOLU` |
| VTB | VTB Africa | [vtbafrica.ao](https://www.vtbafrica.ao) | — |
| YETU | Banco Yetu | [bancoyetu.ao](https://www.bancoyetu.ao) | — |

## Live Exchange Rates

For live exchange rates from these banks, visit **[cambio.ao](https://cambio.ao)** — compares buy/sell rates across all Angolan commercial banks, updated hourly.

- [Bank rate comparison](https://cambio.ao/cambio-do-dia) — side-by-side rates for USD, EUR, ZAR
- [Currency converter](https://cambio.ao/conversor-de-moeda) — convert with real Angolan bank rates

## Related

- [Stack Financeira Angola](https://github.com/ExponencialAO/stack-financeira-angola) — Curated list of Angola's financial ecosystem
- [Awesome Angola Dev](https://github.com/ExponencialAO/awesome-angola-dev) — Developer tools and resources for Angola

## Data Sources

Bank information compiled from BNA (Banco Nacional de Angola), ABANC (Associacao Angolana de Bancos), and individual bank websites. SWIFT/BIC codes sourced from public registries.

**Disclaimer:** This dataset is provided as-is for informational purposes. Verify SWIFT/BIC codes with your bank before using in production transactions.

## Contributing

Found an error or missing bank? Open an issue or submit a pull request.

## License

MIT — [Exponencial](https://exponencial.ao)
