# photo-guide-data

사진 가이드 카메라 앱이 "업데이트 확인" 때 받아가는 촬영 팁 파일.

- `reference.json` 하나만 쓴다.
- 고칠 때마다 `version` 숫자를 1 올려야 앱이 새 버전으로 인식한다.
- `scenes`: 상황별 기본 규칙 (노출 보정, 셔터 제한, 가이드 종류, 안내 문구)
- `tips`: 크리에이터·기본 규칙 팁 (`scene`, `text`, `source`, `added`)
