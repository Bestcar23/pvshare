# 잠언과 함께한 한 주간

손끝으로 책장을 넘기며 읽는 잠언 묵상 웹앱입니다. 가죽 성경 표지 + 7/13(월)~7/18(토) 6일치 묵상 카드, 책장 넘김 애니메이션과 "사그락" 효과음, 잔잔한 재즈 배경음악, 넘길 때마다 흩날리는 꽃잎 효과를 담았습니다.

## 구성

빌드 과정이 없는 순수 정적 사이트입니다. 파일은 셋뿐입니다.

| 파일 | 역할 |
|---|---|
| `index.html` | 웹앱 전체 (HTML · CSS · JS 한 파일) |
| `vercel.json` | Vercel 설정 (캐시 · 보안 헤더) |
| `.gitignore` | Git 제외 목록 |

## GitHub에 올리기

이미 로컬에 이 폴더가 있다면:

```bash
git init
git add .
git commit -m "잠언 묵상 웹앱"
git branch -M main
git remote add origin https://github.com/<사용자명>/<저장소명>.git
git push -u origin main
```

> GitHub 웹사이트에서 **New repository** 로 빈 저장소를 먼저 만든 뒤 위 주소를 넣으세요.
> 터미널이 없다면, GitHub 저장소 페이지의 **Add file → Upload files** 로 세 파일을 끌어다 놓아도 됩니다.

## Vercel로 배포하기

1. [vercel.com](https://vercel.com) 접속 → GitHub 계정으로 로그인
2. **Add New… → Project**
3. 방금 올린 GitHub 저장소를 **Import**
4. 설정은 그대로 두면 됩니다 (빌드 명령·출력 폴더 불필요)
   - Framework Preset: **Other**
   - Build Command: 비움
   - Output Directory: 비움
5. **Deploy** → 잠시 후 `https://<프로젝트명>.vercel.app` 주소가 나옵니다

이후 GitHub에 `git push` 할 때마다 Vercel이 자동으로 새 버전을 배포합니다.

## 사용법

- **넘기기**: 화면을 좌우로 밀거나, 좌/우 절반을 탭하거나, 하단 화살표·키보드 ← → 사용
- **소리**: 우측 상단 **Sound Off / On** 버튼으로 배경음악과 효과음을 켜고 끕니다 (브라우저 정책상 첫 터치 후 재생)

## 참고 — 배경음악

배경음악은 외부 음원(Flow Music 저장소)을 링크로 사용합니다. 링크가 끊기면 버튼에 "BGM 없음"으로 표시되고 효과음은 계속 작동합니다. 더 안정적으로 운영하려면 음원 파일(`.m4a`)을 이 저장소에 넣고 `index.html` 의 `<source src="...">` 를 `src="/bgm.m4a"` 같은 상대경로로 바꾸세요.
