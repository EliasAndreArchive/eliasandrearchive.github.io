# Adding media

## 1. Upload the file

Open Cloudflare Dashboard, then go to:

`Storage & databases` → `R2 Object Storage` → `elias-andre-media` → `Objects`

Open the matching collection folder or create one, then choose **Upload**. Current folders include `ireland/`, `croatia/`, `fields/`, and `concerts/`.

Use web-ready H.264 MP4 files for video and WebP or JPEG files for photos.

## 2. Add its JSON entry

Edit `media.json` and add an object inside the `items` array:

```json
{
  "file": "analog/my-new-video.mp4",
  "category": "analog",
  "label": "A summer memory",
  "text": "Filmed in Berlin in summer 2026.",
  "size": "md"
}
```

The category selector is generated automatically from the category names used in this file. Home always remains the first collection and displays a balanced random selection of 15 videos from the other collections.

Available sizes are `sm`, `md`, and `lg`. The site detects video or photo from the file extension. You can override that by adding `"type": "video"` or `"type": "photo"`.

The `file` value is the object's complete path inside the R2 bucket. It does not need to match the category, although keeping each collection in a matching folder makes the archive easier to manage.

## 3. Publish the metadata change

Commit and push `media.json` to the GitHub Pages repository. The video itself stays in R2; only its metadata is stored in GitHub.
