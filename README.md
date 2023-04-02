# unsafe-fake-image-classifier

**Note: Please be assured that the images you send to the our API are not saved or stored in any way. The API only processes the images to identify NSFW content and returns the results to you. Therefore, it is safe to use this API with your sensitive or confidential images.**


This is an API for identifying NSFW (Not Safe For Work) content in images. The API uses machine learning algorithms to detect the presence of adult content, including nudity, sexual activity, and other explicit content.

To obtain a free API key, please send a request to contactus@skymel.com

## Features

* Identifies NSFW content in images
* Supports multiple tags, including "artificial-images" and "violence"
* Fast and accurate detection
* Easy to integrate into your application


## Usage

To use the API, simply send a POST request to the endpoint https://modelpubsub.com/api-v1.0/SafeUnsafeImageWithTags  with the image file attached in the request body. The response will contain a JSON object with the results of the NSFW detection.

**Please note that the latency of the API may vary depending on the size and complexity of the image being processed. Additionally, the latency for the free version of the API may be higher than the paid versions.**

### Example image:

![Trump fake arrest](https://pbs.twimg.com/card_img/1640755770156253185/CIStxnVY?format=jpg&name=900x900)

### Example response:

```
{
  "error_code": 0,
  "predictions": {
    "artificial-images": 0.72,
    "body-parts_head_lips-mouth": 0.57,
    "safe": 1.0
  }
}
```


The nsfw field will be true if NSFW content is detected in the image, and false otherwise. The tags field is an array of tags describing the detected NSFW content.
