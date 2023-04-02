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

![Anime Image](https://e7.pngegg.com/pngimages/645/118/png-clipart-the-testament-of-sister-new-devil-harem-anime-sticker-shinmai-maou-no-testament-cg-artwork-black-hair-thumbnail.png)

### Example response:

```
{
  "error_code": 0,
  "predictions": {
    "artificial-images": 0.97,
    "artificial-images_hentai": 0.79,
    "composition_one_entity": 0.63,
    "composition_one_female": 0.67,
    "unsafe": 0.58
  }
}
```


The nsfw field will be true if NSFW content is detected in the image, and false otherwise. The tags field is an array of tags describing the detected NSFW content.
