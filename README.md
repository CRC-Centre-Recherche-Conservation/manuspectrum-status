<p align="center">
  <a href="https://manuspectrum.huma-num.fr/">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="./assets/logo-manuspectrum-dark.svg">
      <img alt="ManuSpectrum" src="./assets/logo-manuspectrum-light.svg" width="460">
    </picture>
  </a>
</p>

<p align="center">
  <strong>Status of <a href="https://manuspectrum.huma-num.fr/">manuspectrum.huma-num.fr</a></strong><br>
  An independent probe, run from GitHub every hour, outside the server it watches.
</p>

<p align="center">
  <a href="https://crc-centre-recherche-conservation.github.io/manuspectrum-status/"><img alt="Website uptime" src="https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2FCRC-Centre-Recherche-Conservation%2Fmanuspectrum-status%2FHEAD%2Fapi%2Fwebsite%2Fuptime.json&label=website"></a>
  <a href="https://crc-centre-recherche-conservation.github.io/manuspectrum-status/"><img alt="Response time" src="https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2FCRC-Centre-Recherche-Conservation%2Fmanuspectrum-status%2FHEAD%2Fapi%2Fwebsite%2Fresponse-time.json&label=response%20time"></a>
  <a href="https://github.com/CRC-Centre-Recherche-Conservation/manuspectrum-status/issues?q=label%3Astatus"><img alt="Incidents" src="https://img.shields.io/github/issues/CRC-Centre-Recherche-Conservation/manuspectrum-status/status?label=open%20incidents"></a>
</p>

### Current status: <!--live status--> **🟩 All systems operational**

**[Open the status page →](https://crc-centre-recherche-conservation.github.io/manuspectrum-status/)**

<!--start: status pages-->
<!--end: status pages-->

## About ManuSpectrum

[ManuSpectrum](https://manuspectrum.huma-num.fr/) is an open database of the physico-chemical analyses of medieval
manuscripts (X-ray fluorescence and its imaging, reflectance and infrared spectroscopy, mass
spectrometry), linked to the IIIF images of the folios they were made on. It is developed by the
[Centre de Recherche sur la Conservation](https://crc.mnhn.fr/) (CNRS, MNHN, Ministère de la Culture), built on
[Arches](https://www.archesproject.org/) and hosted by [Huma-Num](https://www.huma-num.fr/).

## What is checked

| Check | What it means | Degraded above |
| --- | --- | --- |
| **Website** | The home page answers (the language redirect is followed). | 15 s |
| **Liveness** | The application server answers `/healthz`, a page with no dependency. | 5 s |
| **TLS certificate** | The certificate is valid for more than 7 more days. | — |

The probe runs every hour from GitHub's servers. The host has its own, finer monitoring (databases, search,
image server, backups); this repository only answers one question from the outside: *can a visitor reach the site?*

## Incidents and maintenance

- When a check fails twice in a row, the probe opens an [issue](https://github.com/CRC-Centre-Recherche-Conservation/manuspectrum-status/issues?q=label%3Astatus)
  and assigns the maintainers; it closes it when the site is back. The issues form the public incident history.
- A planned update is announced beforehand with a
  [maintenance issue](https://github.com/CRC-Centre-Recherche-Conservation/manuspectrum-status/issues/new?template=maintainance-event.md)
  (label `maintenance`, start and end times, checks expected down). During that window a failed check is recorded
  but opens no incident, and the status page shows the maintenance.

## How it works

The checks, the history (`history/`), the badges (`api/`), the graphs (`graphs/`) and the status page are produced by
[Upptime](https://upptime.js.org/) with GitHub Actions, Issues and Pages, from a single configuration file,
[`.upptimerc.yml`](./.upptimerc.yml). The workflows in `.github/workflows` are generated from it: edit the
configuration, never the workflows.

## License

- Probe: [Upptime](https://github.com/upptime/upptime), [MIT](./LICENSE).
- Data in `history/`: [Open Database License](https://opendatacommons.org/licenses/odbl/1-0/).
- ManuSpectrum logo: © Centre de Recherche sur la Conservation.
