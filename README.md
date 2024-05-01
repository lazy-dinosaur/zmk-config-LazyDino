# personal zmk-config

- corne 42키 기반
- cirque trackpad 추가
- urob 유저의 zmk-nodefree 적용
- urob 유저의 개인 설정 기반으로 수정하는중

```bash
# left build
 west build -d build/left -b nice_nano_v2 -- -DSHIELD=wowcorne_left -DZMK_CONFIG="/home/hyeongseokwoo/keyboard/zmk/zmk-config-corne-cirque/config" -DZMK_EXTRA_MODULES="/home/hyeongseokwoo/
keyboard/zmk/zmk-config-corne-cirque;/home/hyeongseokwoo/keyboard/zmk/zmk-config-corne-cirque/cirque-input-module;"
# right build
 west build -d build/right -b nice_nano_v2 -- -DSHIELD=wowcorne_right -DZMK_CONFIG="/home/hyeongseokwoo/keyboard/zmk/zmk-config-corne-cirque/config" -DZMK_EXTRA_MODULES="/home/hyeongseokwoo/
keyboard/zmk/zmk-config-corne-cirque;/home/hyeongseokwoo/keyboard/zmk/zmk-config-corne-cirque/cirque-input-module;"
```
