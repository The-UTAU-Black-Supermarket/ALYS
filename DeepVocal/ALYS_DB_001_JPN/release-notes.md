Thanks to VOISTAR Project's support, this DeepVocal voicebank was configured by Adlez27 based on ALYS_DB_001_JPN.

# Installation
Scroll down and download the file `ALYS_JPN_1.zip`. Unzip the file, then move the resulting `ALYS JPN 1` folder to `C:\Program Files (x86)\DeepVocal\singers`.

# Compiling from source
This is a completely OPTIONAL choice for those who want to modify the voicebank instead of using the precompiled version.

Clone this git repository locally.  
Download and install [DeepVocal ToolBox](https://deep-vocal.com/#/Product).  

Navigate to `ALYS\DeepVocal\ALYS_DB_001_JPN` and open `jpn1.dvtb` using DeepVocal ToolBox.  
Go to Function > Build Voice Bank. 

<!-- TODO: update screenshot -->
![screenshot](build-vb.png)

In Wav Locations, ensure all six sample folders have been added.

In Model Symbols, select "All setted symbols in wav locations". Create a new folder for model files and select it with the "Model File Location" button, then press "Build Voice Model Files".

In Build Voice Bank, ensure that all three pitches and the singer name has been specified. Use the "Voice Bank Location" button to select the `ALYS\DeepVocal\ALYS_DB_001_JPN\build` folder, then press Build Voice Bank.

The build folder can then be moved to `C:\Program Files (x86)\DeepVocal\singers` to use the voicebank in DeepVocal.

# Usage
A dictionary file has been included for compatibility with both romaji and hiragana lyrics.

## Multipitch
There are three full pitches (C4 E4 A4) and three additional vowel-only pitches (A3 G4 C5). It's recommended to cut long notes into a small starting note and long vowel note in order to make use of all six pitches.

## Extra phonemes
Besides standard Japanese syllables, the following extra syllables have been included in this voicebank.

| Romaji | Hiragana |
| - | - |
| kye | きぇ |
| kwa | くぁ |
| kwi | くぃ |
| kwe | くぇ |
| kwo | くぉ |
| gye | ぎぇ |
| gwa | ぐぁ |
| gwi | ぐぃ |
| gwe | ぐぇ |
| gwo | ぐぉ |
| si | すぃ |
| she | しぇ |
| zi | ずぃ |
| je | じぇ |
| zha | ジャ |
| zhi | ジ |
| zhu | ジュ |
| zhe | ジェ |
| zho | ジョ |
| ti | てぃ |
| tu | とぅ |
| tya | てゃ |
| tyu | てゅ |
| tye | てぇ |
| tyo | てょ |
| che | ちぇ |
| tsa | つぁ |
| tsi | つぃ |
| tse | つぇ |
| tso | つぉ |
| di | でぃ |
| du | どぅ |
| dya | でゃ |
| dyu | でゅ |
| dye | でぇ |
| dyo | でょ |
| dza | づぁ |
| dzi | づぃ |
| dzu | づ |
| dze | づぇ |
| dzo | づぉ |
| nye | にぇ |
| hu | ほぅ |
| hye | ひぇ |
| fa | ふぁ |
| fi | ふぃ |
| fe | ふぇ |
| fo | ふぉ |
| fya | ふゃ |
| fyu | ふゅ |
| fye | ふぃぇ |
| fyo | ふょ |
| bye | びぇ |
| pye | ぴぇ |
| mye | みぇ |
| yi | いぃ |
| ye | いぇ |
| rye | りぇ |
| la | ラ |
| li | リ |
| lu | ル |
| le | レ |
| lo | ロ |
| wi | うぃ |
| wu | うぅ |
| we | うぇ |
| wo | うぉ |

## Variant ん
There are 4 different pronunciations of ん available for different contexts. You must manually specify which variation to use in note lyrics.

| Romaji | Hiragana | Context |
|-|-|-|
| nny | んny | Before ny |
| mm | んm | Before b, by, p, py, m, my |
| ng | んng | Before k, ky, kw, g, gy, gw |
| nn | ん | Everywhere else |

## End breaths
Create a note at the end of a note with the lyric `hh` or `息` for an exhale.

![screenshot](end-breath.png)

## Ending consonants
Similar to end breaths, you can put a single consonant at the end of a note, written in all caps. You cannot use consonants as isolated notes, or as consonant clusters. The following consonants can be used.

![screenshot](end-consonant.png)

```
K KY KW G GY GW
S SH Z J ZH
T TY CH TS D DY DZ
N NY
H HY F FY B BY P PY
M MY
Y
R RY L
W
```