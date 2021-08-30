## AI Service > Document OCR > 콘솔 사용 가이드

콘솔을 통해 사업자등록증 파일을 올리고 분석 결과를 얻을 수 있습니다. 

## 사업자등록증 분석

### 얼굴 감지 및 분석을 위한 사진 업로드
이미지 업로드 버튼 클릭 후 이미지를 선택하여 업로드 합니다.

### 분석
사진을 업로드한 후 분석 버튼을 클릭하면 분석 결과가 화면 오른쪽에 나타납니다.

![Business Registration](http://static.toastoven.net/prod_document_ocr/business_ocr_console_ko.png)

* [텍스트(Key Value)] 분석된 사업자등록증의 내용을 Key/Value 형태로 표시합니다.
* [JSON] 분석한 결과를 JSON 형태로 표시합니다.
    * [key] 사업자등록증 내 key에 해당하는 값(구분, 상호명, 주소 등등)
    * [value] 특정 key에 해당하는 값
    * [conf] 분석 결과에 대한 신뢰도
    * [flag] 분석 성공/실패 여부
    * [bbox] 인식 영역에 대한 이미지 상의 좌표값 (box 별 [x1, y1, x2, y2, x3, y3, x4, y4] 형태)
    
        ![bbox](http://static.toastoven.net/prod_document_ocr/bbox.png)
    
* 분셕 결과 복사(JSON) 및 다운로드(CSV) 기능을 제공합니다.