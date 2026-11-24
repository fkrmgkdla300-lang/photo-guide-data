# photo-guide-data

사진 가이드 카메라 앱이 "업데이트 확인" 때 받아가는 촬영 팁 파일.

- `reference.json` 하나만 쓴다.
- 고칠 때마다 `version` 숫자를 1 올려야 앱이 새 버전으로 인식한다.
- `scenes`: 상황별 기본 규칙 (노출 보정, 셔터 제한, 가이드 종류, 안내 문구)
- `tips`: 크리에이터·기본 규칙 팁 (`scene`, `text`, `source`, `added`)

## refs/ — 감성샷 참고 사진

- `refs/refs.json`: 참고 사진 목록. 앱의 '✨ 감성 구도'와 AI 평가가 이 사진들과 비교한다.
  - `id`(Pexels 사진 번호), `scene`(xmas / cafe / food / night_portrait / backlight_portrait / sunset_silhouette / pet / 새 장면),
    `keywords`(ML Kit 라벨과 맞출 영어 단어), `tag`(짧은 구도 이름), `desc`(구도 설명), `img`, `source`, `credit`
- `refs/img/<id>.jpg`: 긴 변 500px 이하.
- 매주 목요일 밤 자동 수집 작업이 새 사진을 추가하고 `version`을 1 올린다. 같은 `id`는 다시 넣지 않는다.
- 사진 출처: Pexels (무료 사용 허용 라이선스).
