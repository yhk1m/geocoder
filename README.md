# 🗺️ Nominatim Geocoder (CSV 업로드 지원)

OpenStreetMap 기반 **무료 지오코딩 도구**입니다.  
CSV 파일을 업로드하여 대량의 주소를 한 번에 변환할 수 있습니다.

## ✨ 특징

| 항목 | 내용 |
|------|------|
| 💰 비용 | **완전 무료** |
| 🔑 API 키 | **불필요** |
| 🌍 범위 | 전 세계 |
| ⏱️ 제한 | 초당 1요청 (자동 적용) |
| 📁 CSV | **업로드 & 다운로드 지원** |

## 🚀 사용 방법

### 1. GitHub Pages 배포

1. 이 저장소를 Fork
2. Settings → Pages → Deploy from branch 활성화
3. `https://your-username.github.io/repo-name/` 접속

### 2. CSV 일괄 변환 사용법

1. **파일 업로드**: CSV 파일을 드래그 & 드롭 또는 클릭하여 선택
2. **열 선택**: 주소가 있는 열 선택 (자동 감지 지원)
3. **변환 실행**: 🚀 버튼 클릭
4. **결과 다운로드**: 원본 데이터 + 위경도 좌표가 포함된 CSV 다운로드

## 📋 기능

### 📁 CSV 일괄 변환
- 드래그 & 드롭 파일 업로드
- 열 자동 감지 (주소, address 등)
- 데이터 미리보기
- 예상 소요 시간 표시
- 진행률 실시간 표시
- 중간 중지 가능
- 결과 CSV 다운로드 (원본 데이터 유지)
- 실패 항목만 따로 다운로드

### 📍 단일 변환
- 주소 → 좌표 변환
- Google Maps / OSM 링크 제공

### 🔄 역지오코딩
- 좌표 → 주소 변환
- 상세 주소 정보 제공

## 📁 파일 구조

```
nominatim-geocoder/
├── index.html    # 웹 인터페이스 (CSV 업로드 지원)
└── README.md     # 설명서
```

## ⚠️ 주의사항

- **속도 제한**: 초당 1요청 (100개 주소 ≈ 2분)
- **한국 주소**: 도로명주소 권장, 상세 번지는 정확도 낮을 수 있음
- **인코딩**: UTF-8 CSV 권장 (엑셀에서 저장 시 "CSV UTF-8" 선택)

## 📊 CSV 형식 예시

### 입력 파일
```csv
이름,주소,전화번호
스타벅스 종로점,서울특별시 종로구 세종대로 110,02-1234-5678
카페 부산점,부산광역시 해운대구 해운대해변로 264,051-1234-5678
```

### 출력 파일
```csv
이름,주소,전화번호,위도,경도,찾은주소,지오코딩상태
스타벅스 종로점,서울특별시 종로구 세종대로 110,02-1234-5678,37.5666,126.9784,"Seoul, South Korea",OK
카페 부산점,부산광역시 해운대구 해운대해변로 264,051-1234-5678,35.1587,129.1604,"Busan, South Korea",OK
```

## 🔗 관련 링크

- [Nominatim 공식 사이트](https://nominatim.org/)
- [OpenStreetMap](https://www.openstreetmap.org/)
- [Papa Parse (CSV 라이브러리)](https://www.papaparse.com/)

## 📜 라이선스

MIT License

데이터: © OpenStreetMap contributors (ODbL)

---

Made with ❤️ for geography education
