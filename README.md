# React TypeScript 를 이용한 이미지 갤러리 

yarn 설치
`npm install -g yarn`

React TypeScript 탬플릿 설치
`yarn create react-app "프로젝트명" -template typescript`

화면에 띄우기
`yarn start`

---

img태그 src 경로

```jsx
function ImageBox(props:{
  src:string;
}){
  return (
    <div className="image-box">
      <img src={props.src} alt="" />
    </div>
  );
}

export default ImageBox;
```
---

useRef 는 태그를 반환할 수 있음


imageList 가 없으면 태그가 나타남

imageList 가 추가되면 태그가 사라짐

```tsx
<div className="initial-box">
    { 
      imageList.length === 0 && 
      <div className="text-center">
        이미지가 없습니다.<br />
        이미지를 추가해주세요.
      </div>
    }
</div>
```

---

이미지 드래그 앤 드랍

react-dropzone 라이브러리

[https://react-dropzone.js.org/](https://react-dropzone.js.org/)

`yarn add react-dropzone`

`yarn add @types/react-dropzone`
