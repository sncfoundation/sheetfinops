<p align="center">
  <img src="https://sncfoundation.github.io/logos/sheetfinops.svg" width="96" alt="SheetFinOps logo">
</p>

<h1 align="center">SheetFinOps</h1>

<p align="center"><b>A \$0 infrastructure cost dashboard</b><br>
A <a href="https://sncfoundation.github.io">Sheet-Native Computing Foundation</a> project &#183; analog of <b>CNCF FinOps</b></p>

---

**Status:** 📝 Unsaved Draft &#183; this project is a proposal. Design notes and contributions are welcome.

## About

A \$0 infrastructure cost dashboard Part of the spreadsheet-native stack — the Sheet stays the source of truth, and it reconciles.

## Get involved

- 📋 Tracking issue &amp; design: [sncfoundation/sheeternetes#13](https://github.com/sncfoundation/sheeternetes/issues/13)
- 🗺️ [SNCF Landscape](https://sncfoundation.github.io/landscape.html)
- 🧩 [All projects](https://sncfoundation.github.io/projects.html)
- ⚖️ [Governance &amp; how to contribute](https://github.com/sncfoundation/governance)
- 🎓 [Get certified (CSFE)](https://sncfoundation.github.io/certification.html)

## Status legend

Everything starts as an **Unsaved Draft**. It reconciles up the tiers from there — see the
[maturity model](https://sncfoundation.github.io/foundation.html#maturity).

---

<sub>Licensed under Apache-2.0. The SNCF does not recommend running production on a spreadsheet. If you do, please film it.</sub>


## Usage

```bash
# full $0 FinOps report (+ estimated avoided cloud spend)
./sheetfinops
./sheetfinops --rate 0.031 --mem-rate 0.005
```

Config via a `.skctl.env` (same as `skctl`): `WEBAPP_URL`, `TOKEN`. Requires `curl`, `jq`, `bc`.

## What it reports

- Per-Deployment replicas, requested vCPU and memory (summed across replicas).
- The itemized infrastructure bill: **$0** (control plane, storage, egress).
- An estimate of what the same workload would cost on a real cloud — your **avoided spend**.

