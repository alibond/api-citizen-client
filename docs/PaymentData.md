# PaymentData

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **int** | Amount of payment in euro cent. PagoPA accepts up to 999999999 euro cents. | 
**invalid_after_due_date** | **bool** |  | [optional] [default to False]
**notice_number** | **str** | The field [\&quot;Numero Avviso\&quot;](https://pagopa-specifichepagamenti.readthedocs.io/it/latest/_docs/Capitolo7.html#il-numero-avviso-e-larchivio-dei-pagamenti-in-attesa) of pagoPa, needed to identify the payment. Format is &#x60;&lt;aux digit (1n)&gt;[&lt;application code&gt; (2n)]&lt;codice IUV (15|17n)&gt;&#x60;. See [pagoPa specs](https://www.agid.gov.it/sites/default/files/repository_files/specifiche_attuative_pagamenti_1_3_1_0.pdf) for more info on this field and the IUV. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

