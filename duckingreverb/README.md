# DuckingReverb

AUv3 Stereo Ducking Reverb Effect Plugin for macOS and iOS

---

## Overview

DuckingReverb is a stereo reverb plugin that automatically reduces the reverb tail level when the input signal is present — a technique known as "ducking."  
This keeps the dry signal clear and upfront while still delivering a rich, spacious reverb in the gaps between notes or phrases.

---

## Parameters

### Ducking

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| Ducking Type | Air / Gentle / Subtle / Room / Push / Tight / Pump | Air | Character of the ducking response. Each type sets the compressor's attack, release, ratio, and gain internally. |
| Comp. Threshold | -50 – 0 dB | -35 dB | Input level above which ducking engages. Lower values mean ducking starts earlier. |

### Reverb

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| HighEQ Gain | -18 – +18 dB | +3 dB | Shelving EQ gain applied to the reverb tail (high frequencies) |
| LowEQ Gain | -18 – +18 dB | -3 dB | Shelving EQ gain applied to the reverb tail (low frequencies) |
| Reverb Time | 0.1 – 10.0 s | 2.0 s | Reverb decay time |

### Master

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| Dry Balance | -50 – +12 dB | 0 dB | Level of the dry (unprocessed) signal |
| Reverb Balance | -50 – +12 dB | -12 dB | Level of the reverb (wet) signal |

---

## Ducking Types

The Ducking Type selector chooses from seven built-in compressor characters. Attack, release, ratio, and gain are set automatically for each type.

| Type | Character | Best for |
|------|-----------|----------|
| Air | Transparent, natural response | Lead vocals |
| Gentle | Smooth, relaxed ducking | Acoustic ensembles |
| Subtle | Very light touch — barely noticeable | Ambient, pads |
| Room | Slow attack, emphasizes space | Room feel, slow passages |
| Push | Assertive, pushes dry signal forward | Guitars, keys |
| Tight | Fast and tight — minimal reverb bleed | Drums, staccato parts |
| Pump | Extreme, intentionally audible pumping | EDM, electronic |

---

## Presets

| # | Name | Ducking Type | Threshold | HighEQ | LowEQ | Reverb Time | Dry Bal | Reverb Bal |
|---|------|-------------|-----------|--------|-------|-------------|---------|------------|
| 1 | Air | Air | -35 dB | +2 dB | -2 dB | 1.8 s | 0 dB | -10 dB |
| 2 | Gentle | Gentle | -30 dB | +1 dB | -1 dB | 2.5 s | 0 dB | -9 dB |
| 3 | Subtle | Subtle | -28 dB | 0 dB | 0 dB | 3.0 s | 0 dB | -8 dB |
| 4 | Room | Room | -32 dB | +3 dB | -3 dB | 2.0 s | 0 dB | -12 dB |
| 5 | Push | Push | -25 dB | +4 dB | -4 dB | 1.5 s | 0 dB | -10 dB |
| 6 | Tight | Tight | -22 dB | +3 dB | -5 dB | 1.2 s | 0 dB | -12 dB |
| 7 | Pump | Pump | -18 dB | +5 dB | -6 dB | 1.0 s | 0 dB | -8 dB |

---

## Signal Flow

```
Input → Reverb (EQ → Decay) → Ducker → Mix (Dry Balance + Reverb Balance) → Output
```

The compressor monitors the dry input signal and attenuates the reverb tail in response.  
When the input is loud, the reverb is pulled back. When the input falls silent, the reverb returns to its full level.  
Dry Balance and Reverb Balance provide independent level control over the two signal paths.

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

### Ducking（ダッキング）

| パラメータ | 範囲 | デフォルト | 説明 |
|----------|------|-----------|------|
| Ducking Type | Air / Gentle / Subtle / Room / Push / Tight / Pump | Air | ダッキングの性格を選択。タイプごとにコンプレッサーのアタック・リリース・レシオ・ゲインが自動設定される |
| Comp. Threshold | -50 – 0 dB | -35 dB | ダッキングが始まる入力レベル。値が低いほど早くダッキングが効き始める |

### Reverb（リバーブ）

| パラメータ | 範囲 | デフォルト | 説明 |
|----------|------|-----------|------|
| HighEQ Gain | -18 – +18 dB | +3 dB | リバーブ音の高域シェルビングEQゲイン |
| LowEQ Gain | -18 – +18 dB | -3 dB | リバーブ音の低域シェルビングEQゲイン |
| Reverb Time | 0.1 – 10.0 s | 2.0 s | リバーブの残響時間 |

### Master

| パラメータ | 範囲 | デフォルト | 説明 |
|----------|------|-----------|------|
| Dry Balance | -50 – +12 dB | 0 dB | ドライ（原音）信号のレベル |
| Reverb Balance | -50 – +12 dB | -12 dB | リバーブ（エフェクト音）のレベル |

---

## Ducking Type

Ducking Typeセレクターで7種類のコンプレッサーキャラクターから選択できます。アタック・リリース・レシオ・ゲインはタイプごとに自動設定されます。

| タイプ | キャラクター | 適した用途 |
|------|------------|---------|
| Air | 透明感のある自然なダッキング | リードボーカル |
| Gentle | なめらかでゆったりとした反応 | アコースティックアンサンブル |
| Subtle | ほとんど気づかない極めて軽い効果 | アンビエント、パッド |
| Room | アタックが遅く空間感を強調 | ルーム感、スローなフレーズ |
| Push | 積極的にドライ信号を前に押し出す | ギター、キーボード |
| Tight | 高速タイト、リバーブの滲みを最小化 | ドラム、スタッカートパート |
| Pump | 意図的に聴かせる強烈なポンピング | EDM、エレクトロニック |

---

## プリセット

| # | 名前 | Ducking Type | Threshold | HighEQ | LowEQ | Reverb Time | Dry Bal | Reverb Bal |
|---|------|-------------|-----------|--------|-------|-------------|---------|------------|
| 1 | Air | Air | -35 dB | +2 dB | -2 dB | 1.8 s | 0 dB | -10 dB |
| 2 | Gentle | Gentle | -30 dB | +1 dB | -1 dB | 2.5 s | 0 dB | -9 dB |
| 3 | Subtle | Subtle | -28 dB | 0 dB | 0 dB | 3.0 s | 0 dB | -8 dB |
| 4 | Room | Room | -32 dB | +3 dB | -3 dB | 2.0 s | 0 dB | -12 dB |
| 5 | Push | Push | -25 dB | +4 dB | -4 dB | 1.5 s | 0 dB | -10 dB |
| 6 | Tight | Tight | -22 dB | +3 dB | -5 dB | 1.2 s | 0 dB | -12 dB |
| 7 | Pump | Pump | -18 dB | +5 dB | -6 dB | 1.0 s | 0 dB | -8 dB |

---

## 信号フロー

```
入力 → リバーブ（EQ → 残響）→ ダッカー → ミックス（Dry Balance + Reverb Balance）→ 出力
```

コンプレッサーはドライ入力信号を監視し、それに応じてリバーブの残響を抑圧します。  
入力が大きいときはリバーブが引っ込み、入力が途切れると残響が自然に戻ってきます。  
Dry BalanceとReverb Balanceにより、2系統のレベルを独立してコントロールできます。

---

## 動作環境

- macOS 13 以降
- iOS 16 以降
- AUv3対応：Logic Pro、GarageBand

---

## サポート

お問い合わせはこちらまでメールをお送りください：

**contact@knaka.net**
