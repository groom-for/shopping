# Shopping Mall Frontend

React, TypeScript, Vite 기반으로 쇼핑몰 서비스 개발을 위한 초기 환경 설정이 완료된 프로젝트입니다.  
TailwindCSS v3 + shadcn/ui(New York 스타일 + Zinc 컬러)를 적용했습니다.

## 프로젝트 개요
- 프론트엔드 초기 세팅 완료
- UI 컴포넌트 시스템(shadcn/ui) 구축
- React + TS 개발환경 정비
- 쇼핑몰 서비스 개발을 위한 기반 구성

## 기술 스택
- Vite + React + TypeScript
- TailwindCSS v3
- shadcn/ui (New York 스타일)
- CSS Variables (자동 적용)
- Alias (@/*) 경로 설정 적용

## 설치 및 실행
- npm install
- npm run dev

## 주요 구성 파일
- src/index.css (Tailwind v3 설정 적용)
- src/lib/utils.ts (shadcn 기본 유틸)
- tailwind.config.js (shadcn 자동 설정 반영)
- postcss.config.js
- tsconfig.json (alias 설정)
- tsconfig.app.json

## 폴더 구조
- src
  - components
    - ui (shadcn에서 추가되는 컴포넌트)
  - lib
  - pages (추가 예정)
  - routes (추가 예정)

## shadcn 컴포넌트 추가 방법
- npx shadcn@latest add button
- npx shadcn@latest add card
- npx shadcn@latest add input
- npx shadcn@latest add dialog

## 다음 작업 예정
- 레이아웃(Header, Footer) 구성
- 페이지 라우팅(AppRoutes) 설정
- 상품 목록 UI 설계
- 상품 상세 페이지
- 장바구니 / 주문 UI 구성
- Spring Boot 백엔드 API 연동


---
# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is enabled on this template. See [this documentation](https://react.dev/learn/react-compiler) for more information.

Note: This will impact Vite dev & build performances.

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```
