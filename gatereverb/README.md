# GateReverb

AUv3 Gated Reverb Effect Plugin for macOS and iOS

---

## Overview

GateReverb is a reverb plugin whose tail is shaped by a gate — a technique that lets the wet signal open and close with the dynamics of the input instead of trailing off in a long, smeared decay.  
The gate listens to the input signal and controls only the reverb return, so the dry signal always passes through untouched while the reverb itself becomes tight, rhythmic, and fully controllable.

---

## Parameters

### Gate

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| Threshold | -55 – -10 dB | -32 dB | Input level above which the gate opens. Lower values mean the gate opens more easily. |
| Attack | 1 – 4000 ms | 8 ms | How quickly the reverb appears once the gate opens. |
| Release | 1 – 5000 ms | 350 ms | How quickly the reverb tail is cut off once the gate closes. |

### Reverb

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| High Damp | 200 – 20000 Hz | 4000 Hz | Tames or brightens the top end of the reverb tail. |
| Dry Level | 0 – 100 % | 82 % | Level of the dry (unprocessed) signal. |
| Reverb Level | 0 – 100 % | 28 % | Level of the gated reverb (wet) signal. |

---

## Presets

| # | Name | Threshold | Attack | Release | High Damp | Dry Level | Reverb Level |
|---|------|-----------|--------|---------|-----------|-----------|--------------|
| 1 | Vocal Air | -32 dB | 8 ms | 350 ms | 4000 Hz | 82 % | 28 % |
| 2 | Vocal Spotlight | -28 dB | 5 ms | 900 ms | 6000 Hz | 70 % | 45 % |
| 3 | Drum Snap | -20 dB | 1 ms | 120 ms | 9000 Hz | 85 % | 22 % |
| 4 | Drum Pump | -16 dB | 1 ms | 60 ms | 11000 Hz | 65 % | 50 % |
| 5 | Bus Glue | -38 dB | 25 ms | 500 ms | 5000 Hz | 78 % | 25 % |
| 6 | Bus Bloom | -34 dB | 15 ms | 1400 ms | 8000 Hz | 60 % | 48 % |
| 7 | Subtle Texture | -45 dB | 40 ms | 180 ms | 3000 Hz | 88 % | 15 % |
| 8 | Extreme Gate | -14 dB | 1 ms | 40 ms | 10000 Hz | 50 % | 60 % |

---

## Signal Flow

```
Input → Reverb (Plate, High Damp) → Gate → Mix (Dry Level + Reverb Level) → Output
```

The gate monitors the dry input signal and controls only the reverb return.  
When the input crosses the Threshold, the gate opens and the reverb fades in over the Attack time. When the input falls back below the threshold, the reverb tail is cut off over the Release time.  
Dry Level and Reverb Level provide independent level control over the two signal paths.

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

GateReverbは、残響をゲートで制御するリバーブプラグインです。ウェット成分が入力のダイナミクスに合わせて開閉することで、だらだらと尾を引く残響ではなく、タイトでリズミカルな空間を作り出します。  
ゲートは入力信号を検知してリバーブの戻り成分だけをコントロールするため、ドライ信号は常にそのまま通過し、リバーブ自体は自在にコントロールできます。

---

## パラメータ

### Gate（ゲート）

| パラメータ | 範囲 | デフォルト | 説明 |
|----------|------|-----------|------|
| Threshold | -55 – -10 dB | -32 dB | ゲートが開く入力レベル。値が低いほどゲートが開きやすくなる |
| Attack | 1 – 4000 ms | 8 ms | ゲートが開いてからリバーブが立ち上がる速さ |
| Release | 1 – 5000 ms | 350 ms | ゲートが閉じてからリバーブの尾が切れる速さ |

### Reverb（リバーブ）

| パラメータ | 範囲 | デフォルト | 説明 |
|----------|------|-----------|------|
| High Damp | 200 – 20000 Hz | 4000 Hz | リバーブ残響の高域を抑える・明るくする |
| Dry Level | 0 – 100 % | 82 % | ドライ（原音）信号のレベル |
| Reverb Level | 0 – 100 % | 28 % | ゲートされたリバーブ（エフェクト音）のレベル |

---

## プリセット

| # | 名前 | Threshold | Attack | Release | High Damp | Dry Level | Reverb Level |
|---|------|-----------|--------|---------|-----------|-----------|--------------|
| 1 | Vocal Air | -32 dB | 8 ms | 350 ms | 4000 Hz | 82 % | 28 % |
| 2 | Vocal Spotlight | -28 dB | 5 ms | 900 ms | 6000 Hz | 70 % | 45 % |
| 3 | Drum Snap | -20 dB | 1 ms | 120 ms | 9000 Hz | 85 % | 22 % |
| 4 | Drum Pump | -16 dB | 1 ms | 60 ms | 11000 Hz | 65 % | 50 % |
| 5 | Bus Glue | -38 dB | 25 ms | 500 ms | 5000 Hz | 78 % | 25 % |
| 6 | Bus Bloom | -34 dB | 15 ms | 1400 ms | 8000 Hz | 60 % | 48 % |
| 7 | Subtle Texture | -45 dB | 40 ms | 180 ms | 3000 Hz | 88 % | 15 % |
| 8 | Extreme Gate | -14 dB | 1 ms | 40 ms | 10000 Hz | 50 % | 60 % |

---

## 信号フロー

```
入力 → リバーブ（Plate, High Damp）→ ゲート → ミックス（Dry Level + Reverb Level）→ 出力
```

ゲートはドライ入力信号を監視し、リバーブの戻り成分だけをコントロールします。  
入力がThresholdを超えるとゲートが開き、Attackの時間をかけてリバーブがフェードインします。入力がThreshold以下に戻るとゲートが閉じ、Releaseの時間をかけてリバーブの尾が切れていきます。  
Dry LevelとReverb Levelにより、2系統のレベルを独立してコントロールできます。

---

## 動作環境

- macOS 13 以降
- iOS 16 以降
- AUv3対応：Logic Pro、GarageBand

---

## サポート

お問い合わせはこちらまでメールをお送りください：

**contact@knaka.net**
