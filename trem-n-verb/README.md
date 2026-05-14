# Trem-N-Verb

AUv3 Stereo Tremolo + Reverb Effect Plugin for macOS and iOS

---

## Overview

Trem-N-Verb is a stereo effect plugin that applies tremolo to the reverb tail.  
The signal flows through reverb first, then tremolo is applied to the reverberated sound — creating a unique rhythmic, spatial texture.

---

## Parameters

### Reverb

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| Reverb SW | ON / OFF | ON | Enables or disables the reverb section |
| Time | 0.3s – 30.0s | 1.2s | Reverb decay time |

### Tremolo

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| Tremolo SW | ON / OFF | ON | Enables or disables the tremolo section |
| Depth | 0 – 100 | 100 | Tremolo modulation depth |
| Rate | Tempo sync (1/64 – 2 bars) / 0 – 20 Hz | 1/16 | LFO rate. Left half of the knob selects a note value synced to host BPM. Right half sets frequency in Hz directly. |
| Phase | 0° – 180° | 180° | Stereo phase offset of the LFO between left and right channels |

### Master

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| Dry/Wet | 0 – 100 | 57 | Mix balance between dry input and processed signal |

---

## Presets

| # | Name | Reverb Time | Rate | Phase | Dry/Wet |
|---|------|-------------|------|-------|---------|
| 1 | Preset 1 | 2.9s | 1/16 (tempo sync) | 180° | 57 |
| 2 | Preset 2 | 4.8s | 3.70 Hz | 90° | 60 |

---

## Signal Flow

```
Input → Reverb → Tremolo → Dry/Wet Mix → Output
```

The tremolo is applied to the reverberated signal, not the dry input.  
Turning Reverb SW off passes the dry signal through the tremolo section instead.

---

## Compatibility

- macOS 13 or later
- iOS 16 or later
- AUv3 compatible: Logic Pro, GarageBand

---

## Support

For support and inquiries, please contact us at:

**contact@knaka.net**

---

## 概要

Trem-N-Verbは、リバーブの残響にトレモロをかけることで独特な効果が得られる、macOSおよびiOS向けのステレオエフェクトプラグインです。

---

## パラメータ

### Reverb（リバーブ）

| パラメータ | 範囲 | デフォルト | 説明 |
|----------|------|-----------|------|
| Reverb SW | ON / OFF | ON | リバーブのオン/オフ |
| Time | 0.3s – 30.0s | 1.2s | リバーブの残響時間 |

### Tremolo（トレモロ）

| パラメータ | 範囲 | デフォルト | 説明 |
|----------|------|-----------|------|
| Tremolo SW | ON / OFF | ON | トレモロのオン/オフ |
| Depth | 0 – 100 | 100 | トレモロの変調深さ |
| Rate | テンポシンク（1/64 – 2小節）/ 0 – 20 Hz | 1/16 | LFOレート。ノブの左半分でホストBPMに同期した音符値を選択、右半分でHz値を直接指定 |
| Phase | 0° – 180° | 180° | 左右チャンネルのLFO位相差 |

### Master

| パラメータ | 範囲 | デフォルト | 説明 |
|----------|------|-----------|------|
| Dry/Wet | 0 – 100 | 57 | ドライ信号とエフェクト音のミックスバランス |

---

## プリセット

| # | 名前 | リバーブタイム | レート | フェーズ | Dry/Wet |
|---|------|--------------|--------|---------|---------|
| 1 | Preset 1 | 2.9s | 1/16（テンポシンク） | 180° | 57 |
| 2 | Preset 2 | 4.8s | 3.70 Hz | 90° | 60 |

---

## 信号フロー

```
入力 → リバーブ → トレモロ → Dry/Wetミックス → 出力
```

トレモロはリバーブ後の信号にかかります。  
Reverb SWをOFFにすると、ドライ信号がトレモロセクションに送られます。

---

## 動作環境

- macOS 13 以降
- iOS 16 以降
- AUv3対応：Logic Pro、GarageBand

---

## サポート

お問い合わせはこちらまでメールをお送りください：

**contact@knaka.net**
