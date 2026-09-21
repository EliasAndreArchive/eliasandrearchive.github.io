# Adding media

## 1. Upload the file

Open Cloudflare Dashboard, then go to:

`Storage & databases` → `R2 Object Storage` → `elias-andre-media` → `Objects`

Open an existing folder or create one, then choose **Upload**. Recommended folders:

- `cinematic/` for cinematic video files
- `analog/` for analog video files
- `photography/` for photographs

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

The category selector is generated automatically from the category names used in this file. The first category in `media.json` is the collection shown when the page opens.

Available sizes are `sm`, `md`, and `lg`. The site detects video or photo from the file extension. You can override that by adding `"type": "video"` or `"type": "photo"`.

The `file` value is the object's complete path inside the R2 bucket. It does not need to match the category. For example, the current Home collection uses files stored in the `cinematic/` folder.

## 3. Publish the metadata change

Commit and push `media.json` to the GitHub Pages repository. The video itself stays in R2; only its metadata is stored in GitHub.
