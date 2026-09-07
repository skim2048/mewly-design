# mewly-design

스마트폰용 Mewly 앱의 화면을 새로 디자인하는 프로젝트다. Claude Design으로 만든 `.dc.html` 시트를 관리한다.

원본 앱은 `skim2048/mewly`(Vue 3 · Capacitor Android)이며, 재현 근거는 원본의 `.vue`, `config/*.json`, `src/i18n/messages.js`다.

## 파일

- `01_Component_Catalog.dc.html` — 모든 화면이 따르는 사양이다.
- `02_Login` · `03_Home_Tab` · `04_Schedule_Tab` · `05_Analysis_Tab` · `06_Settings_Profile` · `07_Settings_Camera` · `08_Settings_Sheets` · `09_Notifications_Overlay` — 화면 시트다. 각 시트는 라이트와 다크를 나란히 둔다.
- `Structure_Map.dc.html` — 원본 앱의 화면 계층·API·토큰 정리다.
- `Handoff_Summary.md`, `github.md` — 작업 진행 기록이다.

## 규칙

- 카탈로그가 사양이다. 화면과 다르면 화면을 카탈로그에 맞춘다.
- 카탈로그 수정은 사양 변경이므로 사용자 승인이 필요하다.
