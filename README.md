# Create a interactive 360-degree photo for Google Maps

yes, this is possible without a prefessional 360 camera.

## Use an APP on your phone 
I like this free [APP](https://apps.apple.com/us/app/360-photo-cam/id6470239030)

## Add GPANO metadata 
With [exiftool](https://exiftool.org/), add tag [-XMP-GPano](https://stackoverflow.com/questions/44405720/how-to-add-mandatory-google-photo-sphere-xmp-metadata-to-an-equirectangular360).

To Meet the requirement of 360 photos on Google Maps, the minimal pixels are 3840*1920.

```
cd /c/exiftool-13.07_64
./exiftool.exe \
-XMP-GPano:UsePanoramaViewer=True \
-XMP-GPano:ProjectionType=equirectangular \
-XMP-GPano:FullPanoWidthPixels=3840 \
-XMP-GPano:FullPanoHeightPixels=1920 \
-XMP-GPano:CroppedAreaLeftPixels=0 \
-XMP-GPano:CroppedAreaTopPixels=0 \
-XMP-GPano:CroppedAreaImageWidthPixels=3840 \
-XMP-GPano:CroppedAreaImageHeightPixels=1920 \
IMG_2653.JPG
```

Upload your photo on Google Maps, for [example](https://maps.app.goo.gl/wStYu4SGfLbsmMB98).