# Screen reader multilanguage experiment

Just a little experiment on how screen readers handle languages.

## Setup

I made a website with the following elements:

1. A top-level heading (`<h1>`)
2. A paragraph (`<p>`)
3. An ordered list (`<ol>`) with two items (`<li>`)
4. An informative image (`<img>`) with an `alt` attribute
5. A decorative image (`<img>`) with an empty `alt` attribute
6. A button (`<button>`) with visible text

And I performed tests...

...using 4 major screen readers (VoiceOver, NVDA, JAWS, TalkBack)

...on 5 major browsers (Safari, Chrome, Firefox, Opera / Opera Touch, Edge)

...on desktop and mobile

...in 2 modes (continous reading, and using keyboard or swiping shortcuts to move the reading cursor)

## Results

Coming soon.

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
