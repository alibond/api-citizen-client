# swagger_client.RestrictedApi

All URIs are relative to *https://api.cd.italia.it/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_info**](RestrictedApi.md#get_info) | **GET** /info | API test endpoint
[**get_message**](RestrictedApi.md#get_message) | **GET** /messages/{fiscal_code}/{id} | Get Message
[**get_messages_by_user**](RestrictedApi.md#get_messages_by_user) | **GET** /messages/{fiscal_code} | Get messages by user
[**get_service**](RestrictedApi.md#get_service) | **GET** /services/{service_id} | Get Service
[**get_services_by_recipient**](RestrictedApi.md#get_services_by_recipient) | **GET** /profiles/{recipient}/sender-services | Get Services by recipient
[**get_visible_services**](RestrictedApi.md#get_visible_services) | **GET** /services | Get all visibile services.
[**upsert_profile**](RestrictedApi.md#upsert_profile) | **POST** /profiles/{fiscal_code} | Updates a User Profile

# **get_info**
> object get_info()

API test endpoint

An endpoint to test authenticated access to the API backend.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: SubscriptionKey
configuration = swagger_client.Configuration()
configuration.api_key['Ocp-Apim-Subscription-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Ocp-Apim-Subscription-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.RestrictedApi(swagger_client.ApiClient(configuration))

try:
    # API test endpoint
    api_response = api_instance.get_info()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RestrictedApi->get_info: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

**object**

### Authorization

[SubscriptionKey](../README.md#SubscriptionKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_message**
> MessageResponseWithContent get_message(fiscal_code, id)

Get Message

The previously created message with the provided message ID is returned.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: SubscriptionKey
configuration = swagger_client.Configuration()
configuration.api_key['Ocp-Apim-Subscription-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Ocp-Apim-Subscription-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.RestrictedApi(swagger_client.ApiClient(configuration))
fiscal_code = 'fiscal_code_example' # str | The fiscal code of the user, all upper case.
id = 'id_example' # str | The ID of the message.

try:
    # Get Message
    api_response = api_instance.get_message(fiscal_code, id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RestrictedApi->get_message: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fiscal_code** | **str**| The fiscal code of the user, all upper case. | 
 **id** | **str**| The ID of the message. | 

### Return type

[**MessageResponseWithContent**](MessageResponseWithContent.md)

### Authorization

[SubscriptionKey](../README.md#SubscriptionKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_messages_by_user**
> InlineResponse200 get_messages_by_user(fiscal_code, cursor=cursor)

Get messages by user

Returns the messages for the user identified by the provided fiscal code. Messages will be returned in inverse acceptance order (from last to first). The \"next\" field, when present, contains an URL pointing to the next page of results.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: SubscriptionKey
configuration = swagger_client.Configuration()
configuration.api_key['Ocp-Apim-Subscription-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Ocp-Apim-Subscription-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.RestrictedApi(swagger_client.ApiClient(configuration))
fiscal_code = 'fiscal_code_example' # str | The fiscal code of the user, all upper case.
cursor = 'cursor_example' # str | An opaque identifier that points to the next item in the collection. (optional)

try:
    # Get messages by user
    api_response = api_instance.get_messages_by_user(fiscal_code, cursor=cursor)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RestrictedApi->get_messages_by_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fiscal_code** | **str**| The fiscal code of the user, all upper case. | 
 **cursor** | **str**| An opaque identifier that points to the next item in the collection. | [optional] 

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[SubscriptionKey](../README.md#SubscriptionKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_service**
> ServicePublic get_service(service_id)

Get Service

A previously created service with the provided service ID is returned.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: SubscriptionKey
configuration = swagger_client.Configuration()
configuration.api_key['Ocp-Apim-Subscription-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Ocp-Apim-Subscription-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.RestrictedApi(swagger_client.ApiClient(configuration))
service_id = 'service_id_example' # str | The ID of an existing Service.

try:
    # Get Service
    api_response = api_instance.get_service(service_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RestrictedApi->get_service: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **service_id** | **str**| The ID of an existing Service. | 

### Return type

[**ServicePublic**](ServicePublic.md)

### Authorization

[SubscriptionKey](../README.md#SubscriptionKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_services_by_recipient**
> InlineResponse2002 get_services_by_recipient(recipient)

Get Services by recipient

Returns the service IDs of all the services that have contacted the recipient, identified by the provided fiscal code, at least once.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: SubscriptionKey
configuration = swagger_client.Configuration()
configuration.api_key['Ocp-Apim-Subscription-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Ocp-Apim-Subscription-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.RestrictedApi(swagger_client.ApiClient(configuration))
recipient = 'recipient_example' # str | The recipient's fiscal code.

try:
    # Get Services by recipient
    api_response = api_instance.get_services_by_recipient(recipient)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RestrictedApi->get_services_by_recipient: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recipient** | **str**| The recipient&#x27;s fiscal code. | 

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[SubscriptionKey](../README.md#SubscriptionKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_visible_services**
> InlineResponse2002 get_visible_services()

Get all visibile services.

Returns all the services that have the 'is_visibile' field value set to true.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: SubscriptionKey
configuration = swagger_client.Configuration()
configuration.api_key['Ocp-Apim-Subscription-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Ocp-Apim-Subscription-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.RestrictedApi(swagger_client.ApiClient(configuration))

try:
    # Get all visibile services.
    api_response = api_instance.get_visible_services()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RestrictedApi->get_visible_services: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[SubscriptionKey](../README.md#SubscriptionKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upsert_profile**
> InlineResponse2001 upsert_profile(fiscal_code, body=body)

Updates a User Profile

Create or update the preferences for the user identified by the provided fiscal code.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: SubscriptionKey
configuration = swagger_client.Configuration()
configuration.api_key['Ocp-Apim-Subscription-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Ocp-Apim-Subscription-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.RestrictedApi(swagger_client.ApiClient(configuration))
fiscal_code = 'fiscal_code_example' # str | The fiscal code of the user, all upper case.
body = swagger_client.ExtendedProfile() # ExtendedProfile |  (optional)

try:
    # Updates a User Profile
    api_response = api_instance.upsert_profile(fiscal_code, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RestrictedApi->upsert_profile: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fiscal_code** | **str**| The fiscal code of the user, all upper case. | 
 **body** | [**ExtendedProfile**](ExtendedProfile.md)|  | [optional] 

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

[SubscriptionKey](../README.md#SubscriptionKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

