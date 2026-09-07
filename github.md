repo: skim2048/mewly
branch: master

design-repo: skim2048/mewly-design
design-branch: master

reference-repo: skim2048/babycat
reference-branch: master

## Last sync

date: 2026-09-07T07:05:00Z

### Updated in this project

- 파일 이름을 영어 소문자 케밥 케이스 `nn-screen-name.dc.html`로 전환(사용자 지시). 「Mewly」「V3」 접두어 제거 — 리포지토리 이름이 mewly-design이고 남은 시트가 전부 v3라 구분 대상이 없다. 01 Component_Catalog · 02 Login · 03 Home_Tab · 04 Schedule_Tab · 05 Analysis_Tab · 06 Settings_Profile · 07 Settings_Camera · 08 Settings_Sheets · 09 Notifications_Overlay · structure-map · handoff-summary.md
- 시트 10개의 코드 주석(JS `//`, CSS `/* */`) 146줄을 전부 영어로 전환(CLAUDE.md 「코딩」 규칙). 화면 안 텍스트 레이블·카탈로그 사양 문장·기록 문서는 한국어 유지(사용자 확정 1안). structure-map 안의 `/* 타입 스케일 */` `/* 최종 승자 */`는 원본 global.css를 인용해 보여 주는 화면 내용이라 그대로 둠
- 08 안의 링크를 `02-login.dc.html`로 갱신

### 2026-09-07T06:28:00Z

- 이 디자인 프로젝트의 저장소 「skim2048/mewly-design」(master) 등록 — 사용자가 리포지터리를 만들고 프로젝트 zip으로 초기 커밋. 커밋·푸시는 사용자가 로컬에서 한다. 리포지토리에는 `.gitignore`·`README.md`가 더 있고 `uploads/`는 제외된다. `CLAUDE.md`·`skills/`는 로컬 `.claude/` 아래에 두어 `.gitignore`로 제외한다 — 지침과 스킬은 저장소에 올리지 않는다(사용자 의도)
- 설정 축 파일 이름 확정(사용자 승인, 안 A) — 「V3-8 카메라 설정」→「V3-7 Mewly 설정·카메라」, 「V3-9 설정 시트」→「V3-8 Mewly 설정·시트」, 「V3-7 알림 오버레이」→「V3-9」. 근거: MainView.vue에서 카메라·프롬프트·분석·비밀번호 모달과 알림 설정은 SettingsTab에서 열리고, 알림함은 상단 바 종 버튼에서 열린다(설정 축 밖). 파일 내용은 시트 머리 라벨만 바꿈
- V3-8 설정·시트 안의 깨진 링크 「V3-2 Mewly 로그인·전체화면」→「V3-2 Mewly 로그인」 수정
- 카탈로그 대조(빈 상태 한 줄 등급 = 0.8125rem · 줄 간격 1.6): V3-3 회전 전체화면 「로그가 없습니다.」 0.75→0.8125, V3-5 「이 날은 감지된 이벤트가 없습니다」 0.875→0.8125, V3-5 「이 날의 추론 데이터가 없습니다」를 0.75 배지 자리에서 분리해 0.8125 한 줄로. 카메라 꺼짐·VLM 카드·알림함 빈 상태·「일정」 각주는 카탈로그와 일치

### 2026-09-07T04:20:00Z

- B 그룹 확정 반영 — V3-3: 카메라 꺼짐 상태(HomeTab.vue 604행, Tweaks `camera` on/off/none) · 로그 없음 상태(787·693행, Tweaks `noLogs`). V3-5: 이벤트 없음(AnalysisTab.vue 513행, `noEvents`) · 추론 데이터 없음(427행, `noData`) · 클립 플레이어 정보 영역 「탭하여 닫기」(ClipPlayerModal.vue 226행). V3-7: 「일정」 행 각주를 원본 `.switch-foot`처럼 항상 표시로 바꾸고 꺼진 뒤에만 나오던 상자 제거
- 유지 확정(원본과 다르게 둠): V3-4 일정 편집기 카테고리 칩 없음(이름 칸만), V3-6 견종 드롭다운(검색 모드 없음)
- 카탈로그 04에 「뱈 상태의 두 등급」과 「행의 각주 줄」 확정 문장 추가

### 2026-09-07T03:52:09Z

