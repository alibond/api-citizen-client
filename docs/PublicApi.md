# swagger_client.PublicApi

All URIs are relative to *https://api.cd.italia.it/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_message**](PublicApi.md#get_message) | **GET** /messages/{fiscal_code}/{id} | Get Message
[**get_profile**](PublicApi.md#get_profile) | **GET** /profiles/{fiscal_code} | Get a User Profile
[**submit_messagefor_user**](PublicApi.md#submit_messagefor_user) | **POST** /messages/{fiscal_code} | Submit a message

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
api_instance = swagger_client.PublicApi(swagger_client.ApiClient(configuration))
fiscal_code = 'fiscal_code_example' # str | The fiscal code of the user, all upper case.
id = 'id_example' # str | The ID of the message.

try:
    # Get Message
    api_response = api_instance.get_message(fiscal_code, id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PublicApi->get_message: %s\n" % e)
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

# **get_profile**
> InlineResponse2001 get_profile(fiscal_code)

Get a User Profile

Returns the preferences for the user identified by the provided fiscal code. The field `sender_allowed` is set fo `false` in case the service which is calling the API is blacklisted by the user.

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
api_instance = swagger_client.PublicApi(swagger_client.ApiClient(configuration))
fiscal_code = 'fiscal_code_example' # str | The fiscal code of the user, all upper case.

try:
    # Get a User Profile
    api_response = api_instance.get_profile(fiscal_code)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PublicApi->get_profile: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fiscal_code** | **str**| The fiscal code of the user, all upper case. | 

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

[SubscriptionKey](../README.md#SubscriptionKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **submit_messagefor_user**
> InlineResponse201 submit_messagefor_user(fiscal_code, body=body)

Submit a message

Submits a message to a user. On error, the reason is returned in the response payload. In order to call `submitMessageforUser`, before sending any message, the sender MUST call `getProfile` and check that the profile exists (for the specified fiscal code) and that the `sender_allowed` field of the user's profile it set to `true`.

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
api_instance = swagger_client.PublicApi(swagger_client.ApiClient(configuration))
fiscal_code = 'fiscal_code_example' # str | The fiscal code of the user, all upper case.
body = swagger_client.NewMessage() # NewMessage |  (optional)

try:
    # Submit a message
    api_response = api_instance.submit_messagefor_user(fiscal_code, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PublicApi->submit_messagefor_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fiscal_code** | **str**| The fiscal code of the user, all upper case. | 
 **body** | [**NewMessage**](NewMessage.md)|  | [optional] 

### Return type

[**InlineResponse201**](InlineResponse201.md)

### Authorization

[SubscriptionKey](../README.md#SubscriptionKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

