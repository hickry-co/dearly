# Dearly

**A cozy scrapbook journal for iPhone.** Every day gets its own page. Decorate it with stickers, washi tape, photos, places and moods, then keep it all in a notebook that looks and feels like yours.

Made with love, by [hickry.co](https://hickry.co). Istanbul, 2026.

## Features

**Decorate every day**
- One page per day with a desk-style scrapbook look and a taped date label
- Stickers: emoji, doodles, pins and clips, cut-out ransom-note letters, numbers and punctuation in many paper styles
- Cut your own stickers out of any photo (Vision foreground cut-out)
- Washi tapes, clips, clothespins, thumbtacks, brads, manila tags, sticky notes
- Polaroid photos and videos with handwritten captions
- Text in several fonts, with any colour (swatches or a custom picker)
- Page backgrounds: paper, dots, grid, lines, kraft, or your own photo

**Arrange with ease**
- Drag, pinch, rotate and resize with visible handles
- Rotation snaps at 45 and 90 degrees with guide lines and a light haptic tap
- Layer order: to front, forward, backward, to back
- Groups: move, rotate and scale items together; add or remove members; ungroup; duplicate
- Favorites: keep stickers and whole groups and reuse them on any day

**Mood and places**
- Mood heart on a liquid-glass slider (iOS 26 glass, material fallback before that)
- One or several places on an airmail postcard map, nearest results first
- Mood and place stickers can be moved, resized and rotated like any other item

**Notebooks**
- Grid or stacked-deck view
- Leather, craft-paper and chipboard covers, or design a cover from your own stickers
- Elastic band, satin ribbon, striped, stitched, cord and twine (red/blue, red/white, green/white, jute, gold)
- Vertical or horizontal band, up to three charms in gold, brass or silver
- Short texts pressed, foil-stamped or inked into the cover (nine positions)
- Password and Face ID / Touch ID locks per journal

**Look back**
- Calendar of stamps or moods, statistics
- Home Screen widgets: streak (small, medium) and a large calendar (stamps or moods)
- Deleted Records, JSON backup export / import, optional iCloud sync
- English and Turkish

## Tech

- SwiftUI and SwiftData, iOS 17+ (Liquid Glass is used where available)
- Observation, PhotosUI, MapKit and CoreLocation, Vision, LocalAuthentication
- WidgetKit and App Intents, shared data through the App Group group.co.hickry.dearly
- XcodeGen: project.yml generates the Xcode project

## Build

Requirements: Xcode 16 or newer (Xcode 26 adds the Liquid Glass look), XcodeGen (brew install xcodegen).

~~~
xcodegen generate
open Dearly.xcodeproj
~~~

Then, for both targets (Dearly and DearlyWidgets), pick your Team under Signing & Capabilities. The App Group and iCloud capabilities need a paid developer account. Run Clean Build Folder after adding or removing source files.

## Project layout

~~~
Dearly/            app: models, services, views (Home, Journal, Stickers, Profile)
DearlyWidgets/     widget extension
Shared/            code shared by the app and the widgets (mood, stamps, snapshots)
project.yml        XcodeGen project definition
~~~

## Privacy

Journals live on your device. iCloud sync is optional and off by default. Dearly has no accounts, no ads and no analytics. Location is used only when you add a place to a page.

## License

All rights reserved, hickry.co.
