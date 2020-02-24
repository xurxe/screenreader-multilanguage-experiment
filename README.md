# Screen reader multilanguage experiment

Just a little experiment on how screen readers handle languages.

## Setup

I made a website with the following elements:

1. A top-level heading (`<h1>`)
2. A paragraph (`<p>`)
3. An ordered list (`<ol>`) with two items (`<li>`)
4. An informative image (`<img>`) with an `alt` attribute'
5. An informative image (`<img>`) with an `alt` attribute and an explict `lang` attribute
6. A decorative image (`<img>`) with an empty `alt` attribute
7. A button (`<button>`) with visible text
8. A portion of text (`<span>`)in a different language, with an explict `lang` attribute

And I performed tests...

...using 4 major screen readers (VoiceOver, NVDA, JAWS, TalkBack)

...on 5 major browsers (Safari, Chrome, Firefox, Opera / Opera Touch, Edge)

...on desktop and mobile

...in 2 modes (continous reading, and using keyboard or swiping shortcuts to move the reading cursor)

## Results

- For each test case, I recorded the following (check out [data.md](data.md) for more details):

  - In what language or voice the screen reader announces the type of content (screen readers tell you if the content is a heading, an image, etc.)
  - In what voice the screen reader announces text content itself.

- I gave scores for each test case. Check out [the Google spreadsheet](https://docs.google.com/spreadsheets/d/1UDNJCGyYOdQPOof5yYwxzfnuhoUbblhwi_tgZR_N0I0/), on the "Scores" tab:
  - 2: Perfect announcement.
    - For element descriptions: the language and voice match (either both in Finnish or both in English)
    - For decorative image: the element is skipped completely
    - For portion in Spanish: the text is announced in a Spanish voice
    - For all other: the text content is announced in a Finnish voice
  - 1: The language and/or voice used are correct, but there's some small issue, such as additional content, additional elements with no content, etc.
  - 0: Incorrect announcement.
    - For element descriptions: the language and voice don't match, or they are mixed
    - For decorative image: the element is not skipped completely
    - For all other: the text content is announced in the wrong voice.
  - -1: An element is skipped when it shouldn't.

## Testing site

[Check it out on GitHub pages](https://xurxe.github.io/screenreader-multilanguage-experiment/)!

## Testing environment

- Website language: English
- OS language: Finnish
- VoiceOver (desktop):

  - Device: MacBook Pro (16-inch, 2019)
  - macOS version: 10.15.2
  - VoiceOver: included with macOS
  - Safari version: 13.0.4
  - Chrome version: 79.0.3945.130
  - Firefox version: 72.0.2
  - Opera version: 66.0.3515.72
  - Edge version: 80.0.361.48

- VoiceOver (mobile):

  - Device: iPhone 11
  - iOS version: 13.3
  - VoiceOver: included with iOS
  - Safari version: 13.0
  - Chrome version: 79.0.3945.73
  - Firefox version: 20.2 (16690)
  - Opera Touch version: 2.0.4
  - Edge version: 44.10.13

- NVDA

  - Device: Asus X540LA
  - Windows version: 10 Home 18362.418
  - NVDA version: 2019.3.1
  - Safari version: N/A (not maintained)
  - Chrome version: 80.0.3987.87
  - Firefox version: 72.0.2
  - Opera version: 66.0.3515.72
  - Edge version: 80.0.361.50

- JAWS

  - Device: Asus X540LA
  - Windows version: 10 Home 18362.418
  - JAWS version: 2019.1912.9 Multilingual
  - JAWS with "Language Detect Change" selected
  - Safari version: N/A (not maintained)
  - Chrome version: 80.0.3987.87
  - Firefox version: 72.0.2
  - Opera version: 66.0.3515.72
  - Edge version: 80.0.361.50

- TalkBack

  - Device: Samsung Galaxy S8+
  - OS: Android 9 Build/PPR1.180610.011
  - TalkBack version: 8.1.0.278818032
  - Safari version: N/A (not maintained)
  - Chrome version: 80.0.3987.99
  - Firefox version: 68.5.0
  - Opera Touch version: 2.3.0
  - Edge version: 44.11.4.4140

## Author

Xurxe Toivo García

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
