---
title: "吉他樂理學習筆記"
date: 2026-09-01 00:00:00 +0800
tags: [guitar, music-theory]
---

> 這份筆記以「先理解樂理，再對應到指板，最後應用在樂器上」為主軸

指板圖片使用 [fretboardgtr](https://github.com/Chienweichih/fretboardgtr) 生成

## 目錄

- [網路資源](#網路資源)
- [音高、空弦音與音程](#音高空弦音與音程)
- [音階與調式](#音階與調式)
- [和弦組成公式、和弦級數與和弦進行](#和弦)
- [吉他常用和弦](#吉他常用和弦)
- [烏克麗麗常用和弦](#烏克麗麗常用和弦)
- [指板系統與 CAGED](#指板系統)

---

# 網路資源

### YouTube

1. [Do This for 6 Minutes Each Day!](https://youtu.be/3hTPvNQlegw)
2. [The Guitar Exercise that Changed My Life](https://youtu.be/zROZNaKeDmo)
3. [Every chord is actually just 1 shape](https://youtu.be/LblEV3P0JQY)

### 好和弦文章

1. [一次搞懂所有的現代和弦代號！](https://nicechord.com/post/chord-symbols/)
2. [一次搞懂音程名稱！](https://nicechord.com/post/interval/)
3. [什麼是大調和小調？](https://nicechord.com/post/major-and-minor-modes/)
4. [搞懂七種調式，以及永遠把它們的名字記起來！](https://nicechord.com/post/7-modes/)
5. [什麼是「五聲音階」？](https://nicechord.com/post/pentatonic-scale/)
6. [一篇文章之內，真的完全搞懂「五度圈」！](https://nicechord.com/post/circle-of-fifths/)

### 好和弦線上工具

1. [音樂名詞查詢器](https://nicechord.com/terms/)
2. [和弦代號查詢器](https://nicechord.com/chordfinder/)
3. [音程計算器](https://nicechord.com/interval/)
4. [文字移調器](https://nicechord.com/transpose/)
5. [節拍器](https://nicechord.com/metro3/)
6. [調音器](https://nicechord.com/tuner/)
7. [音樂靈感隨機產生器](https://nicechord.com/NiceIdea/)
8. [鋼琴鍵盤顯示器](https://nicechord.com/pianometer/)

### 資訊與樂譜

1. [all-guitar-chords](https://www.all-guitar-chords.com/)
2. [chord-c](https://chord-c.com/guitar-chord/A/major/)
3. [ukulele-chords](https://ukulele-chords.com/soprano/)
4. [#fretflip](https://fretflip.com)
5. [吉他島嶼](https://gtisland.com/posts/)
6. [Easy Guitar Tabs](https://www.freeguitarmusic.net/easy-tabs)
7. [Traditional Songs](https://www.traditionalsongs.org/overview.html)

---

# 音高、空弦音與音程

本表將吉他音名、唱名、頻率、烏克麗麗弦位與半音音程放在同一張對照表，方便查找

| 吉他琴弦 | 音名 | 唱名 | 頻率 (Hz) | 烏克麗麗 | 半音數 | 音程               |
| :------: | :--: | :--: | :-------: | :------: | :----: | ------------------ |
| 6        | E2   | Mi   | 82.41     |          |        |                    |
|          | F2   | Fa   | 87.31     |          |        |                    |
|          |      |      |           |          |        |                    |
|          | G2   | Sol  | 98.00     |          |        |                    |
|          |      |      |           |          |        |                    |
| 5        | A2   | La   | 110.00    |          |        |                    |
|          |      |      |           |          |        |                    |
|          | B2   | Ti   | 123.47    |          |        |                    |
|          | C3   | Do   | 130.81    |          | 0      | Perfect Unison     |
|          |      |      |           |          | 1      | Minor Second       |
| 4        | D3   | Re   | 146.83    |          | 2      | Major Second       |
|          |      |      |           |          | 3      | Minor Third        |
|          | E3   | Mi   | 164.81    |          | 4      | Major Third        |
|          | F3   | Fa   | 174.61    |          | 5      | Perfect Fourth     |
|          |      |      |           |          | 6      | Diminished Fifth   |
| 3        | G3   | Sol  | 196.00    | 4 Low    | 7      | Perfect Fifth      |
|          |      |      |           |          | 8      | Minor Sixth        |
|          | A3   | La   | 220.00    |          | 9      | Major Sixth        |
|          |      |      |           |          | 10     | Minor Seventh      |
| 2        | B3   | Ti   | 246.94    |          | 11     | Major Seventh      |
|          | C4   | Do   | 261.63    | 3        | 12     | Perfect Octave     |
|          |      |      |           |          | 13     | Minor Ninth        |
|          | D4   | Re   | 293.66    |          | 14     | Major Ninth        |
|          |      |      |           |          | 15     | Minor Tenth        |
| 1        | E4   | Mi   | 329.63    | 2        | 16     | Major Tenth        |
|          | F4   | Fa   | 349.23    |          | 17     | Perfect Eleventh   |
|          |      |      |           |          | 18     | Augmented Eleventh |
|          | G4   | Sol  | 392.00    | 4 High   | 19     | Perfect Twelfth    |
|          |      |      |           |          | 20     | Minor Thirteenth   |
|          | A4   | La   | 440.00    | 1        | 21     | Major Thirteenth   |
|          |      |      |           |          | 22     | Minor Fourteenth   |
|          | B4   | Ti   | 493.88    |          | 23     | Major Fourteenth   |
|          | C5   | Do   | 523.25    |          | 24     | Perfect Fifteenth  |
|          |      |      |           |          |        |                    |
|          | D5   | Re   | 587.33    |          |        |                    |
|          |      |      |           |          |        |                    |
|          | E5   | Mi   | 659.26    |          |        |                    |
|          | F5   | Fa   | 698.46    |          |        |                    |
|          |      |      |           |          |        |                    |
|          | G5   | Sol  | 783.99    |          |        |                    |
|          |      |      |           |          |        |                    |
|          | A5   | La   | 880.00    |          |        |                    |
|          |      |      |           |          |        |                    |
|          | B5   | Ti   | 987.77    |          |        |                    |
|          | C6   | Do   | 1046.50   |          |        |                    |
|          |      |      |           |          |        |                    |
|          | D6   | Re   | 1174.66   |          |        |                    |

# 音階與調式

## 七種教會調式音階

| Ionian | Dorian | Phrygian | Lydian | Mixolydian | Aeolian | Locrian |
| :----: | :----: | :------: | :----: | :--------: | :-----: | :-----: |
|   C    |   D    |   E      |   F    |   G        |   A     |   B     |
|   D    |   E    |   F      |   G    |   A        |   B     |   C     |
|   E    |   F    |   G      |   A    |   B        |   C     |   D     |
|   F    |   G    |   A      |   B    |   C        |   D     |   E     |
|   G    |   A    |   B      |   C    |   D        |   E     |   F     |
|   A    |   B    |   C      |   D    |   E        |   F     |   G     |
|   B    |   C    |   D      |   E    |   F        |   G     |   A     |
|   C    |   D    |   E      |   F    |   G        |   A     |   B     |

| Major | Lydian | Mixolydian | Minor | Dorian | Phrygian | Locrian |
| :---: | :----: | :--------: | :---: | :----: | :------: | :-----: |
|   C   |   C    |   C        |   C   |   C    |   C      |   C     |
|   D   |   D    |   D        |   D   |   D    |   Db     |   Db    |
|   E   |   E    |   E        |   Eb  |   Eb   |   Eb     |   Eb    |
|   F   |   F#   |   F        |   F   |   F    |   F      |   F     |
|   G   |   G    |   G        |   G   |   G    |   G      |   Gb    |
|   A   |   A    |   A        |   Ab  |   A    |   Ab     |   Ab    |
|   B   |   B    |   Bb       |   Bb  |   Bb   |   Bb     |   Bb    |

> 第一個表格是用 C 大調的音符排列  
> 第二個表格是從 C 開始，方便比較調式之間的差異  
> 自然大調就是 Ionian  
> 自然小調就是 Aeolian

<div style="break-after:page"></div>
<div style="break-after:page"></div>

# 和弦

## 和弦組成公式

| 和弦類型        | 符號   | 組成音程 (度數) |   |    |    |    |   |
| --------------- | :----: | :-------------: |:-:|:--:|:--:|:--:|:-:|
| Major           | C      | 1 3 5           | C | E  | G  |    |   |
| Major 7th       | Cmaj7  | 1 3 5 7         | C | E  | G  | B  |   |
| Major 9th       | Cmaj9  | 1 3 5 7 9       | C | E  | G  | B  | D |
| Sixth           | C6     | 1 3 5 6         | C | E  | G  | A  |   |
| Seventh         | C7     | 1 3 5 b7        | C | E  | G  | Bb |   |
| Dominant 9th    | C9     | 1 3 5 b7 9      | C | E  | G  | Bb | D |
| Added 9th       | Cadd9  | 1 3 5 9         | C | E  | G  | D  |   |
| Augmented       | Caug   | 1 3 #5          | C | E  | G# |    |   |
| Augmented 7th   | C7+5   | 1 3 #5 b7       | C | E  | G# | Bb |   |
| Suspended 2nd   | Csus2  | 1 2 5           | C | D  | G  |    |   |
| Suspended 4th   | Csus4  | 1 4 5           | C | F  | G  |    |   |
| Dom. 7 Sus. 4th | C7sus4 | 1 4 5 b7        | C | F  | G  | Bb |   |
| minor           | Cm     | 1 b3 5          | C | Eb | G  |    |   |
| minor 6th       | Cm6    | 1 b3 5 6        | C | Eb | G  | A  |   |
| minor 7th       | Cm7    | 1 b3 5 b7       | C | Eb | G  | Bb |   |
| minor 9th       | Cm9    | 1 b3 5 b7 9     | C | Eb | G  | Bb | D |
| Diminished      | Cdim   | 1 b3 b5         | C | Eb | Gb |    |   |
| Dim. 7th        | Cdim7  | 1 b3 b5 bb7     | C | Eb | Gb | A  |   |
| Half-dim. 7th   | Cm7b5  | 1 b3 b5 b7      | C | Eb | Gb | Bb |   |

## 自然大調和弦級數表

| 級數   | 羅馬數字 | 和弦性質 | C 大調 | 組成音 |
| :----: | :------: | :------: | :----: | :----: |
| 第一級 | I        | 大三和弦 | C      | C E G  |
| 第二級 | ii       | 小三和弦 | Dm     | D F A  |
| 第三級 | iii      | 小三和弦 | Em     | E G B  |
| 第四級 | IV       | 大三和弦 | F      | F A C  |
| 第五級 | V        | 大三和弦 | G      | G B D  |
| 第六級 | vi       | 小三和弦 | Am     | A C E  |
| 第七級 | vii°     | 減三和弦 | Bdim   | B D F  |

## 常見和弦進行

| 名稱     | 和弦進行        | 級數              | 風格      |
| :------: | :-------------: | :---------------: | :-------: |
| 流行經典 | C - G - Am - F  | I - V - vi - IV   | 青春 流行 |
| 抒情常用 | Am - F - C - G  | vi - IV - I - V   | 溫柔 抒情 |
| 經典老歌 | C - Am - F - G  | I - vi - IV - V   | 懷舊 浪漫 |
| 明亮開朗 | C - F - G - C   | I - IV - V - I    | 陽光 開心 |
| 柔和抒情 | C - Em - Am - F | I - iii - vi - IV | 溫柔 感性 |
| 小調進行 | Am - G - F - G  | vi - V - IV - V   | 悲傷 深情 |
| 經典流行 | C - Am - Dm - G | I - vi - ii - V   | 流行 復古 |

<div style="break-after:page"></div>

# 吉他常用和弦

## 指板和弦圖

![][G_C_Major]

| C | C7 | Cmaj7 | Cadd9 |
|:---:|:---:|:---:|:---:|
| [![][G_Chords_C]][G_Pics_C] | [![][G_Chords_C7]][G_Pics_C7] | [![][G_Chords_Cmaj7]][G_Pics_Cmaj7] | [![][G_Chords_Cadd9]][G_Pics_Cadd9] |

| A | Am | A7 | Am7 |
|:---:|:---:|:---:|:---:|
| [![][G_Chords_A]][G_Pics_A] | [![][G_Chords_Am]][G_Pics_Am] | [![][G_Chords_A7]][G_Pics_A7] | [![][G_Chords_Am7]][G_Pics_Am7] |

| B | Bm | B7 | Bm7 |
|:---:|:---:|:---:|:---:|
| [![][G_Chords_B]][G_Pics_B] | [![][G_Chords_Bm]][G_Pics_Bm] | [![][G_Chords_B7]][G_Pics_B7] | [![][G_Chords_Bm7]][G_Pics_Bm7] |

| G | G7 | Gmaj7 | Gsus4 |
|:---:|:---:|:---:|:---:|
| [![][G_Chords_G]][G_Pics_G] | [![][G_Chords_G7]][G_Pics_G7] | [![][G_Chords_Gmaj7]][G_Pics_Gmaj7] | [![][G_Chords_Gsus4]][G_Pics_Gsus4] |

| E | Em | E7 | Em7 |
|:---:|:---:|:---:|:---:|
| [![][G_Chords_E]][G_Pics_E] | [![][G_Chords_Em]][G_Pics_Em] | [![][G_Chords_E7]][G_Pics_E7] | [![][G_Chords_Em7]][G_Pics_Em7] |

| F | Fm | F7 | Fmaj7 |
|:---:|:---:|:---:|:---:|
| [![][G_Chords_F]][G_Pics_F] | [![][G_Chords_Fm]][G_Pics_Fm] | [![][G_Chords_F7]][G_Pics_F7] | [![][G_Chords_Fmaj7]][G_Pics_Fmaj7] |

| D | Dm | D7 | Dm7 |
|:---:|:---:|:---:|:---:|
| [![][G_Chords_D]][G_Pics_D] | [![][G_Chords_Dm]][G_Pics_Dm] | [![][G_Chords_D7]][G_Pics_D7] | [![][G_Chords_Dm7]][G_Pics_Dm7] |

<div style="break-after:page"></div>

# 烏克麗麗常用和弦

## 指板和弦圖

![][U_C_Major]

| F | F7 | Fmaj7 | Fadd9 |
|:---:|:---:|:---:|:---:|
| [![][U_Chords_F]][U_Pics_F] | [![][U_Chords_F7]][U_Pics_F7] | [![][U_Chords_Fmaj7]][U_Pics_Fmaj7] | [![][U_Chords_Fadd9]][U_Pics_Fadd9] |

| D | Dm | D7 | Dm7 |
|:---:|:---:|:---:|:---:|
| [![][U_Chords_D]][U_Pics_D] | [![][U_Chords_Dm]][U_Pics_Dm] | [![][U_Chords_D7]][U_Pics_D7] | [![][U_Chords_Dm7]][U_Pics_Dm7] |

| E | Em | E7 | Em7 |
|:---:|:---:|:---:|:---:|
| [![][U_Chords_E]][U_Pics_E] | [![][U_Chords_Em]][U_Pics_Em] | [![][U_Chords_E7]][U_Pics_E7] | [![][U_Chords_Em7]][U_Pics_Em7] |

| C | C7 | Cmaj7 | Csus4 |
|:---:|:---:|:---:|:---:|
| [![][U_Chords_C]][U_Pics_C] | [![][U_Chords_C7]][U_Pics_C7] | [![][U_Chords_Cmaj7]][U_Pics_Cmaj7] | [![][U_Chords_Csus4]][U_Pics_Csus4] |

| A | Am | A7 | Am7 |
|:---:|:---:|:---:|:---:|
| [![][U_Chords_A]][U_Pics_A] | [![][U_Chords_Am]][U_Pics_Am] | [![][U_Chords_A7]][U_Pics_A7] | [![][U_Chords_Am7]][U_Pics_Am7] |

| B | Bm | B7 | Bmaj7 |
|:---:|:---:|:---:|:---:|
| [![][U_Chords_B]][U_Pics_B] | [![][U_Chords_Bm]][U_Pics_Bm] | [![][U_Chords_B7]][U_Pics_B7] | [![][U_Chords_Bmaj7]][U_Pics_Bmaj7] |

| G | Gm | G7 | Gm7 |
|:---:|:---:|:---:|:---:|
| [![][U_Chords_G]][U_Pics_G] | [![][U_Chords_Gm]][U_Pics_Gm] | [![][U_Chords_G7]][U_Pics_G7] | [![][U_Chords_Gm7]][U_Pics_Gm7] |

<div style="break-after:page"></div>

# 指板系統

## CAGED 指型

| 根音在第六弦 `G E` | 根音在第五弦 `C A` | 根音在第四弦 `F D` |
| :----------------: | :----------------: | :----------------: |
| ![][G_Chords_G]    | ![][G_Chords_C]    | ![][G_Chords_F]    |
| ![][G_Chords_E]    | ![][G_Chords_A]    | ![][G_Chords_D]    |

> F 和弦指型就是 E 和弦指型平移一格  
> B 和弦指型就是 A 和弦指型平移兩格

## CAGED - 以 C 大調為例

> 用封閉和弦，找到對應的根音，就可以在全把位按出想要的和弦

<div style="break-after:page"></div>

| 指型  | C 和弦          | C 大調音階   | C 大調五聲音階      |
|:-----:| :-------------: | :----------: | :-----------------: |
| **C** | ![][Chords_C_C] | ![][CAGED_C] | ![][pentatonic_C_C] |
| **A** | ![][Chords_C_A] | ![][CAGED_A] | ![][pentatonic_C_A] |
| **G** | ![][Chords_C_G] | ![][CAGED_G] | ![][pentatonic_C_G] |
| **E** | ![][Chords_C_E] | ![][CAGED_E] | ![][pentatonic_C_E] |
| **D** | ![][Chords_C_D] | ![][CAGED_D] | ![][pentatonic_C_D] |

### 五聲音階

| 音階               | 組成音程 (度數) |   |   |   |   |   |
| :----------------: | :-------------: |:-:|:-:|:-:|:-:|:-:|
| A minor Pentatonic | 1 b3 4 5 b7     | A | C | D | E | G |
| C Major Pentatonic | 1 2 3 5 6       | C | D | E | G | A |

> C 大調和 A 小調使用完全相同的音，只是主音不同，這種關係稱為關係大小調

<div style="break-after:page"></div>

## 快速找到根音的練習

| 0 - 3          | 2 - 5          | 3 - 7          |
| :------------: | :------------: | :------------: |
| ![][CAGED_EFG] | ![][CAGED_GA]  | ![][CAGED_GAB] |

| 5 - 8          | 7 - 10         | 10 - 12        |
| :------------: | :------------: | :------------: |
| ![][CAGED_ABC] | ![][CAGED_BCD] | ![][CAGED_CDE] |

> 熟悉指板上音級之間的相對位置，就可以在快速定位根音及音階  
> 移調就是把一樣的形狀套用在不同的根音上

<div style="break-after:page"></div>

## 和弦在指板上的位置

| C                    | Cm                    | Cdim                    |
| :------------------: | :-------------------: | :---------------------: |
| ![][chord_on_fret_C] | ![][chord_on_fret_Cm] | ![][chord_on_fret_Cdim] |

| Csus2                    | Csus4                    | Caug                    |
| :----------------------: | :----------------------: | :---------------------: |
| ![][chord_on_fret_Csus2] | ![][chord_on_fret_Csus4] | ![][chord_on_fret_Caug] |



[G_C_Major]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/C_Major.svg
[G_Chords_C]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/C.svg
[G_Chords_C7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/C7.svg
[G_Chords_Cmaj7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Cmaj7.svg
[G_Chords_Cadd9]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Cadd9.svg
[G_Chords_A]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/A.svg
[G_Chords_Am]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Am.svg
[G_Chords_A7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/A7.svg
[G_Chords_Am7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Am7.svg
[G_Chords_B]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/B.svg
[G_Chords_Bm]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Bm.svg
[G_Chords_B7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/B7.svg
[G_Chords_Bm7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Bm7.svg
[G_Chords_G]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/G.svg
[G_Chords_G7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/G7.svg
[G_Chords_Gmaj7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Gmaj7.svg
[G_Chords_Gsus4]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Gsus4.svg
[G_Chords_E]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/E.svg
[G_Chords_Em]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Em.svg
[G_Chords_E7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/E7.svg
[G_Chords_Em7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Em7.svg
[G_Chords_F]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/F.svg
[G_Chords_Fm]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Fm.svg
[G_Chords_F7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/F7.svg
[G_Chords_Fmaj7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Fmaj7.svg
[G_Chords_D]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/D.svg
[G_Chords_Dm]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Dm.svg
[G_Chords_D7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/D7.svg
[G_Chords_Dm7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chords/Dm7.svg
[G_Pics_C]: https://chord-c.com/img/share/chords/pics/c/C_1.jpg
[G_Pics_C7]: https://chord-c.com/img/share/chords/pics/c/C7_1.jpg
[G_Pics_Cmaj7]: https://chord-c.com/img/share/chords/pics/c/Cmaj7_1.jpg
[G_Pics_Cadd9]: https://chord-c.com/img/share/chords/pics/c/Cadd9_1.jpg
[G_Pics_A]: https://chord-c.com/img/share/chords/pics/a/A_1.jpg
[G_Pics_Am]: https://chord-c.com/img/share/chords/pics/a/Am_1.jpg
[G_Pics_A7]: https://chord-c.com/img/share/chords/pics/a/A7_1.jpg
[G_Pics_Am7]: https://chord-c.com/img/share/chords/pics/a/Am7_1.jpg
[G_Pics_B]: https://chord-c.com/img/share/chords/pics/b/B_1.jpg
[G_Pics_Bm]: https://chord-c.com/img/share/chords/pics/b/Bm_1.jpg
[G_Pics_B7]: https://chord-c.com/img/share/chords/pics/b/B7_1.jpg
[G_Pics_Bm7]: https://chord-c.com/img/share/chords/pics/b/Bm7_1.jpg
[G_Pics_G]: https://chord-c.com/img/share/chords/pics/g/G_1.jpg
[G_Pics_G7]: https://chord-c.com/img/share/chords/pics/g/G7_1.jpg
[G_Pics_Gmaj7]: https://chord-c.com/img/share/chords/pics/g/Gmaj7_1.jpg
[G_Pics_Gsus4]: https://chord-c.com/img/share/chords/pics/g/Gsus4_1.jpg
[G_Pics_E]: https://chord-c.com/img/share/chords/pics/e/E_1.jpg
[G_Pics_Em]: https://chord-c.com/img/share/chords/pics/e/Em_1.jpg
[G_Pics_E7]: https://chord-c.com/img/share/chords/pics/e/E7_1.jpg
[G_Pics_Em7]: https://chord-c.com/img/share/chords/pics/e/Em7_1.jpg
[G_Pics_F]: https://chord-c.com/img/share/chords/pics/f/F_1.jpg
[G_Pics_Fm]: https://chord-c.com/img/share/chords/pics/f/Fm_1.jpg
[G_Pics_F7]: https://chord-c.com/img/share/chords/pics/f/F7_1.jpg
[G_Pics_Fmaj7]: https://chord-c.com/img/share/chords/pics/f/Fmaj7_1.jpg
[G_Pics_D]: https://chord-c.com/img/share/chords/pics/d/D_1.jpg
[G_Pics_Dm]: https://chord-c.com/img/share/chords/pics/d/Dm_1.jpg
[G_Pics_D7]: https://chord-c.com/img/share/chords/pics/d/D7_1.jpg
[G_Pics_Dm7]: https://chord-c.com/img/share/chords/pics/d/Dm7_1.jpg
[U_C_Major]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/C_Major.svg
[U_Chords_C]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/C.svg
[U_Chords_C7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/C7.svg
[U_Chords_Cmaj7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Cmaj7.svg
[U_Chords_Csus4]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Csus4.svg
[U_Chords_A]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/A.svg
[U_Chords_Am]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Am.svg
[U_Chords_A7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/A7.svg
[U_Chords_Am7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Am7.svg
[U_Chords_B]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/B.svg
[U_Chords_Bm]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Bm.svg
[U_Chords_B7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/B7.svg
[U_Chords_Bmaj7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Bmaj7.svg
[U_Chords_G]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/G.svg
[U_Chords_Gm]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Gm.svg
[U_Chords_G7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/G7.svg
[U_Chords_Gm7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Gm7.svg
[U_Chords_F]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/F.svg
[U_Chords_F7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/F7.svg
[U_Chords_Fmaj7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Fmaj7.svg
[U_Chords_Fadd9]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Fadd9.svg
[U_Chords_D]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/D.svg
[U_Chords_Dm]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Dm.svg
[U_Chords_D7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/D7.svg
[U_Chords_Dm7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Dm7.svg
[U_Chords_E]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/E.svg
[U_Chords_Em]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Em.svg
[U_Chords_E7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/E7.svg
[U_Chords_Em7]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/ukulele/chords/Em7.svg
[U_Pics_C]: https://ukulele-chords.com/img/chord/photo/Cmajor_132.jpg
[U_Pics_C7]: https://ukulele-chords.com/img/chord/photo/C7_140.jpg
[U_Pics_Cmaj7]: https://ukulele-chords.com/img/chord/photo/Cmaj7_150.jpg
[U_Pics_Csus4]: https://ukulele-chords.com/img/chord/photo/Csus4_157.jpg
[U_Pics_A]: https://ukulele-chords.com/img/chord/photo/Amajor_1.jpg
[U_Pics_Am]: https://ukulele-chords.com/img/chord/photo/Aminor_6.jpg
[U_Pics_A7]: https://ukulele-chords.com/img/chord/photo/A7_11.jpg
[U_Pics_Am7]: https://ukulele-chords.com/img/chord/photo/Am7_15.jpg
[U_Pics_B]: https://ukulele-chords.com/img/chord/photo/Bmajor_85.jpg
[U_Pics_Bm]: https://ukulele-chords.com/img/chord/photo/Bminor_88.jpg
[U_Pics_B7]: https://ukulele-chords.com/img/chord/photo/B7_93.jpg
[U_Pics_Bmaj7]: https://ukulele-chords.com/img/chord/photo/Bmaj7_100.jpg
[U_Pics_G]: https://ukulele-chords.com/img/chord/photo/Gmajor_504.jpg
[U_Pics_Gm]: https://ukulele-chords.com/img/chord/photo/Gminor_509.jpg
[U_Pics_G7]: https://ukulele-chords.com/img/chord/photo/G7_513.jpg
[U_Pics_Gm7]: https://ukulele-chords.com/img/chord/photo/Gm7_518.jpg
[U_Pics_F]: https://ukulele-chords.com/img/chord/photo/Fmajor_405.jpg
[U_Pics_F7]: https://ukulele-chords.com/img/chord/photo/F7_414.jpg
[U_Pics_Fmaj7]: https://ukulele-chords.com/img/chord/photo/Fmaj7_422.jpg
[U_Pics_Fadd9]: https://ukulele-chords.com/img/chord/photo/Fadd9_444.jpg
[U_Pics_D]: https://ukulele-chords.com/img/chord/photo/Dmajor_244.jpg
[U_Pics_Dm]: https://ukulele-chords.com/img/chord/photo/Dminor_249.jpg
[U_Pics_D7]: https://ukulele-chords.com/img/chord/photo/D7_255.jpg
[U_Pics_Dm7]: https://ukulele-chords.com/img/chord/photo/Dm7_260.jpg
[U_Pics_E]: https://ukulele-chords.com/img/chord/photo/Emajor_353.jpg
[U_Pics_Em]: https://ukulele-chords.com/img/chord/photo/Eminor_357.jpg
[U_Pics_E7]: https://ukulele-chords.com/img/chord/photo/E7_361.jpg
[U_Pics_Em7]: https://ukulele-chords.com/img/chord/photo/Em7_365.jpg
[Chords_C_C]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/Chords/C_C.svg
[Chords_C_A]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/Chords/C_A.svg
[Chords_C_G]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/Chords/C_G.svg
[Chords_C_E]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/Chords/C_E.svg
[Chords_C_D]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/Chords/C_D.svg
[CAGED_C]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/C.svg
[CAGED_A]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/A.svg
[CAGED_G]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/G.svg
[CAGED_E]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/E.svg
[CAGED_D]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/D.svg
[pentatonic_C_C]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/pentatonic/C_C.svg
[pentatonic_C_A]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/pentatonic/C_A.svg
[pentatonic_C_G]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/pentatonic/C_G.svg
[pentatonic_C_E]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/pentatonic/C_E.svg
[pentatonic_C_D]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/pentatonic/C_D.svg
[CAGED_EFG]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/EFG.svg
[CAGED_GA]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/GA.svg
[CAGED_GAB]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/GAB.svg
[CAGED_ABC]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/ABC.svg
[CAGED_BCD]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/BCD.svg
[CAGED_CDE]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/CAGED/CDE.svg
[chord_on_fret_C]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chord_on_fret/C.svg
[chord_on_fret_Cm]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chord_on_fret/Cm.svg
[chord_on_fret_Cdim]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chord_on_fret/Cdim.svg
[chord_on_fret_Csus2]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chord_on_fret/Csus2.svg
[chord_on_fret_Csus4]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chord_on_fret/Csus4.svg
[chord_on_fret_Caug]: {{ site.url }}{{ site.baseurl }}/assets/images/2026-09-01-guitar-learning-notes/guitar/chord_on_fret/Caug.svg