- 카탈로그 첫머리에 「용어」 표 신설 — 원본 i18n과 다르게 확정한 낱말을 모은다. 현재 둘: `sched.done` 마침→완료, `ana.acto.sub` 문구의 비누움→닭지 않음(V3-5 라이트·다크 반영)
- V3-6 설정 행 「서버」→「서버 주소」(`set.rowServer`, SettingsTab.vue 40행)
- B 그룹 8항목(원본에 있고 v3 화면에 없는 상태·부품)을 HomeTab·ScheduleEditor·AnalysisTab·ClipPlayerModal·ProfileOverlay·NotifSettingsOverlay.vue에서 표시 조건까지 확인. 사용자 확정 대기

### 2026-09-07T09:20:00Z

- 「V3-3 Mewly 홈 탭」의 기기 줄(조명·온도·마이크·PTZ)에서 열리던 임시 오버레이(제목·설명 한 줄·토글 하나·적용) 제거 — 원본에 없는 설명문 4줄도 함께 사라짐
- 「V3-8 Mewly 기기 제어 시트」의 조명·온도·마이크 시트(라이트·다크 6화면)와 그 로직(스위치·칩·세그먼트·휠·예약)을 「V3-3 Mewly 홈 탭」 안으로 옮기고 V3-8 파일 삭제
- 빈 번호를 메워 「V3-9 카메라 설정」→「V3-8」, 「V3-10 설정 시트」→「V3-9」로 개명. 파일 내용은 그대로
- 모바일 설계 규칙 스킬(iOS HIG · Material 3 · 대비)을 `skills/mobile-design-rules/`에 배치
- V3-2의 「03 회전 전체화면」·「04 PTZ 시트」를 V3-3 홈 탭으로 이동(HomeTab.vue의 소속을 따른다). V3-2는 로그인·밀밀번호 변경·세션 만료만 남기고 「V3-2 Mewly 로그인」으로 개명
- V3-3 기기 줄 네 버튼(조명·온도·마이크·PTZ)이 홈 프레임 안에서 실제 시트를 열도록 연결 — 원본 `emit('open-sheet', key)`와 같다. 독립 시트 프레임 6개는 오버레이로 대체해 제거
- 카탈로그 04에 「완료」 용어와 끝냄 켜고 꺼기 조작(사양 변경) 문장 추가

### 2026-09-04T08:12:00Z

- 이전 세션의 「V3-8 Mewly 기기 제어 시트」 파일이 프로젝트에 없어(카탈로그 사양 문장만 남아 있었다) LightSheet.vue · TempSheet.vue · MicSheet.vue · useDevices.js · i18n(dev.* light.* temp.* mic.* common.*)를 다시 판독해 재작성했다 — 조명·온도·마이크, 라이트·다크
- 카탈로그 확정 사양 적용: 프리셋 4슬롯은 PTZ 위치에만 두어 조명·온도에서 제외, 온도에 냉난방 예약(한 구간) 추가, 원본의 글로우 오브·상태 칩·시스템 select·마이크 파형은 큰 수치·상태 텍스트·스위치·세그먼트·96 누름 버튼으로 대치
- PtzSheet.vue · usePtz.js · CameraPanel.vue · useCamera.js · config/ptz.json 판독 — V3-9 범위 판단(PTZ는 V3-2에 이미 있어 V3-9는 카메라 등록만 담기로 결정)
- 구 버전 재현 3개(기기 시트 · 클립·카메라 · PTZ·설정 시트) 삭제 — V3-8 · V3-9·V3-5 · V3-2로 대체됨. 「Mewly 구조 지도」는 v3 대응 시트가 없어 유지
- CameraPanel.vue · useCamera.js · i18n(camera.* toast.cam*) 판독 → 「V3-9 Mewly 카메라 설정」 신설(라이트·다크). 여섯 칸 모두 02 입력 필드, 저장은 카메라가 꺼진 동안에만, 저장 후 이어서 켜기, 완료는 토스트·실패는 인라인 주의, 저장된 비밀번호는 초점을 두면 비워진다

### 2026-09-04T04:50:00Z

- LightSheet.vue · TempSheet.vue · MicSheet.vue · SheetFrame.vue · useDevices.js · i18n(dev.* light.* temp.* mic.*) 판독 → 「V3-8 Mewly 기기 제어 시트」 신설(조명·온도·마이크, 라이트·다크)
- 카탈로그 02에 슬라이더(트랙 8 · 손잡이 22 · 눈금 1×5) · 큰 수치(1.25rem) · 상태 텍스트 · 전원/모드(스위치·세그먼트) · 프리셋 4슬롯 · 누르고 있는 동안 동작하는 버튼(96) 사양 문장 추가
- 원본의 글로우 오브·상태 칩·시스템 select·마이크 파형은 카탈로그 부품으로 대치
- 사용자 승인으로 조명·온도 프리셋 4슬롯 제거, 온도에 냉난방 예약(한 구간 · 나이트 모드와 같은 구조) 추가 — 원본 mewly에 없는 기능(사양 변경). 카탈로그에 「프리셋은 PTZ 위치에만」·「예약 구조」 문장 추가
- 구 버전 재현 3개(분석 설정 · 설정 탭 · 알림 오버레이) 삭제 — v3 시트로 대체됨

