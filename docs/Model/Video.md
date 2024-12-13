# Video

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**classification** | **string[]** | The intended use for this video content. Currently, videos can only be added and associated with eBay listings, so the only supported value is &lt;code&gt;ITEM&lt;/code&gt;. | [optional] 
**description** | **string** | The description of the video. The video description is an optional field that can be set using the &lt;a href&#x3D;\&quot; /api-docs/commerce/media/resources/video/methods/createVideo\&quot; target&#x3D;\&quot;_blank\&quot;&gt;createVideo&lt;/a&gt; method. | [optional] 
**expiration_date** | **string** | The expiration date of the video in Coordinated Universal Time (UTC). The video’s expiration date is automatically set to 30 days after the video’s initial upload. | [optional] 
**moderation** | [**\Swagger\Client\Model\Moderation**](Moderation.md) |  | [optional] 
**play_lists** | [**\Swagger\Client\Model\Play[]**](Play.md) | The playlist created for the uploaded video, which provides the streaming video URLs to play the video. The supported streaming video protocols are DASH (Dynamic Adaptive Streaming over HTTP) and HLS (HTTP Live Streaming). The playlist will only be generated if a video is successfully uploaded with a status of &lt;code&gt;LIVE&lt;/code&gt;. | [optional] 
**size** | **int** | The size, in bytes, of the video content. | [optional] 
**status** | **string** | The status of the current video resource. For implementation help, refer to &lt;a href&#x3D;&#x27;https://developer.ebay.com/api-docs/commerce/media/types/api:VideoStatusEnum&#x27;&gt;eBay API documentation&lt;/a&gt; | [optional] 
**status_message** | **string** | The &lt;b&gt;statusMessage&lt;/b&gt; field contains additional information on the status. For example, information on why processing might have failed or if the video was blocked. | [optional] 
**thumbnail** | [**\Swagger\Client\Model\Image**](Image.md) |  | [optional] 
**title** | **string** | The title of the video. | [optional] 
**video_id** | **string** | The unique ID of the video. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

