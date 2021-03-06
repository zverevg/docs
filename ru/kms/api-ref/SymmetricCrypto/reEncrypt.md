---
editable: false
---

# Метод reEncrypt
Заново шифрует заданный зашифрованный текст с указанным ключом KMS.
 

 
## HTTP-запрос {#https-request}
```
POST https://kms.yandex/kms/v1/keys/{keyId}:reEncrypt
```
 
## Path-параметры {#path_params}
 
Параметр | Описание
--- | ---
keyId | Обязательное поле. Идентификатор нового ключа, который следует использовать для шифрования.  Максимальная длина строки в символах — 50.
 
## Параметры в теле запроса {#body_params}
 
```json 
{
  "versionId": "string",
  "aadContext": "string",
  "sourceKeyId": "string",
  "sourceAadContext": "string",
  "ciphertext": "string"
}
```

 
Поле | Описание
--- | ---
versionId | **string**<br><p>Идентификатор версии нового ключа, которую следует использовать для шифрования. По умолчанию используется основная версия, если версия не указана явно.</p> <p>Максимальная длина строки в символах — 50.</p> 
aadContext | **string** (byte)<br><p>Дополнительные аутентифицированные данные (AAD-контекст), которые потребуются для расшифровки. Должен быть в кодировке base64.</p> <p>Максимальная длина строки в символах — 8192.</p> 
sourceKeyId | **string**<br><p>Обязательное поле. Идентификатор ключа, которым на текущий момент зашифрован текст. Может быть таким же, как и новый ключ.</p> <p>Максимальная длина строки в символах — 50.</p> 
sourceAadContext | **string** (byte)<br><p>Дополнительные аутентификационные данные, переданные с первоначальным запросом шифрования. Должен быть в кодировке base64.</p> <p>Максимальная длина строки в символах — 8192.</p> 
ciphertext | **string** (byte)<br><p>Обязательное поле. Шифртекст, который следует расшифровать и зашифровать повторно. Должен быть в кодировке base64.</p> 
 
## Ответ {#responses}
**HTTP Code: 200 - OK**

```json 
{
  "keyId": "string",
  "versionId": "string",
  "sourceKeyId": "string",
  "sourceVersionId": "string",
  "ciphertext": "string"
}
```

 
Поле | Описание
--- | ---
keyId | **string**<br><p>Идентификатор ключа, которым в данный момент зашифрован текст.</p> 
versionId | **string**<br><p>Идентификатор версии ключа, которая использовалась для шифрования.</p> 
sourceKeyId | **string**<br><p>Идентификатор ключа, с помощью которого шифртекст был зашифрован ранее.</p> 
sourceVersionId | **string**<br><p>Идентификатор версии ключа, которая использовалась для расшифровки перешифруемых данных.</p> 
ciphertext | **string** (byte)<br><p>Заново зашифрованный шифртекст.</p> 