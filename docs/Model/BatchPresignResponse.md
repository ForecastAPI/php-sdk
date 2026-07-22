# # BatchPresignResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**upload_url** | **string** | Presigned URL — HTTP PUT the JSON file here, including any returned headers | [optional]
**headers** | **array<string,string>** | Headers that must be sent with the upload request | [optional]
**file_key** | **string** | Pass this as &#x60;file_key&#x60; to POST /v2/batch/forecast after uploading | [optional]
**expires_in** | **int** | Seconds the upload URL stays valid | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
