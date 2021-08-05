# Media Organizer

Need an organizer for your media content on the computer? Run this!

## Features

- Organize photos and videos in a folder structure based off creation dates.

  - Photos organized based off of EXIF creation dates.

    - Whitelisted photo file types. ("jpeg", "jpg", "JPEG", "JPG", "HEIC", "heic", "PNG", "png")

  - Video organized based off of FFMPEG creation dates.

    - Whitelisted video file types. ("mp4", "MP4", "mov", "MOV")

  - User provides target folder of unorganized images. Will move photos to a default `photos` directory in the directory where the binary was ran. The outputed folders will be the respective creation dates on the media.

- Allow configurable destination folder.

  - Use the `--dest` flag.

## Dependencies

- C++ build tools (or equivalent like build-essentials) (for ffmpeg-next package)
- FFMPEG

## CLI usage

To quickly organize photos in the target folder, run the following command to output them into the default destination directory.

```bash
photo_organizer --target test-media
```

To add a destination folder for all the organized photos, add the `--dest <DEST_FOLDER>` flag to the end.

While developing with cargo, forward the flags.

```bash
cargo run -- --target test-photos
```

## Future development

- Make a multi-media organizer binary.
- Organize single file entry through cli.
- through CLI organize specific media files.
- Organize audio files? https://github.com/pdeljanov/Symphonia
- Export web assembly binary to use in JS/Node/Electron.

  - Watch out for `DEST_FOLDER` environment variable.

- Option to index photos.
- Option to compress image sizes.