## Sync history

### 2026-09-03T08:10:59Z

- AnalysisPanel.vue · PromptSheet.vue · ChangePasswordPanel.vue · ProfileOverlay.vue(크롭 모드) · analysisConfig.js · config/analysis.json · config/ui.json 판독 → 「V3-10 Mewly 설정 시트」 신설(분석 설정·프롬프트 설정·밀밀번호 밀경·사진 조정, 라이트·다크)
- 주간 구간을 시스템 드롭다운에서 05-G 폼 행 + 한 열 휠(160)로 재해석, 상태 어휘 보기 바랍은 읽기 전용 묶으로 유지
- 프롬프트 보호 장지 재현 — 검증 및안 이탈 상시 경고·복원, 질의 변경 시 2단계 확인, X는 마지막 저장 상틜로 되돌림
- 사진 조정은 원본 수치(무대 300 · 출력 512 · 배율 최소~3배)로 실제 끌기·확대 구현, 자리표시자 이밀지 public/crop-placeholder.png 추가
- 카타로그 04항에 「밀어서 동작」 사양 기재(두 방향 · 버튼 72 · 덮는 증 · 절반 넘김 스랩 0.22s · 색 위계 · 확인 없는 지우기), V3-4 일정 행에 스와이프 동작 구현
- 일정 목록을 04 묶음 리스트로 전환하고 끝난 항목을 아랫 묶음으로 분리(소제목 없음)

## Sync history

### 2026-09-03T06:56:45Z

### Updated in this project

- useSchedules.js + ScheduleEditor.vue 재확인 — 원본 편집기엔 날짜 선택기가 없고(`endDate: undefined` 고정), 날짜는 고른 하루로 고정된 읽기 전용 라벨이다. V3-4에서 시작일·종료일 칩·편집기 달력·연·월 휠·날짜 역전 검증을 제거하고 읽기 전용 날짜 한 줄로 대치
- 반복(repeat)은 알람 예약 메타데이터로 달력 회차를 만들지 않는다는 원본 주석을 카탈로그에 사양 문장으로 명문화
- V3-4 연·월 시트를 인라인 펼침으로 변경(오버레이 제거), V3-5 날짜 줄·세그먼트를 스크롤 영역 안으로 이동
- 휠 연도 범위 사양 통일 — 기본 전제 올해 ±50년, 미래를 고를 수 없는 용도(분석·생년월)는 상한을 오늘로 — 카탈로그·V3-4·V3-5·V3-6 적용

## Sync history

### 2026-09-03T04:49:22Z · b7bfca2ec415

- AnalysisTab.vue 재확인(395~399행 date-btn·date-label) → 「V3-5 Mewly 분석 탭」에서 원본에 없는 근거 문장 시트와 날짜 이동 시트를 제거하고, 상단을 일정 탭 어법(연·월 라벨 → 연·월 두 열 휠 시트, 월 이동 버튼, 요일 줄, 42셀 달력)으로 교체
- 목록 행 높이 규격 통일 — 카탈로그에 「행 56은 구분선과 세로 패딩을 포함한 값 · 세로 패딩은 (56 − 보더 − 내용 최고 높이) ÷ 2 이하 · 한 행 두 줄 간격 2」 명문화, V3-5·V3-6·V3-7 적용
- V3-7 클립 플레이어에 설명 문장 추가(V3-5와 같은 형식)

## Sync history

### 2026-09-03T00:39:37Z · b7bfca2ec415

- ClipPlayerModal.vue + useClips.js 재판독 → 「V3-5 Mewly 분석 탭」에 클립 플레이어(카드 모달 · 재생/일시정지/시크/닫기, 8초 모의 재생) 추가 — 이벤트 클립 행 탭으로 진입
- NotificationsOverlay/NotifSettingsOverlay → 「V3-7 Mewly 알림 오버레이」 신설 (세그먼트 전체·일정·이벤트, 날짜 묶음, 읽지 않음 점, 개별·전체 삭제, 알림 설정 스위치)

### 2026-09-02T07:31:38Z · b7bfca2ec415

