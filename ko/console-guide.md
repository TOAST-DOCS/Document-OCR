## AI Service > Document OCR > 콘솔 사용 가이드

콘솔을 통해 사업자등록증 파일을 올리고 분석 결과를 얻을 수 있습니다. 


## 사업자등록증 분석


### 분석을 위한 사진 업로드

분석할 사업자등록증 이미지를 업로드 합니다.

- 이미지은 다음 2가지 방법으로 업로드 할 수 있습니다.
    1. 이미지 업로드 버튼 클릭
    2. 이미지 드래그 앤드 드롭

### 입력 이미지 가이드
    
- .pdf, .jpeg, .png 형식의 사업자등록증 이미지 분석 기능을 지원합니다. 
    - 최대 용량: 5MB
    - 권장 해상도: 1280 x 720 이상
- pdf의 경우 단일 페이지에 대한 분석 결과만 제공합니다. (여러 페이지인 경우 첫 페이지에 대한 분석 결과가 제공됩니다.)
- 평평한 곳에 놓고 최대한 바르게 펴진 이미지로 인식해 주세요.
- 사각 형태의 가득 찬 이미지로 인식해 주세요.
- 카메라 플래쉬 등으로 인한 빛 반사나 그늘로 인해 글자가 잘 안 보이는 경우 정확한 Key-Value 추출이 어려울 수 있습니다.
- 흑백/컬러 이미지에 대해 결과 분석이 가능하지만, 정확한 분석을 위해서 컬러 이미지를 권장합니다.
- 사업자등록증은 한국어에 한해 분석 결과를 제공합니다.

### 분석

사진을 업로드한 후 분석 버튼을 클릭하면 분석 결과가 화면 오른쪽에 나타납니다.

![Business Registration](http://static.toastoven.net/prod_document_ocr/business_ocr_console_ko.png)

* [텍스트(Key Value)] 분석된 사업자등록증의 내용을 Key/Value 형태로 표시합니다.
* [JSON] 분석한 결과를 JSON 형태로 표시합니다.
    * [success] 분석 성공/실패 여부
    * [fileType] 파일 확장자 (pdf, jpg, png)
    * [keyValues] 분석 결과
        * [key] 사업자등록증 내 key에 해당하는 값(구분, 상호명, 주소 등등)
        * [value] 특정 key에 해당하는 값
        * [conf] 분석 결과에 대한 신뢰도
    * [unitType] boxes 좌표 단위 (기본 pixel, PDF의 경우 point)
    * [resolution] 권장 해상도(HD 1280*720px) 이상이면 normal, 권장 해상도 미만은 low
    * [boxes] 인식 영역에 대한 이미지 상의 좌표값 (box 별 {x1, y1, x2, y2, x3, y3, x4, y4} 형태)
    
        ![bbox](http://static.toastoven.net/prod_document_ocr/bbox.png)
    
* 분셕 결과에 대한 복사 및 다운로드(Excel, JSON) 기능을 제공합니다.