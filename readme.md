# toon.zzoman.com

## 기획의도

* 웹툰서비스
* 이미지만 `attachment` 폴더에 삽입하여 새로운 포스트 생성
* `attachment` 폴더를 읽어서 `JSON` 형태의 파일로 목록화된 data 생성하여 업로드
    * `JSON` 굳이 필요없을 듯. `gulpfile.js` 내에서 변수로 생성하여 사용하는 것으로 수정.
    * 하지만 추후 여러 페이지를 작성할 필요가 있다면? `JSON`이나 `Object`로 데이터를 가지고 있어야 할지도.
* JavaScript는 ES6로 작성


## 구조

```
- /  
    - src/
        - js/
        - scss/
        - template/
    - attachment/
        - thumbnail/
    - dist/             
    - index.html
    - config.json
    - gulpfile.js
```

## Install

    git clone 저장소 [작업위치]
    
프로젝트를 다운로드 한다.

    npm install
    
필요한 `node.js` 모듈을 설치한다.

## get started

1. `config.json` 파일을 수정한다.
```json
{
  "title": "Website Title",
  "description": "Descriptions for your website",
  "rootUrl": "http://localhost:9999/dist"
}
```
    - title : 웹사이트의 제목 입력
    - description : 웹사이트의 설명 입력
    - rootUrl : `dist` 폴더가 업로드될 웹사이트의 접속 루트 입력
    
2. `attachment/` 폴더에 이미지를 위치시킨다. 파일명은 아래의 규칙을 엄수한다.
```
YYYYMMDD_category_title.jpg
```
예를 들면 `20160201_만화_1화.jpg` 이렇게 작성할 수 있다.
 
3. Command Line에서 `gulp build` 명령어로 산출물을 제작한다.
4. 제작된 `dist/`폴더의 내용을 웹사이트에 업로드 한다.