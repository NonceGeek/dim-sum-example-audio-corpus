# Dim Sum Example Audio Corpus

A sample Cantonese (Yue Chinese) audio corpus with transcriptions, romanization, and scenario labels. Each audio file is paired with metadata in CSV format.

## Contents

| File | Description |
|------|-------------|
| `*.wav` | Audio recordings named by ID (e.g. `00020.wav`) |
| `examples.csv` | Sample entries with text, pinyin, and scenario labels |
| `scenarioes.csv` | Scenario taxonomy extracted from the full corpus index |
| `LICENSE` | Apache License 2.0 |

## Audio Format

- Format: WAV (RIFF PCM)
- Channels: mono
- Sample rate: 22050 Hz
- Bit depth: 16-bit

## CSV Schema

### `examples.csv`

| Column | Description |
|--------|-------------|
| 序号 | Entry ID; matches the numeric prefix of the corresponding `.wav` file |
| 粤语文本 | Cantonese text |
| 普通话文本 | Mandarin translation |
| 拼音 | Jyutping romanization (Hong Kong Linguistic Society scheme) |
| 场景 | Scenario label |

### `scenarioes.csv`

| Column | Description |
|--------|-------------|
| 场景 | Scenario name |
| 父场景 | Parent scenario (for sub-scenarios) |
| 条目数 | Number of entries in the full corpus for this scenario |

## Usage

Audio files are referenced by ID. For example, the row with 序号 `20` in `examples.csv` corresponds to `00020.wav`.

```text
00020.wav  ←→  examples.csv row where 序号 = 20
```

## Scenarios

The corpus covers everyday Cantonese dialogue across many situations, including greetings, dining, shopping, travel, healthcare, banking, and more. See `scenarioes.csv` for the full list of scenarios and sub-scenarios.

## License

Licensed under the [Apache License 2.0](LICENSE).
