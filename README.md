# moment-token

제품 UI용 디자인 토큰 패키지입니다. CSS 변수, SCSS 변수, Tailwind 테마 토큰을 한 번에 사용할 수 있도록 구성되어 있습니다.

## 특징

- 웹 앱에서 바로 사용하는 CSS 커스텀 프로퍼티 제공
- Sass 기반 프로젝트용 SCSS 변수 제공
- Tailwind v4 `@theme` 지원
- 디자인 토큰 원본을 JSON으로 관리 가능
- 토큰 소스 기반 자동 생성 구조

## 설치

```bash
npm install @soyen98/moment-token
```

## 사용 방법

### CSS

```css
@import "@soyen98/moment-token/css";

.card {
  background: var(--color-surface-default);
  color: var(--color-text-primary);
  border-radius: var(--radius-md);
  padding: var(--spacing-4);
}
```

### SCSS

```scss
@use "@soyen98/moment-token/scss" as *;

.card {
  background: $color-surface-default;
  color: $color-text-primary;
  border-radius: $radius-md;
  padding: $spacing-4;
}
```

### Tailwind CSS

```css
@import "tailwindcss";
@import "@soyen98/moment-token/tailwind";
```

그 다음, 프로젝트에서 다음처럼 바로 사용할 수 있습니다.

```html
<div class="bg-[var(--color-brand-primary)] text-white rounded-md p-4">
  Moment token demo
</div>
```

## 제공되는 토큰 그룹

- Color: `--color-*`
- Spacing: `--spacing-*`
- Radius: `--radius-*`
- Typography: `--font-size-*`, `--leading-*`, `--tracking-*`, `--font-*`

예시:

```css
--color-brand-primary
--color-text-primary
--spacing-4
--radius-md
--font-size-h1
--leading-normal
```

## 패키지 export

```js
import "@soyen98/moment-token/css";
import "@soyen98/moment-token/scss";
import "@soyen98/moment-token/tailwind";
```

또한 원본 토큰 JSON 파일은 `tokens/` 경로에 포함되어 있어, 디자인 동기화나 커스텀 도구 제작에도 활용할 수 있습니다.

## 로컬 개발

```bash
npm install
npm run build
```

이 명령을 실행하면 `dist/` 디렉터리에 배포용 산출물이 생성됩니다.

## 라이선스

MIT

## 저장소

https://github.com/dusml/moment-token

