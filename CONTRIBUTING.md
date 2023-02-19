# Contributing guide

The purpose of this guide is to ensure
that all files are committed according to the agreed standards
to improve the repository's performance and accessibility.

By following this guide, we can ensure that
the repository remains fast and accessible for everyone,
and that we are making the most efficient use of our storage space.

## Avatars

When possible, use textures with the high compression (such as JPEG).

## Images

Before committing images to the repository, follow these steps:

- Compress all images using the image compression tool.
- Verify that the compressed images are of acceptable quality.
- Commit the compressed images to the repository.

If you would like to know more information about your image, run:

    identify -verbose someimagefile

### Compression

Use an image compression tool to optimize all images before committing them to the repository.
Continuously strive to improve the image compression process and make it more efficient.
For example, you can start with a medium compression level and adjust as needed.

Here are few examples:

     jpegoptim --all-progressive -m60 *.jpg
     pngquant --force --quality=40-100 --skip-if-larger --verbose file.png --output file.png

## Optimal format

Optimal file format for images depends on the type of image.
In general JPEG format is best for photographs
and PNG format is best for graphics and logos with transparent backgrounds.

To convert from one format to another, use ImageMagick's `convert` command:

    convert file.png file.jpg
    convert file.jpg file.jp2

### Size

Find the right balance between image quality and file size by experimenting with different compression levels.
When the images dimensions are too big, use tools to resize it.

Example using ImageMagick command-line tools:

    convert file.jpg -scale 50% file.jpg

Exceptions:
If an image needs to be kept at its original size and quality,
include a clear justification in the commit message explaining
why the image could not be compressed.

## Large files

Ensure all large binary files are send to Git LFS (Large File Storage).
Most of the image files are already convered in `.gitattributes`.

## Unity

### Scene

The scene is used and included from the main Ecilos project,
so please don't add any extra objects into Avatars scene.
