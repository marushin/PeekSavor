# PeekSavor

**PeekSavor**는 이미지를 분석하여 Stable Diffusion, ComfyUI, Midjourney 및 AI 비디오 생성 도구(Sora, RunwayML, Pika 등)를 위한 프롬프트를 자동으로 생성해주는 Windows 데스크톱 애플리케이션입니다.


## 🚀 주요 기능

### 🎨 Image Studio (이미지 스튜디오)
- **이미지 분석 및 프롬프트 생성**: 이미지를 드래그 앤 드롭하여 시각적 요소를 분석하고 AI 이미지 생성용 텍스트 프롬프트로 변환합니다.
- **다양한 출력 스타일**: 키워드 기반, 자연어, 상세 설명, 한국어 출력 등 다양한 옵션 지원
- **OCR 기능**: 이미지 내 텍스트 추출 기능 내장

### 🎬 Video Director (비디오 디렉터)
- **비디오 프롬프트 생성**: 이미지 분석 결과와 장면 설명을 결합하여 AI 비디오 생성 도구용 프롬프트 작성
- **원활한 워크플로우**: Image Studio에서 생성된 프롬프트가 자동으로 연동

### 🛠️ 편의 기능
- **드래그 앤 드롭**: 파일 탐색기에서 이미지를 바로 끌어와서 열기
- **원클릭 복사**: 생성된 프롬프트를 클립보드로 즉시 복사
- **다중 LLM 지원**: Google Gemini, OpenAI, Claude, Qwen, LM Studio 등 다양한 AI 프로바이더 지원
- **자동 업데이트 알림**: 앱 시작 시 새 버전이 있으면 자동으로 알림

### 🧠 프롬프트 메모리 (Prompt Memory)
- **최근 프롬프트 기록**: 최근 생성된 10개의 프롬프트를 자동
- **슬라이딩 패널**: 타이틀바의 문서 아이콘을 클릭하여 기록을 확인하고 쉽게 복사하거나 재사용할 수 있음

### 📊 실시간 시스템 리소스 모니터링
- **리소스 대시보드**: CPU 사용량, 시스템 RAM, GPU 및 GPU RAM 사용량을 실시간으로 확인할 수 있는 기능이 추가되었습니다.
- **컴팩트 상태 표시**: 앱 우측 하단 상태바에서 RAM과 GPU RAM의 사용 상태를 요약해서 볼 수 있습니다.
- **상세 리소스 패널**: 상태바를 클릭하면 아래에서 위로 슬라이딩되는 패널을 통해 모든 리소스의 상세 상태를 확인할 수 있습니다.

### 🎨 UI 및 디자인 고도화
- **Suit 폰트 적용**: 앱 전체에 프리미엄 폰트인 'Suit'를 적용
- **상태 인디케이터**: 타이틀바의 상태 표시등 애니메이션 효과가 작업 상태를 더 직관적으로 인지할 수 있게 도와줌


## 🐛 버그 수정
- **프롬프트 동기화 오류 해결**: Image Studio에서 생성한 프롬프트가 Video Director 탭의 베이스 프롬프트로 간헐적으로 동기화되지 않던 문제를 수정했습니다.

---

## 💻 시스템 요구사항

| 항목 | 최소 요구사항 |
|------|---------------|
| **운영체제** | Windows 10/11 (64비트) |
| **인터넷** | 클라우드 API 사용 시 필요 |
| **LM Studio** | 로컬 모델 사용 시 필요 (Vision 모델 권장) |

### 권장 로컬 모델 (LM Studio)
- `devstral-small` (24B) - 개발자 추천
- `llava` / `bakllava` - 비전 기능 지원
- `qwen-vl` - 비전 기능 지원
- 기타 Vision(이미지 인식) 기능이 있는 모델

---

## 📦 설치 방법

### 방법 1: 실행 파일 사용 (권장) ⭐

