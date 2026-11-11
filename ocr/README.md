# ocr

Self-hosted [Tesseract.js](https://github.com/naptha/tesseract.js) 7.0.0 assets for Plug Source v4.82+.

Used only when someone takes or picks a photo of a hazard placard or orange panel in the ERG search. The service worker caches these files in `ps-media-v1` after the first load so reading works offline.

| File | Role |
| --- | --- |
| `tesseract.min.js` | Browser API |
| `worker.min.js` | Web worker |
| `tesseract-core-lstm.wasm.js` | WASM core (no SIMD) |
| `tesseract-core-simd-lstm.wasm.js` | WASM core (SIMD) |
| `tesseract-core-relaxedsimd-lstm.wasm.js` | WASM core (relaxed SIMD) |
| `eng.traineddata.gz` | English LSTM data (`@tesseract.js-data/eng` 4.0.0_best_int) |

Legacy (non-LSTM) cores are omitted to keep the download small. Tesseract.js picks the SIMD variant that the device supports.

Licenses: Apache-2.0 (see `LICENSE-tesseract-js.md` and `LICENSE-tesseract-core`).