- SettingsTab + ProfileOverlay 판독 → 「V3-6 Mewly 설정·프로필」 재현 (프로필 카드·두 묶음 리스트·언어 전환, 프로필 편집과 견종 검색 두 모드)
- CalendarTab + ScheduleEditor + useSchedules 재판독 → 「Mewly 일정 탭 신규」 재현 (v3 어법 · 라이트/다크, 42셀 달력·일정 점·다음 일정 강조, 편집기 검증 3단·종일 전환·시간 역전 오류)
- LoginView + ChangePasswordPanel + SessionExpiryModal + HomeTab(.video-wrap.fs) + PtzSheet 재판독 → 「Mewly 로그인·전체화면 신규」 재현 (v3 컴포넌트 어법 · 라이트/다크 대조, 연결 실패 흐름, 강제 비밀번호 변경 3종 검증, 세션 카운트다운, 회전 전체화면 캔버스·PTZ 패드, PTZ 시트 게이지·프리셋·자동 순찰 잠금)
- AnalysisPanel.vue 판독 → 「Mewly 분석 설정」 재현 (주간 구간 경계·상태 어휘, 경계 효과 도해) + 판독 메모 4건 — mewly 전 화면 재현 완료
- ClipPlayerModal + CameraPanel 판독 → 「Mewly 클립·카메라」 재현 (카드/회전 전체화면 플레이어, 카메라 프로필 저장·켜기 시퀀스) + 판독 메모 4건
- NotificationsOverlay/NotifSettingsOverlay 판독 → 「Mewly 알림 오버레이」 재현 (필터·날짜 구분·읽음/삭제, 권한 경고 분기) + 판독 메모 4건 (권한 UI 죽은 분기, 알림 생성 경로 부재)
- PtzSheet/PromptSheet/ResourcesSheet 판독 → 「Mewly PTZ·설정 시트」 재현 (D-Pad 노브·STOP 플래시, 순찰 잠금·적용 대기, 프롬프트 2단계 가드, 리소스 스파크라인) + 판독 메모 4건
- LightSheet/TempSheet/MicSheet + SheetFrame + controls.css 판독 → 「Mewly 기기 시트」 재현 (조도·온도 슬라이더, 오브 전원, 프리셋 저장 모드, 나이트 모드) + 판독 메모 4건
- LoginView.vue + ChangePasswordPanel.vue + SessionExpiryModal.vue 판독 → 「Mewly 로그인」 재현 (연결 시퀀스·강제 비밀번호 변경·세션 카운트다운) + 판독 메모 4건
- SettingsTab.vue + ProfileOverlay.vue + ServerPanel.vue 판독 → 「Mewly 설정 탭」 재현 (다크·라이트 팔레트 대조, 프로필 편집/견종 선택, 서버 주소 모달) + 판독 메모 4건
- CalendarTab.vue + ScheduleEditor.vue 판독 → 「Mewly 일정 탭」 재현 (달력 42셀·일정 점·다음 일정 강조, 편집기 검증/종일/삭제) + 판독 메모 4건
- AnalysisTab.vue 판독 → 「Mewly 분석 탭」 재현 (상태/이벤트 세그먼트, 히트맵 드릴다운, 페이지네이션) + 추론 원문 열람 시안
- HomeTab.vue 전문 판독 → 「Mewly 홈 탭」 재현 (연결 흐름·VLM 카드·요약 대시보드, Tweaks 상태 전환)
- 리포지토리 자산 복사: NanumSquare/Inter/Patrick Hand 폰트, Phosphor 아이콘 폰트+CSS, user_profile.svg
- 이전: 「Mewly 구조 지도」 문서 (화면 계층 · API 매핑 · 토큰 · 진단 5건)

## Screen map

