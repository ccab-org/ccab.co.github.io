# Como emitir Certificado

Com o token já obtido, através da autenticação.
Veja: [Como se autenticar na API](../../quickStart/howToAuthenticate/).<br>
Utilize o Bearer Token para autenticar na API.
Realize uma chamada ao endpoint **/api/OriginCertificate**, utilizando o método POST:

![api/OriginCertificate!](../../assets/post_co.png "api/OriginCertificate")

## Fazendo a requisição

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

## Retorno esperado

**Curl**

```
curl -X POST "https://api.dev.casaarabe.org.br/ellos/easytrade/OriginCertificate" -H "accept: */*" -H "Content-Type: application/json-patch+json" -d "{\"incotermType\":\"Cip\",\"currency\":2,\"cost\":487844.54,\"freightCost\":0,\"insurance\":0,\"landingFee\":0,\"others\":0,\"invoiceNumber\":\"JIU5454\",\"emissionDate\":\"2023-02-06T03:00:00.000Z\",\"originCountry\":\"BRA\",\"destinationCountry\":\"DZA\",\"certificateLanguage\":\"English\",\"certificateEmail\":\"email@email.com\",\"observations\":\"\",\"hasCertificateBrazilianOrigin\":true,\"companiesEnvolved\":{\"exporter\":{\"id\":1},\"importer\":{\"id\":2029,\"crmId\":null,\"name\":\"Importador na BRF teste\",\"website\":null,\"creationDate\":\"2023-01-16T20:00:55.000Z\",\"associationDate\":null,\"idCountry\":1,\"city\":\"Cidade\",\"state\":null,\"phoneNumber\":null,\"phoneNumber2\":null,\"street\":\"Endereço\",\"number\":null,\"contactEmail\":\"gcampos@ccab.org.br\",\"associationType\":null,\"certifierType\":null,\"fantasyName\":null,\"stateRegistry\":null,\"sectorId\":null,\"primaryChapterId\":null,\"zipCode\":null,\"poBox\":\"54545454\",\"complement\":\"complemento\",\"fax\":null,\"cnpj\":null,\"status\":1,\"profileExtension\":null,\"coverExtension\":null,\"idTimezone\":null,\"district\":null,\"idAssociateCreated\":822,\"erpId\":null,\"traderType\":1,\"idAccessGroup\":36,\"companyType\":1,\"exporter\":1,\"tradelensId\":null,\"favorite\":true}},\"shipmentInformation\":{\"shipmentType\":2,\"shippingDate\":\"2023-03-30T03:00:00.000Z\",\"blawbNumber\":null,\"imoNumber\":null,\"vesselName\":null,\"id\":null,\"portOfDeparture\":144,\"portOfDestination\":1},\"products\":[{\"ncm\":\"97053100\",\"idUnitMeasure\":14,\"idUnitMeasureWeight\":2,\"quantity\":462,\"grossWeight\":16.4145,\"netWeight\":15.4547,\"productionDate\":\"2023-02-02T03:00:00.000Z\",\"expirationDate\":\"2024-03-31T03:00:00.000Z\",\"description\":\"Over 100 years old\",\"sif\":null,\"marks\":null,\"productValue\":487844.54,\"currency\":2}]}"
```

**Request URL**
```
https://api.dev.casaarabe.org.br/ellos/easytrade/OriginCertificate
```

**Code**
```
200
``` 

**Description**
```
Successo
```

**Details**

Retorna o id do certificado de origem criado na tabela.

```json
{
  "success": true,
  "data": 1661,
  "errors": null
}
```
