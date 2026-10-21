# Small-carrier ELD directory

A starting-point directory of electronic logging device (ELD) providers for small U.S. motor carriers. “Small carrier” is used here as a practical audience description for owner-operators and carriers operating 1–20 power units; it is not a legal or regulatory classification. This directory lists ELD vendors, not motor carriers.

Applicability and exceptions under the federal hours-of-service rules depend on a carrier's circumstances. Consult FMCSA guidance or a qualified compliance professional.

## Verify the exact device

FMCSA registration is device-specific and can change. A provider’s marketing claim, an older directory, or another model from the same vendor is not enough to establish that a device is currently registered. FMCSA does not endorse or certify listed products. Before purchase or use, search the [FMCSA Registered ELDs list](https://eld.fmcsa.dot.gov/List) for the exact device/model and provider, and check its current status and any revocation or other FMCSA notices. See [FMCSA ELD information](https://www.fmcsa.dot.gov/hours-service/elds) for federal requirements.

## Browse the directory

Open [`docs/index.html`](docs/index.html) (search and filter, no build step). It loads [`docs/vendors.json`](docs/vendors.json), which lists every registered and revoked device per provider with model, software version and ELD ID.

## FMCSA verification (checked 2026-10-21)

Each provider below was matched against the official [FMCSA Registered ELD list](https://eld.fmcsa.dot.gov/List) and [revoked list](https://eld.fmcsa.dot.gov/List/GetListOfELDs?listType=Revoked). "Verified" means the provider has at least one device currently registered; it does not mean every product of theirs is registered. Prices, service areas and hardware compatibility are not verified — confirm with the provider.

| Provider | FMCSA provider name | Status | Registered devices | Revoked devices | Checked |
| --- | --- | --- | --- | --- | --- |
| BigRoad | BigRoad Inc | Verified - registered devices listed | 7 | 0 | 2026-10-21 |
| Blue Ink Technology (BIT) | Blue Ink Tech | Verified - registered devices listed | 7 | 0 | 2026-10-21 |
| Geotab | Geotab Inc. | Verified - registered devices listed | 6 | 0 | 2026-10-21 |
| HOS247 | HOS247 LLC | Verified - registered devices listed | 5 | 1 | 2026-10-21 |
| J. J. Keller | J. J. Keller & Associates, Inc. | Verified - registered devices listed | 7 | 3 | 2026-10-21 |
| Motive | Motive Technologies, Inc. | Verified - registered devices listed | 1 | 0 | 2026-10-21 |
| Samsara | Samsara Inc. | Verified - registered devices listed | 2 | 0 | 2026-10-21 |
| TruckX | TruckX Inc | Verified - registered devices listed | 3 | 1 | 2026-10-21 |

## Contributing and maintaining listings

Open an issue or pull request to suggest a provider or update an entry. Include:

- Provider name, product name, and exact FMCSA-listed device name and identifier.
- The FMCSA registry entry and direct provider product/contact sources.
- U.S. service area, hardware and vehicle/mobile-device requirements, and current pricing only when supported by a primary source.
- The date each detail was checked.

Check the official FMCSA list for the exact device before adding or refreshing a listing. Mark an entry unverified if the device is missing, revoked, or cannot be matched, and link any relevant FMCSA notice. Recheck entries periodically and when a change is reported. Keep descriptions factual, avoid copying vendor marketing text, and do not imply FMCSA endorsement or present this directory as legal or compliance advice.

### Updating the data

Edit `docs/vendors.json` (one object per provider; keep `source`, `checked` and device `eld_id` fields), re-check against both FMCSA lists, and update the table above. Preview locally with `python3 -m http.server -d docs` and open http://localhost:8000.
