# كيفية اصدار الشهادة

مع الرمز الذي تم الحصول عليه بالفعل ، من خلال المصادقة.
راجع: [كيفية المصادقة على API] (../../quickStart/howToAuthenticate/).<br>
استخدم رمز الحامل للمصادقة على واجهة برمجة التطبيقات.
قم بإجراء مكالمة إلى نقطة نهاية **/api/OriginCertificate** ، باستخدام طريقة POST:

![api/OriginCertificate!](../../assets/post_co.png "api/OriginCertificate")

## تقديم الطلب

```json
{
  "incotermType": "Cip",
  "currency": 2,
  "cost": 487844.54,
  "freightCost": 0,
  "insurance": 0,
  "landingFee": 0,
  "others": 0,
  "invoiceNumber": "JIU5454",
  "emissionDate": "2023-02-06T03:00:00.000Z",
  "originCountry": "BRA",
  "destinationCountry": "DZA",
  "certificateLanguage": "English",
  "certificateEmail": "email@email.com",
  "observations": "",
  "hasCertificateBrazilianOrigin": true,
  "companiesEnvolved": {
    "exporter": {
      "id": 1
    },
    "importer": {
      "id": 2029,
      "crmId": null,
      "name": "Importador na BRF teste",
      "website": null,
      "creationDate": "2023-01-16T20:00:55.000Z",
      "associationDate": null,
      "idCountry": 1,
      "city": "Cidade",
      "state": null,
      "phoneNumber": null,
      "phoneNumber2": null,
      "street": "Endereço",
      "number": null,
      "contactEmail": "gcampos@ccab.org.br",
      "associationType": null,
      "certifierType": null,
      "fantasyName": null,
      "stateRegistry": null,
      "sectorId": null,
      "primaryChapterId": null,
      "zipCode": null,
      "poBox": "54545454",
      "complement": "complemento",
      "fax": null,
      "cnpj": null,
      "status": 1,
      "profileExtension": null,
      "coverExtension": null,
      "idTimezone": null,
      "district": null,
      "idAssociateCreated": 822,
      "erpId": null,
      "traderType": 1,
      "idAccessGroup": 36,
      "companyType": 1,
      "exporter": 1,
      "tradelensId": null,
      "favorite": true
    }
  },
  "shipmentInformation": {
    "shipmentType": 2,
    "shippingDate": "2023-03-30T03:00:00.000Z",
    "blawbNumber": null,
    "imoNumber": null,
    "vesselName": null,
    "id": null,
    "portOfDeparture": 144,
    "portOfDestination": 1
  },
  "products": [
    {
      "ncm": "97053100",
      "idUnitMeasure": 14,
      "idUnitMeasureWeight": 2,
      "quantity": 462,
      "grossWeight": 16.4145,
      "netWeight": 15.4547,
      "productionDate": "2023-02-02T03:00:00.000Z",
      "expirationDate": "2024-03-31T03:00:00.000Z",
      "description": "Over 100 years old",
      "sif": null,
      "marks": null,
      "productValue": 487844.54,
      "currency": 2
    }
  ]
}

```

## العائد المتوقع

**لفة**

```
curl -X POST "https://api.hom.ellos.org.br/ellos/easytrade/OriginCertificate" -H "accept: */*" -H "Content-Type: application/json-patch+json" -d "{\"incotermType\":\"Cip\",\"currency\":2,\"cost\":487844.54,\"freightCost\":0,\"insurance\":0,\"landingFee\":0,\"others\":0,\"invoiceNumber\":\"JIU5454\",\"emissionDate\":\"2023-02-06T03:00:00.000Z\",\"originCountry\":\"BRA\",\"destinationCountry\":\"DZA\",\"certificateLanguage\":\"English\",\"certificateEmail\":\"email@email.com\",\"observations\":\"\",\"hasCertificateBrazilianOrigin\":true,\"companiesEnvolved\":{\"exporter\":{\"id\":1},\"importer\":{\"id\":2029,\"crmId\":null,\"name\":\"Importador na BRF teste\",\"website\":null,\"creationDate\":\"2023-01-16T20:00:55.000Z\",\"associationDate\":null,\"idCountry\":1,\"city\":\"Cidade\",\"state\":null,\"phoneNumber\":null,\"phoneNumber2\":null,\"street\":\"Endereço\",\"number\":null,\"contactEmail\":\"gcampos@ccab.org.br\",\"associationType\":null,\"certifierType\":null,\"fantasyName\":null,\"stateRegistry\":null,\"sectorId\":null,\"primaryChapterId\":null,\"zipCode\":null,\"poBox\":\"54545454\",\"complement\":\"complemento\",\"fax\":null,\"cnpj\":null,\"status\":1,\"profileExtension\":null,\"coverExtension\":null,\"idTimezone\":null,\"district\":null,\"idAssociateCreated\":822,\"erpId\":null,\"traderType\":1,\"idAccessGroup\":36,\"companyType\":1,\"exporter\":1,\"tradelensId\":null,\"favorite\":true}},\"shipmentInformation\":{\"shipmentType\":2,\"shippingDate\":\"2023-03-30T03:00:00.000Z\",\"blawbNumber\":null,\"imoNumber\":null,\"vesselName\":null,\"id\":null,\"portOfDeparture\":144,\"portOfDestination\":1},\"products\":[{\"ncm\":\"97053100\",\"idUnitMeasure\":14,\"idUnitMeasureWeight\":2,\"quantity\":462,\"grossWeight\":16.4145,\"netWeight\":15.4547,\"productionDate\":\"2023-02-02T03:00:00.000Z\",\"expirationDate\":\"2024-03-31T03:00:00.000Z\",\"description\":\"Over 100 years old\",\"sif\":null,\"marks\":null,\"productValue\":487844.54,\"currency\":2}]}"
```

**طلب URL**
```
https://api.hom.ellos.org.br/ellos/easytrade/OriginCertificate
```

**شفرة**
```
200
``` 

**وصف**
```
نجاح
```

**تفاصيل**

تُرجع معرّف شهادة المصدر التي تم إنشاؤها في الجدول.

```json
{
  "success": true,
  "data": 1661,
  "errors": null
}
```
