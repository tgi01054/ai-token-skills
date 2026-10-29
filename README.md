# AI Token Skills

토큰 사용량을 줄이고 컨텍스트를 효율적으로 관리하는 도구와 스킬을 Git submodule로 관리하는 저장소입니다.

## 포함된 저장소

| 이름 | 경로 | 원본 저장소 |
| --- | --- | --- |
| Ponytail | `vendor/ponytail` | [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) |
| Caveman | `vendor/caveman` | [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman) |
| RTK | `vendor/rtk` | [rtk-ai/rtk](https://github.com/rtk-ai/rtk) |
| Headroom | `vendor/headroom` | [headroomlabs-ai/headroom](https://github.com/headroomlabs-ai/headroom) |
| Context Mode | `vendor/context-mode` | [mksglu/context-mode](https://github.com/mksglu/context-mode) |
| Serena | `vendor/serena` | [oraios/serena](https://github.com/oraios/serena) |
| Token Optimizer | `vendor/token-optimizer` | [alexgreensh/token-optimizer](https://github.com/alexgreensh/token-optimizer) |

## 레이아웃

외부 저장소는 `ai-agent-skills` 저장소와 같은 방식으로 `vendor/<저장소명>` 아래에 배치합니다.

```text
vendor/
  ponytail/
  caveman/
  rtk/
  headroom/
  context-mode/
  serena/
  token-optimizer/
```

## Clone 및 초기화

```bash
git clone --recurse-submodules <repository-url>
```

이미 clone한 저장소에서 submodule을 초기화하거나, 네트워크 오류로 중단된 초기화를 재시도하려면 다음 명령어를 실행합니다.

```bash
git submodule update --init --recursive
```
