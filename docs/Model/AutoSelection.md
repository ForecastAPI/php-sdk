# # AutoSelection

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**requested** | **string** |  | [optional]
**selected** | **string** | The model that produced this response | [optional]
**reason** | **string** | Why this model was selected. &#x60;scored_winner&#x60; means one model beat every alternative by a clear margin on realized accuracy for this identifier; everything else means the evidence-gathering default was served. | [optional]
**scores** | [**array<string,\ForecastAPI\Sdk\Model\AutoSelectionScoresValue>**](AutoSelectionScoresValue.md) | Per-model realized-accuracy scorecard for this identifier, when one exists | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
