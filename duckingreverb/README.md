# DuckingReverb

AUv3 Stereo Ducking Reverb Effect Plugin for macOS and iOS

---

## Overview

DuckingReverb is a stereo reverb plugin that automatically reduces the reverb tail level when the input signal is present — a technique known as "ducking."  
This keeps the dry signal clear and upfront while still delivering a rich, spacious reverb in the gaps between notes or phrases.

---

## Parameters

### Reverb

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| Time | 0.3s – 30.0s | 2.0s | Reverb decay time |
| Pre Delay | 0 – 100 ms | 0 ms | Delay before the reverb tail begins |

### Ducking

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| Threshold | -60 – 0 dB | -24 dB | Input level above which ducking begins |
| Depth | 0 – 100 | 80 | Amount of reverb reduction when ducking is active |
| Attack | 1 – 500 ms | 10 ms | Time for ducking to engage after the signal exceeds the threshold |
| Release | 10 – 2000 ms | 200 ms | Time for the reverb to return to full level after the signal drops below the threshold |

### Master

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| Dry/Wet | 0 – 100 | 50 | Mix balance between dry input and processed signal |

---

## Presets

| # | Name | Time | Threshold | Depth | Attack | Release | Dry/Wet |
|---|------|------|-----------|-------|--------|---------|---------|
| 1 | Preset 1 | 2.0s | -24 dB | 80 | 10 ms | 200 ms | 50 |
| 2 | Preset 2 | 4.5s | -30 dB | 100 | 5 ms | 500 ms | 65 |

---

## Signal Flow

```
Input → Reverb → Ducker → Dry/Wet Mix → Output
```

The ducker monitors the dry input level and attenuates the reverb tail accordingly.  
When the input signal is loud, the reverb is pulled back. When the input falls silent, the reverb blooms back to its full level.

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

DuckingReverbは、入力信号が存在するときにリバーブの残響レベルを自動的に下げる「ダッキング」機能を持つ、macOSおよびiOS向けのステレオリバーブプラグインです。  
ドライ信号をクリアに保ちながら、フレーズの隙間では豊かな空間表現を実現します。

---

## パラメータ

### Reverb（リバーブ）

| パラメータ | 範囲 | デフォルト | 説明 |
|----------|------|-----------|------|
| Time | 0.3s – 30.0s | 2.0s | リバーブの残響時間 |
| Pre Delay | 0 – 100 ms | 0 ms | リバーブが始まるまでの遅延時間 |

### Ducking（ダッキング）

| パラメータ | 範囲 | デフォルト | 説明 |
|----------|------|-----------|------|
| Threshold | -60 – 0 dB | -24 dB | ダッキングが始まる入力レベル |
| Depth | 0 – 100 | 80 | ダッキング時のリバーブ抑圧量 |
| Attack | 1 – 500 ms | 10 ms | 入力がThresholdを超えてからダッキングが効くまでの時間 |
| Release | 10 – 2000 ms | 200 ms | 入力がThreshold以下になってからリバーブが戻るまでの時間 |

### Master

| パラメータ | 範囲 | デフォルト | 説明 |
|----------|------|-----------|------|
| Dry/Wet | 0 – 100 | 50 | ドライ信号とエフェクト音のミックスバランス |

---

## プリセット

| # | 名前 | Time | Threshold | Depth | Attack | Release | Dry/Wet |
|---|------|------|-----------|-------|--------|---------|---------|
| 1 | Preset 1 | 2.0s | -24 dB | 80 | 10 ms | 200 ms | 50 |
| 2 | Preset 2 | 4.5s | -30 dB | 100 | 5 ms | 500 ms | 65 |

---

## 信号フロー

```
入力 → リバーブ → ダッカー → Dry/Wetミックス → 出力
```

ダッカーはドライ入力のレベルを監視し、それに応じてリバーブの残響を抑圧します。  
入力信号が大きいときはリバーブが引っ込み、入力が途切れると残響が自然に戻ってきます。

---

## 動作環境

- macOS 13 以降
- iOS 16 以降
- AUv3対応：Logic Pro、GarageBand

---

## サポート

お問い合わせはこちらまでメールをお送りください：

**contact@knaka.net**
