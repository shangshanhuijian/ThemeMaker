# ThemeMaker

[CH](https://github.com/exthmui/ThemeMaker/blob/master/README.md) | EN

This tool is used to make themes for `exTHmUI`.

`template` folder is a template for themes.

## License
- Apache Version 2.0

## Requirements
- x86_64 enviroment (Windows Or Linux)
- Python 3
- JRE

## Usage
`make.py <src> <out> [resource packages]`

### Examples
- `./make.py template/ template.apk`
- `./make.py template/ template.apk framework-res.apk SystemUI.apk`

## Note
- Before using, please use the tool named `get_resapk` to get `framework-res.apk`.
- According to the `overlay` that is used in the target theme, you might need to acquire *target apk* into the `resource packages`.
- All files in the `bin` folder come from [Android SDK Build Tools](https://android.googlesource.com/platform/prebuilts/fullsdk/build-tools/)

# Making themes

## How does it work?
exTHmUI theme engine uses methods similar to [Substratum](https://github.com/substratum/), editing the system resources by controlling the overlay.

For fonts and boot animation, exTHmUI uses custom resolving ways.

## Theme template structure
```
/
├── AndroidManifest.xml
├── assets
│   ├── backgrounds           <--- Wallpapers(lockscreen)
│   ├── fonts                 <--- Fonts and font configuration
│   ├── media                 <--- Boot animation(light and dark included)
│   ├── previews              <--- Theme preview
│   └── sounds                <--- Sounds(notification, alarm, etc)
├── overlay                   <--- Overlay
└── res
    ├── drawable
    │   ├── theme_banner      <--- Banner for the theme preview
    │   ├── theme_icon        <--- Theme icons
    │   └── theme_image       <--- Pictures of the configuration page
    ├── values
    │   ├── bools.xml         <--- Part of the configuration
    │   └── strings.xml       <--- Theme name and author
    └── xml
        └── theme_data.xml    <--- Configuration of theme resources
```

## Theme template
Please refer to the `template` folder.

## Signing
If you want to sign your theme,

You just need to replace `testkey.pk8` and `testkey.x509.pem` with your own keys.

You might need to edit `make.py` for signing configurations.

Spring River Flower Moon Night
Zhang Ruyu
The spring river tide is even the sea level, the sea moon tides together.
With thousands of miles, where the spring river no moon!
The river flows around Fangdian, and the moon shines like a forest;
The air flow frost does not feel flying, the white sand on the Ting can not see.
Jiangtian color without fiber dust, the lone moon wheel in the sky.
Who is on the banks of the river seeing the moon for the first time? Jiang Yue who took the picture at the beginning of the year?
Generations of life are endless, jiang yue year after year look similar.
I don't know who the river and moon are for, but see the Yangtze River to send water.
Baiyun a piece to melodious, Green Maple Pu on the endless worry.
Whose house is flat tonight? Where is xiang Siming Moon Building?
Poor building last month back, should be taken away from the makeup mirror.
The jade curtain can't be rolled up, and the mash-up is brushed back.
At this time look at each other do not hear, would like to month-by-month Flow of the king.
Hongyu long flying light is not degrees, fish and dragon dive into the water into writing.
Last night idle pond dream falling flowers, poor spring half do not return home.
The river flow in spring to exhaust, the river pond fall moon re-slope.
The oblique moon sinks into the sea mist, and the yanshi Xiang unlimited road.
I do not know how many people by the moon return, the fall of the moon full of river trees.
