## AI Service > Document OCR > 개요

Document OCR은 NHN Cloud의 OCR(광학 문자 인식) 기술을 통해 사업자등록증의 문자 영역을 인식하고, 영역별 문자를 추출하는 기능을 제공합니다.
사업자등록증 정보를 Database에 저장하거나 문서 처리 자동화를 구현하는 고객사의 경우 활용 할 수 있습니다.

## 주요 기능

* **사업자등록증 문자 영역 인식**
	* 사업자등록증의 문자 영역(Bounding Box)을 인식하고, 해당 영역의 좌표를 제공합니다.
	
* **사업자등록증 주요 데이터 추출 및 분석**
    * 사업자등록증 분류(개인/법인)에 따른 주요 데이터는 Key/Value 한 쌍으로 분석되며, 결과에 대한 정확도(Confidence)를 제공합니다.

* **분석 결과 다운로드**
	* 사업자등록증 파일에서 추출한 결과를 Excel 및 JSON 파일로 다운로드할 수 있습니다.

## 입력 이미지 가이드
    
* .pdf, .jpeg, .png 형식의 사업자등록증 이미지 분석 기능을 지원합니다. 
    * 최대 용량: 5MB
    * 권장 해상도: 1280 x 720 이상
* pdf의 경우 단일 페이지에 대한 분석 결과만 제공합니다. (여러 페이지인 경우 첫 페이지에 대한 분석 결과가 제공됩니다.)
* 평평한 곳에서 최대한 바르게 펴진 상태로 촬영된 이미지를 사용해 주세요.
* 사각 형태의 가득 찬 이미지로 인식해 주세요.
* 카메라 플래쉬 등으로 인한 빛 반사나 그늘로 인해 글자가 잘 안 보이는 경우 정확한 Key-Value 추출이 어려울 수 있습니다.
* 흑백/컬러 이미지에 대해 결과 분석이 가능하지만, 정확한 분석을 위해서 컬러 이미지를 권장합니다.
* 사업자등록증은 한국어에 한해 분석 결과를 제공합니다.

## 서비스 대상
* 사업자등록증을 자동으로 고객사 시스템에 등록하는 경우
* 문서 처리 자동화를 구현하는 경우
* 회계/재무 관리 자동화 솔루션을 구축하는 경우

## Privacy Policy
* While using the Document OCR service, the customer may collect personal and sensitive information of their users. Therefore, the customer of this service must inform a legal notice to their users as per the Personal Information Protection Act and acquire their consent regarding the matter. Also during this process, work consignment relation regarding the processing of personal information may arise between the customer and NHN. The customer who assumes the position of consignor may enter into a consignment contract with the consignee, NHN, separately in writing, and post a privacy policy notice by referencing the following:
    - Consignee: NHN 
    - Consignment Description: Providing Document OCR service
    
## 기술적/관리적 수준에 대한 합의서
* 고객은 Document OCR 서비스를 이용하는 과정에서 수집/이용하는 정보의 민감성을 고려하여 기술적, 관리적 보호조치를 충실히 이행하여야 합니다.
* 고객은 Document OCR 서비스를 통하여 인식된 정보를 전달받기 위하여 Document OCR 서비스 이용 개시전 통신구간 암호화를 완료하여야 합니다.
* 고객은 Document OCR 서비스에 인식 요청을 하는 원본 데이터는 안전한 장소에 저장되어야 하며, 외부 노출가능한 URL을 통해 접근 불가 해야 합니다.
* 고객은 Document OCR 서비스에서 안전한 인식결과 데이터를 제공하기 위해서 권장하는 전송방식(전용선, IPSecVPN 등)을 채택해야 합니다.
* 고객은 Document OCR 서비스를 통하여 인식된 정보를 저장/보관/관리하는 데 있어서 개인정보 보호법 등 관련 법령을 준수하여야 합니다.
* 회사는 고객이 위에서 정한 기술적, 관리적 조치를 모두 갖추고 있는지 확인이 필요한 경우 고객에게 증빙을 요청할 수 있습니다.
* 위와 같은 사항은 Document OCR 서비스를 통하여 고객이 수집/이용하는 정보가 중요한 정보에 해당하기에 고객에게 요청하는 사항이며, 고객은 위 사항의 이행을 보증하고 위반으로 인하여 발생하는 정보주체, 규제기관 등에 대한 모든 책임을 부담하는 것을 확인합니다.