1. [Releases](https://github.com/marushin/PeekSavor/releases) 페이지에서 최신 버전의 `PeekSavor_v*.exe` 파일을 다운로드합니다.
2. 다운로드한 exe 파일을 원하는 폴더에 저장합니다.
3. exe 파일을 더블클릭하여 실행합니다.

> **💡 팁**: 처음 실행 시 Windows Defender SmartScreen 경고가 나타날 수 있습니다. "추가 정보" → "실행"을 클릭하세요.


---

## 🏃 빠른 시작

### 1단계: 앱 실행
- exe 파일을 더블클릭하거나, 소스에서 `python main.py` 실행

### 2단계: API 프로바이더 설정
1. 프로바이더 타입 선택 (예: Google, LMStudio)
2. PROVIDER 설정 우측 톱니바퀴 클릭
4. API Key/URL 입력
6. **"설정저장"** 버튼으로 프로바이더 추가

### 3단계: 이미지 분석
1. 이미지를 앱 화면에 드래그 앤 드롭
2. 원하는 프롬프트 옵션 선택 (좌측 사이드바)
3. **"프롬프트 생성"** 버튼 클릭
4. 분석결과 창 옆에 복사 아이콘 클릭으로 복사

---

## 📖 상세 사용법

### Image Studio 탭

#### 이미지 로드 방법
1. **드래그 앤 드롭**: 파일 탐색기에서 이미지를 앱 화면에 끌어다 놓기

#### 줌(확대/축소) 컨트롤
화면 상단의 드롭다운에서 줌 레벨을 선택할 수 있습니다:
- **Fit Screen**: 화면에 맞게 축소 (기본값)
- **Fill Screen**: 화면을 채우도록 확대
- **Actual Size (100%)**: 원본 크기
- **25% ~ 400%**: 퍼센트 단위 확대/축소

#### 프롬프트 생성 과정
1. 이미지 로드 후 좌측 사이드바에서 원하는 옵션 선택
2. **"프롬프트 생성"** 버튼 클릭
3. 하단 텍스트 박스에 프롬프트가 생성됩니다
4. 분석결과 창 옆에 복사 아이콘 클릭으로 복사

### Video Director 탭

AI 비디오 생성 도구(Sora, RunwayML, Pika Labs 등)를 위한 프롬프트를 생성합니다.

#### 사용 방법
1. **Base Prompt**: 
   - Image Studio에서 생성한 프롬프트가 자동으로 입력됩니다
   - 또는 직접 이미지 설명을 입력할 수 있습니다
   
2. **Scene Description**:
   - 원하는 장면의 동작과 움직임을 설명합니다
   - 예시:
     - `Camera slowly zooms in on the subject's face`
     - `The character walks towards the camera`
     - `Cinematic pan from left to right`
     
3. **"Generate Video Prompt"** 클릭하여 최종 비디오 프롬프트 생성

#### Scene Description 작성 팁
| 요소 | 예시 |
|------|------|
| **카메라 무브먼트** | Zoom in, Pan left, Dolly out, Tilt up |
| **인물 동작** | Walking, Turning around, Smiling |
| **분위기** | Dramatic lighting, Soft focus, Cinematic mood |
| **속도** | Slow motion, Time-lapse, Real-time |

---

## ⚙️ API 프로바이더 설정

### 프로바이더 추가 방법

1. 좌측 사이드바에서 **"API Settings"** 클릭
2. 우측 패널 하단의 "Add New Provider" 섹션에서:
   - **Type**: 프로바이더 종류 선택
   - **Name**: 원하는 이름 입력 (예: "My Gemini")
   - **API Key/URL**: 인증 정보 입력
3. **"Verify"** 버튼으로 연결 테스트
4. 성공 시 **"Add"** 버튼이 활성화됩니다

### 지원 프로바이더 목록

#### 🏠 LM Studio (로컬)
- **Type**: LMStudio
- **URL**: `http://localhost:1234/v1` (기본값)
- **장점**: 무료, 인터넷 불필요, 프라이버시 보장
- **설정 방법**:
  1. [LM Studio](https://lmstudio.ai/) 다운로드 및 설치
  2. Vision 지원 모델 다운로드 (llava, bakllava, qwen-vl 등)
  3. 서버 시작 (기본 포트: 1234)
  4. PeekSavor에서 URL 입력

#### 🌐 Google Gemini
- **Type**: Google
- **API Key**: [Google AI Studio](https://aistudio.google.com/)에서 발급
- **지원 모델**: gemini-1.5-flash, gemini-1.5-pro, gemini-2.0-flash-exp
- **장점**: 빠른 속도, 무료 사용량 제공

#### 🔵 OpenAI
- **Type**: OpenAI
- **API Key**: [OpenAI Platform](https://platform.openai.com/)에서 발급
- **지원 모델**: gpt-4o, gpt-4o-mini, gpt-4-turbo
- **장점**: 우수한 이미지 이해 능력

#### 🟣 Claude (Anthropic)
- **Type**: Claude
- **API Key**: [Anthropic Console](https://console.anthropic.com/)에서 발급
- **지원 모델**: claude-3-5-sonnet, claude-3-opus, claude-3-haiku
- **장점**: 섬세한 디테일 묘사

#### 🟠 Qwen (Alibaba)
- **Type**: Qwen
- **API Key**: [DashScope](https://dashscope.aliyuncs.com/)에서 발급
- **지원 모델**: qwen-vl-max, qwen-vl-plus
- **장점**: 아시아 콘텐츠에 강함

### 프로바이더 전환
- 좌측 사이드바 상단의 드롭다운에서 등록된 프로바이더를 선택하면 즉시 전환됩니다
- 모델 목록은 프로바이더 전환 시 자동으로 새로고침됩니다

### 모델 관리
- **새로고침 버튼 (↻)**: 현재 프로바이더의 사용 가능한 모델 목록을 다시 불러옵니다
- **모델 언로드 버튼 (⏏)**: LM Studio 전용 - 현재 로드된 모델을 메모리에서 해제합니다

---

## 🎚️ 프롬프트 옵션 상세 가이드

좌측 사이드바의 "Prompt Options" 섹션에서 다음 옵션을 선택할 수 있습니다:

### Detailed Description (매우 자세하게 묘사)
- **적용 시**: 이미지의 세부 요소를 더욱 상세하게 분석합니다
- **포함 내용**: 빛의 방향과 강도, 질감, 구도, 색상 팔레트, 분위기
- **권장 사용처**: 고품질 이미지 생성이 필요할 때

**예시 (비활성화)**:
```
woman, red dress, garden, sunset, portrait
```

**예시 (활성화)**:
```
young woman with flowing auburn hair, elegant crimson silk dress with subtle 
sheen, standing in a lush English garden, golden hour sunset casting warm 
orange-pink light from the left, soft bokeh background, three-quarter portrait 
composition, film grain texture, romantic atmosphere
```

### Natural Language (자연스러운 언어로 묘사)
- **적용 시**: 콤마로 구분된 키워드 대신 완전한 문장 형태로 출력합니다
- **권장 사용처**: Midjourney, DALL-E 등 자연어 프롬프트를 선호하는 도구

**예시 (비활성화)**:
```
cat, sleeping, windowsill, afternoon sunlight
```

**예시 (활성화)**:
```
A fluffy orange tabby cat peacefully sleeping on a wooden windowsill, 
bathed in warm afternoon sunlight streaming through the window.
```

### Korean (한국어)
- **적용 시**: 모든 분석 결과를 한국어로 출력합니다
- **용도**: 한국어 프롬프트가 필요하거나 내용을 한국어로 확인하고 싶을 때

**예시**:
```
부드러운 햇살이 비치는 창가에서 평화롭게 잠든 주황색 얼룩 고양이, 
따스한 오후의 분위기, 아늑한 분위기
```

### Extract Text / OCR
- **적용 시**: 이미지 내의 모든 텍스트를 추출합니다
- **특징**: **다른 옵션들과 함께 사용 불가** - OCR 활성화 시 다른 옵션은 자동으로 비활성화됩니다
- **용도**: 스크린샷, 문서, 간판 등에서 텍스트 추출

> ⚠️ **주의**: OCR 모드에서는 이미지 묘사가 아닌 텍스트 추출만 수행됩니다.

### 옵션 조합 예시

| Detailed | Natural | Korean | 결과 |
|----------|---------|--------|------|
| ❌ | ❌ | ❌ | 영어 키워드 (Stable Diffusion용) |
| ✅ | ❌ | ❌ | 상세 영어 키워드 |
| ❌ | ✅ | ❌ | 영어 자연어 문장 |
| ✅ | ✅ | ❌ | 상세 영어 자연어 문장 |
| ❌ | ❌ | ✅ | 한국어 키워드 |
| ✅ | ✅ | ✅ | 상세 한국어 자연어 문장 |

---

## ❓ 자주 묻는 질문

### Q: 처음 실행했는데 모델이 없다고 나옵니다.
**A**: API 프로바이더를 먼저 설정해야 합니다. 좌측 "API Settings" 버튼을 클릭하여 프로바이더를 추가하세요.

### Q: LM Studio를 사용하고 싶은데 어떻게 하나요?
**A**: 
1. LM Studio 앱을 설치하고 실행합니다
2. Vision 지원 모델을 다운로드합니다 (llava, bakllava 등)
3. "Local Server" 탭에서 서버를 시작합니다
4. PeekSavor의 API Settings에서 Type을 "LMStudio"로, URL을 `http://localhost:1234/v1`로 설정합니다

### Q: 무료로 사용할 수 있나요?
**A**: 
- **LM Studio (로컬)**: 완전 무료
- **Google Gemini**: 무료 사용량 제공 (제한적)
- **OpenAI/Claude**: 유료 API 키 필요

### Q: 어떤 이미지 형식을 지원하나요?
**A**: JPG, JPEG, PNG, GIF, BMP, WebP 등 대부분의 일반적인 이미지 형식을 지원합니다.

### Q: 프롬프트 생성이 느립니다.
**A**: 
- 클라우드 API: 네트워크 상태 확인
- LM Studio: 더 작은 모델 사용 또는 GPU 가속 확인
- 이미지 크기가 너무 크면 처리 시간이 길어질 수 있습니다

### Q: 설정이 저장되지 않습니다.
**A**: `config.ini` 파일이 exe 파일과 같은 폴더에 생성됩니다. 해당 폴더에 쓰기 권한이 있는지 확인하세요.

---

## 🔧 문제 해결

### 앱이 실행되지 않는 경우
1. Windows 10/11 64비트인지 확인
2. Visual C++ Redistributable 설치 ([다운로드](https://aka.ms/vs/17/release/vc_redist.x64.exe))
3. 바이러스 백신에서 앱을 예외로 추가

### API 연결 오류
```
Error: Connection refused
```
- LM Studio 서버가 실행 중인지 확인
- URL이 정확한지 확인 (기본: `http://localhost:1234/v1`)
- 방화벽에서 포트 1234가 허용되어 있는지 확인

### 모델 목록이 비어 있는 경우
- 새로고침 버튼(↻) 클릭
- LM Studio: 모델이 로드되어 있는지 확인
- 클라우드 API: API 키가 유효한지 확인

### 이미지가 표시되지 않는 경우
- 지원되는 형식인지 확인 (JPG, PNG, GIF, BMP, WebP)
- 파일이 손상되지 않았는지 확인
- 파일 경로에 한글이나 특수문자가 있으면 문제가 될 수 있습니다


---

## 📝 라이선스

이 프로젝트는 [MIT License](LICENSE)에 따라 배포됩니다.




<div align="center">

**참고**: 이 프로젝트는 로컬 AI 서버와 통신하므로, 외부 인터넷 연결 없이도 (모델 다운로드 후) 안전하게 프라이버시를 지키며 사용할 수 있습니다.

Made with ❤️ by [marushin](https://github.com/marushin)

</div>
