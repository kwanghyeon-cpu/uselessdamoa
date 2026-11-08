# 음원 출처

앱에 들어간 녹음 파일과 그 출처·라이선스 기록. 광고가 있는 앱이라 상업적 사용이 허용된 음원만 쓴다(CC0, Pixabay 콘텐츠 라이선스 등). 비상업(NC) 라이선스와 Sampling+는 쓰지 않는다.

Pixabay의 `freesound_community` 계정 음원은 Freesound에서 옮겨 온 것이다. Pixabay 페이지는 모두 Pixabay Content License로 표시하지만, **원본의 Freesound 라이선스가 더 엄격할 수 있으니 원본도 확인한다.**

원본은 `sounds/`, 앱에 들어가는 사본은 `app/src/main/res/raw/`.

| 앱 파일 | 받은 곳 | Freesound 원본 | 원본 라이선스 | 판단 |
|---|---|---|---|---|
| `sigh_any_2.mp3` | [sigh](https://pixabay.com/sound-effects/people-sigh-100452/) (Pixabay, 2022-09-01) | [Kiyoshiakira – sigh.wav](https://freesound.org/people/Kiyoshiakira/sounds/436775/) (2.1초, 같은 녹음으로 추정) | CC0 | 사용 가능 |
| `sigh_any_3.mp3` | [woman sigh](https://pixabay.com/sound-effects/people-woman-sigh-101931/) (Pixabay, 2022-09-02) | [threadzz – woman sigh](https://freesound.org/people/threadzz/sounds/384992/) | CC0 | 사용 가능 |
| `sigh_any_4.mp3` | [male sigh](https://pixabay.com/sound-effects/people-male-sigh-6763/) (Pixabay, 2021-08-10) | [Reitanna – male sigh.wav](https://freesound.org/people/Reitanna/sounds/215380/) | CC0 | 사용 가능 |

모두 2026-11-06에 받음. CC0와 Pixabay Content License는 출처 표시 의무가 없다.

### 뺀 음원
- `sigh_any_1.mp3` — [Pixabay "sigh"](https://pixabay.com/sound-effects/people-sigh-103855/), 원본은 [the_justin – sigh.wav](https://freesound.org/people/the_justin/sounds/9891/). 원본 라이선스가 **Sampling+ 1.0**(원본 그대로 배포는 비상업만, 출처 표시 필수, 광고·홍보 용도 금지)이라 광고가 있는 이 앱에 맞지 않아 2026-11-06에 앱에서 뺐다. 원본 파일은 `sounds/excluded/`에 보관만 한다 — 다시 넣지 말 것.

## 앱에서 쓰는 방식
`SighScreen.kt`의 `SighSamples`가 12종 한숨마다 `res/raw`의 `sigh_any_*` 중 하나를 골라 0.7~1.4배 속도로 재생한다. 종류 전용 녹음(`sigh_<id>.mp3`, id는 `SIGHS` 참고)을 넣으면 그 종류는 전용 녹음을 그대로 쓴다.
