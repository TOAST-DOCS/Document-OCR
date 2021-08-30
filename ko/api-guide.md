## AI Service > Document OCR > API 가이드

### 사업자등록증 분석 API
- .pdf, .jpeg, .png 형식의 사업자등록증 이미지 분석 기능을 지원합니다. (최대 용량: 5MB)

#### 요청

[URI]

| 메서드 | URI |
|---|---|
| POST | https://kr1-ocr.api.nhncloudservice.com/v1.0/appkeys/{appKey}/business |

[요청 본문]

- {appKey}는 콘솔 상단 "URL & Appkey" 메뉴에서 확인이 가능합니다.
- 이미지 파일의 Binary Data를 넣습니다.

```
curl -X POST 'https://kr1-ocr.api.nhncloudservice.com/v1.0/appkeys/{appKey}/business' \
--data-binary '@sample.png' 
```

#### 응답

[응답 본문]

```
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "data": {
        "key_value": [
            {
                "key":"구분",
                "value":" 간이과세자",
                "conf":0.93
            },
            {
                "key":"등록번호",
                "value":"270-06-01309",
                "conf":1
            },
            ...
        ],
        "bbox": [
            [2095,142,2237,142,2237,202,2095,202],
            [751,361,1733,361,1733,510,751,510],
            ...
        ],
        "flag": true
    }
}
```

[필드]

| 이름 | 타입 | 설명 |
|---|---|---|
| key_value | List | 인식 결과 목록 |
| key_value.key | String | 인식 항목명 |
| key_value.value | String | 인식 내용 |
| key_value.conf | double | 인식 결과 신뢰도 |
| bbox | List | 인식 영역 좌표 [x1, y1, x2, y2, x3, y3, x4, y4] |
| flag | boolean | 분석 성공 여부 |

* bbox
 
    ![bbox](http://static.toastoven.net/prod_document_ocr/bbox.png)

