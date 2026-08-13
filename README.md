# Sieun Kim — Personal Website

개인 연구자 웹사이트. GitHub Pages로 호스팅됩니다.

## 파일 구조

| 파일 | 내용 |
|---|---|
| `index.html` | 메인 페이지 (소개, Research, News, Publications, Education) |
| `projects.html` | 연구 프로젝트 목록 |
| `diary.html` | 사이드 프로젝트 & Growth Notes |

각 파일은 독립된 HTML이라 하나만 수정해도 다른 페이지에 영향이 없어요.
스타일(색·폰트)은 각 파일 상단 `<style>` 안 `:root`에 모여 있습니다.

## 수정하는 법 (GitHub 웹에서)

1. GitHub 저장소에서 수정할 파일 클릭 (예: `index.html`)
2. 오른쪽 위 연필 아이콘(✏️ Edit) 클릭
3. 내용 수정 후 초록색 **Commit changes** 버튼 클릭
4. 1~2분 뒤 웹사이트에 자동 반영

## 자주 하는 수정

### News 추가 (`index.html`)
`<!-- ================= NEWS -->` 섹션에서 아래 블록을 복사해 맨 위에 붙여넣기:

```html
<li><span class="nd">2026</span>
  <span class="nt">여기에 뉴스 내용 (영어로) <span class="badge-hl">optional badge</span></span></li>
```

### Publication 추가 (`index.html`)
`<!-- ================= PUBLICATIONS -->` 섹션에서 기존 `<div class="pub">...</div>` 블록 하나를 통째로 복사해 수정:

```html
<div class="pub">
  <div class="venue-chip">CHI<span class="yr">2027</span></div>
  <div class="pub-body">
    <div class="pub-title">논문 제목</div>
    <div class="pub-authors"><b>Sieun Kim</b>, Co-author</div>
    <div class="pub-venue">Venue 이름</div>
    <div class="pub-links">
      <a class="plink" href="DOI주소" target="_blank">DOI</a>
      <a class="plink" href="PDF주소" target="_blank">PDF</a>
    </div>
  </div>
</div>
```

수상 배지가 필요하면 `pub-title` 아래에:
```html
<span class="pub-award">🏅 Best Paper Honorable Mention (Top 10%)</span>
```

### 프로필 사진 넣기 (`index.html`)
1. 저장소에 사진 업로드 (Add file → Upload files, 예: `photo.jpg`)
2. `index.html`에서 `<div class="hero-photo">` 안의 `🎐`를 지우고:
```html
<img src="photo.jpg" alt="Sieun Kim">
```

### CV 링크 연결 (`index.html`)
CV PDF를 저장소에 업로드한 뒤 `href="#"`를 `href="CV_SieunKim.pdf"`로 변경:
```html
<a class="btn" href="CV_SieunKim.pdf">CV</a>
```

### 색 바꾸기
각 파일 `<style>` 상단의 `:root`에서:
- `--accent: #2b4c7e;` ← 포인트 색 (링크, 버튼)
- 세 파일 모두 같은 값으로 맞춰야 통일감이 유지돼요.

## 로컬에서 미리보기
파일을 더블클릭해 브라우저로 열면 바로 확인할 수 있어요 (서버 불필요).
