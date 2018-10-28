# AnkiDeckGenerator

Convert a list of Chinese characters/words/sentences and/or English words/sentences into an extremely powerful Anki Deck Package (apkg).

# Screenshots
![gif-video](screenshots/screen-recording.gif)

## TODO
- [ ] Make popup work on Windows
- [x] Make popup work on Linux
- [x] Make popup work on Android
- [x] Accept individual Chinese characters as input
- [x] Accept Chinese words consisting of multiple characters as input
- [x] Accept Chinese sentences consisting of multiple character as input
- [x] Create a highly dynamic and configurable input file format
- [ ] Fill missing data (hanzi, pinyin, audio) when only specifying English words/sentences as input
- [x] Generate Anki card data for the Hanzi
- [x] Generate Anki card data for the English translation
- [x] Generate Anki card data for example words that contain a given cards Hanzi
- [x] Generate Anki card data for the english translation of the example words
- [x] Generate Anki card data for example sentences that contain a given cards Hanzi
- [x] Generate Anki card data for the english translation of the example sentences
- [x] Add multiple audio files for the pronunciation of the used Hanzi for every context
- [x] Generate Anki card data for the Pinyin
- [x] Generate Anki card data for the Hanzi decomposition
- [x] Generate Anki card data for the Hanzi type (ideographic/pictographic/pictophonetic)
- [x] Generate Anki card data for the Hanzi formation in case of ideographic/pictographic
- [x] Generate Anki card data for the semantic/phonetic Hanzi etymology in case of pictophonetic
- [x] Generate Anki card data for the primary radical of the Hanzi
- [x] Generate Anki card data for the charCode as used in JavaScript
- [x] Create a Stroke order diagram generator that outputs still images with numbers
- [x] and create a Pull Request at https://github.com/skishore/makemeahanzi adding this generator script and the generated stroke diagrams
- [x] Generate Anki card data for the charCode as used in JavaScript
- [x] Copy the Hanzi stroke order diagrams into the deck output
- [x] Write a bootstrap based Anki card template that uses all the features mentioned above
- [x] Allow specifiying an output dir for the generated files
- [x] Write Anki card data in Anki compatible tsv format as output
- [ ] Document all features
- [ ] Clean up for initial release
- [ ] Add screenshots

## Requirements
- git
- nodejs (at least v10)

## Installation
```
git clone --recursive https://github.com/FOSS-Chinese/AnkiDeckGenerator.git
cd AnkiDeckGenerator
npm i
cd submodules/makemeahanzi/stroke_caps
node generateStillSvgs.js
```

## Example Usage
```
node index.js auto-generate MyNewDeck.apkg -c example-input.txt -n MyNewDeck -d MyDeckDescription
```
Or just run `npm run example`.

## Usage
```
Usage: index [options]

Options:

  -V, --version                         output the version number
  -c, --input-file-chinese <file-path>  File containing a json-array of Chinese characters, words and/or sentences
  -o, --output-folder <folder-path>     Folder in which the deck files will be written

  -h, --help                            output usage information
```
