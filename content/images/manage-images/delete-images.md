---
pcx_content_type: how-to
title: Delete images
weight: 17
---

# Delete images

You can delete an image from the Cloudflare Images storage using the dashboard or the API.

## Delete images via the Cloudflare dashboard

1. Log in to the [Cloudflare dashboard](https://dash.cloudflare.com/login) and select your account.
2. Select **Images**.
3. Find the image you want to remove and select **Delete**.
4. (Optional) To delete more than one image, select the checkbox next to the images you want to delete and then **Delete selected**.

Your image will be deleted from your account.

## Delete images via the API

Make a `DELETE` request to the [delete image endpoint](/api/operations/cloudflare-images-delete-image). `<IMAGE_ID>` must be fully URL encoded in the API call URL.

```bash
curl -X DELETE https://api.cloudflare.com/client/v4/accounts/<ACCOUNT_ID>/images/v1/<IMAGE_ID> \
--header 'Authorization: Bearer <API_TOKEN>'
```

After the image has been deleted, the response returns `"success": true`.