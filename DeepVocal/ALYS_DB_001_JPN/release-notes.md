Thanks to [VOISTAR Project](https://www.voistarproject.com/)'s support, this DeepVocal voicebank was configured by Adlez27 based on ALYS_DB_001_JPN.

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

In Wav Locations, ensure all 6 sample folders have been added.

In Model Symbols, select "All setted symbols in wav locations". Create a new folder for model files and select it with the "Model File Location" button, then press "Build Voice Model Files".

In Build Voice Bank, ensure that all 6 pitches and the singer name has been specified. Use the "Voice Bank Location" button to select the `ALYS\DeepVocal\ALYS_DB_001_JPN\build` folder, then press Build Voice Bank.

The build folder can then be moved to `C:\Program Files (x86)\DeepVocal\singers` to use the voicebank in DeepVocal.

# Usage
A dictionary file has been included for compatibility with both romaji and hiragana lyrics.

If you would like to see all of this voicebank's features in action, download `alys_demo.dv` from below and open the file in DeepVocal.

## Multipitch
There are three full pitches (C4 E4 A4) and three additional vowel-only pitches (A3 G4 C5). It's recommended to cut long notes into a small starting note and long vowel note in order to make use of all six pitches.

## Extra phonemes
Besides standard Japanese syllables, the following extra syllables have been included in this voicebank.

| Consonant | IPA | Romaji | Hiragana | Romaji | Hiragana | Romaji | Hiragana | Romaji | Hiragana | Romaji | Hiragana |
| - | - | - | - | - | - | - | - | - | - | - | - |
| ky | k?? |  |  |  |  |  |  | kye | ?????? |  |  |
| kw | k?? | kwa | ?????? | kwi | ?????? |  |  | kwe | ?????? | kwo | ?????? |
| gy | ???? |  |  |  |  |  |  | gye | ?????? |  |  |
| gw | ???? | gwa | ?????? | gwi | ?????? |  |  | gwe | ?????? | gwo | ?????? |
| s | s |  |  | si | ?????? |  |  |  |  |  |  |
| sh | ?? |  |  |  |  |  |  | she | ?????? |  |  |
| z | z |  |  | zi | ?????? |  |  |  |  |  |  |
| j | d???? |  |  |  |  |  |  | je | ?????? |  |  |
| zh | ?? | zha | ?????? | zhi | ??? | zhu | ?????? | zhe | ?????? | zho | ?????? |
| t | t |  |  | ti | ?????? | tu | ?????? |  |  |  |  |
| ty | t?? | tya | ?????? |  |  | tyu | ?????? | tye | ?????? | tyo | ?????? |
| ch | t???? |  |  |  |  |  |  | che | ?????? |  |  |
| ts | t??s | tsa | ?????? | tsi | ?????? |  |  | tse | ?????? | tso | ?????? |
| d | d |  |  | di | ?????? | du | ?????? |  |  |  |  |
| dy | d?? | dya | ?????? |  |  | dyu | ?????? | dye | ?????? | dyo | ?????? |
| dz | d??z | dza | ?????? | dzi | ?????? | dzu | ??? | dze | ?????? | dzo | ?????? |
| ny | ?? |  |  |  |  |  |  | nye | ?????? |  |  |
| h | h |  |  |  |  | hu | ?????? |  |  |  |  |
| hy | ?? |  |  |  |  |  |  | hye | ?????? |  |  |
| f | ?? | fa | ?????? | fi | ?????? |  |  | fe | ?????? | fo | ?????? |
| fy | ???? | fya | ?????? |  |  | fyu | ?????? | fye | ????????? | fyo | ?????? |
| by | b?? |  |  |  |  |  |  | bye | ?????? |  |  |
| py | p?? |  |  |  |  |  |  | pye | ?????? |  |  |
| my | m?? |  |  |  |  |  |  | mye | ?????? |  |  |
| y | j |  |  | yi | ?????? |  |  | ye | ?????? |  |  |
| ry | ???? |  |  |  |  |  |  | rye | ?????? |  |  |
| l | l | la | ??? | li | ??? | lu | ??? | le | ??? | lo | ??? |
| w | w |  |  | wi | ?????? | wu | ?????? | we | ?????? | wo | ?????? |

## Variant ???
There are 4 different pronunciations of ??? available for different contexts. You must manually specify which variation to use in note lyrics.

| Romaji | Hiragana | Context |
|-|-|-|
| nny | ???ny | Before ny |
| mm | ???m | Before b, by, p, py, m, my |
| ng | ???ng | Before k, ky, kw, g, gy, gw |
| nn | ??? | Everywhere else |

## End breaths
Create a note at the end of a note with the lyric `hh` or `???` for an exhale.

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