| 프로젝트 화면 | mewly 소스 | babycat 소스 |
|---|---|---|
| 구조 지도 — 전체 | src/router.js, src/App.vue, src/views/MainView.vue, src/endpoints.js, docs/babycat-correspondence.md | README.md, router/main.py |
| 구조 지도 — 화면 계층 | src/views/MainView.vue, src/components/*.vue | — |
| 구조 지도 — API 매핑 | src/endpoints.js, src/composables/*.js | router/main.py |
| 구조 지도 — 디자인 토큰 | src/assets/global.css, src/assets/controls.css | — |
| 구조 지도 — 진단 | src/assets/global.css, src/endpoints.js, src/components/HomeTab.vue, src/components/AnalysisTab.vue | router/main.py |
| 분석 탭 재현 (Mewly 분석 탭.dc.html) | src/components/AnalysisTab.vue, src/composables/useInferenceSummary.js, src/composables/analysisConfig.js, config/analysis.json, src/i18n/messages.js | router/main.py (/summary, /events, /clips, /inferences) |
| 분석 설정 재현 (Mewly 분석 설정.dc.html) | src/components/AnalysisPanel.vue, src/composables/analysisConfig.js, config/analysis.json | router/main.py (/presets) |
| 분석 탭 + 클립 플레이어 (05-analysis-tab.dc.html) | src/components/AnalysisTab.vue, src/components/ClipPlayerModal.vue, src/composables/useClips.js, src/composables/analysisConfig.js | router/main.py (/summary, /events, /clips, /clips/{name}) |
| 알림함·알림 설정 (09-notifications-overlay.dc.html) | src/components/NotificationsOverlay.vue, src/components/NotifSettingsOverlay.vue, src/composables/useNotifications.js, src/composables/useNotifSettings.js | — (서버 미지원 목업) |
| 알림 오버레이 재현 (Mewly 알림 오버레이.dc.html) | src/components/NotificationsOverlay.vue, src/components/NotifSettingsOverlay.vue, src/composables/useNotifications.js, src/composables/useNotifSettings.js, src/composables/dates.js | — (서버 미지원 목업) |
| 홈 탭 + 기기 제어 시트(조명·온도·마이크·PTZ) + 회전 전체화면 (03-home-tab.dc.html) | src/components/HomeTab.vue, src/views/MainView.vue, src/composables/useVlmStatus.js, src/composables/useInferLog.js, src/components/LightSheet.vue, src/components/TempSheet.vue, src/components/MicSheet.vue, src/components/PtzSheet.vue, src/components/SheetFrame.vue, src/composables/useDevices.js, src/composables/usePtz.js, config/ptz.json, src/i18n/messages.js | router/main.py (/ptz/*) · 기기 제어는 서버 미지원 목업(localStorage device.*) |
| 설정·카메라 (07-settings-camera.dc.html) | src/components/CameraPanel.vue, src/composables/useCamera.js, src/i18n/messages.js | router/main.py (/camera, /streaming/start·stop) |
| 로그인·계정 재현 (Mewly 로그인.dc.html) | src/views/LoginView.vue, src/components/ChangePasswordPanel.vue, src/components/SessionExpiryModal.vue, src/composables/useAuth.js, src/i18n/messages.js | router/main.py (/login, /change-password, /refresh) |
| 설정 탭 재현 (Mewly 설정 탭.dc.html) | src/components/SettingsTab.vue, src/components/ProfileOverlay.vue, src/components/ServerPanel.vue, src/components/ModalFrame.vue, src/composables/useProfile.js, src/composables/useTheme.js, src/composables/useLocale.js, src/assets/global.css | router/main.py (/client-storage/pet_profile) |
| 일정 탭 재현 (Mewly 일정 탭.dc.html) | src/components/CalendarTab.vue, src/components/ScheduleEditor.vue, src/components/OverlayFrame.vue, src/components/ToggleSwitch.vue, src/composables/useSchedules.js, src/composables/dates.js | — (서버 미지원) |
| 로그인·밀밀번호 변경·세션 만료 (02-login.dc.html) | src/views/LoginView.vue, src/components/ChangePasswordPanel.vue, src/components/SessionExpiryModal.vue, src/i18n/messages.js | router/main.py (/login, /change-password, /refresh) |
| 설정·시트 — 분석·프롬프트·비밀번호·사진 조정 (08-settings-sheets.dc.html) | src/components/AnalysisPanel.vue, src/components/PromptSheet.vue, src/components/ChangePasswordPanel.vue, src/components/ProfileOverlay.vue, src/composables/analysisConfig.js, config/analysis.json, config/ui.json | router/main.py (/presets, /prompt, /change-password) |
| 일정 탭·편집기 재현 (04-schedule-tab.dc.html) | src/components/CalendarTab.vue, src/components/ScheduleEditor.vue, src/composables/useSchedules.js, src/composables/dates.js | — (서버 미지원, localStorage) |
| 설정·프로필 재현 (06-settings-profile.dc.html) | src/components/SettingsTab.vue, src/components/ProfileOverlay.vue, src/composables/useProfile.js | — (localStorage) |

## Notes

- 프론트엔드 = mewly (Vue 3 + Vite + Capacitor, Android). 백엔드 = babycat (FastAPI, Jetson, 4컨테이너).
- babycat은 참조 전용 — 변경 추적의 기준 리포지토리는 mewly.
- 의미 결정권(라벨 어휘·프리셋·기준선·리듬 카드 판정)은 전부 mewly에 있다. babycat은 부분 문자열 매치만 수행.
- 일정·알림·알림 설정·기기 제어(마이크/온도/조명)는 서버 미지원 — localStorage 목업(`mewly.` 접두어).
