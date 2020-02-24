# Screen reader multilanguage experiment

Just a little experiment on how screen readers handle working in multiple languages on the web (for example, when the OS or screen reader UI is in one language, but the website is in another).

## TL;DR

All screen readers have major issues, and no screen reader and browser combination provided even a passable experience. The most common and troublesome issue is that the `alt` attribute of informative images is read in the wrong language or, in some cases, not read at all.

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
    - For all other: the text content is announced in an English voice
  - 1: The language and/or voice used are correct, but there's some small issue, such as additional content, additional elements with no content, etc.
  - 0: Incorrect announcement.
    - For element descriptions: the language and voice don't match, or they are mixed
    - For decorative image: the element is not skipped completely
    - For all other: the text content is announced in the wrong voice.
  - -1: An element is skipped when it shouldn't, or the combination of screen reader and browser just doesn't work

- I did some analysis. Check out [the Google spreadsheet](https://docs.google.com/spreadsheets/d/1UDNJCGyYOdQPOof5yYwxzfnuhoUbblhwi_tgZR_N0I0/), on the "Analysis" tab. Some highlights:
  - All combinations had major issues that severely impact users, but the issues vary wildly.
  - Overall, the elements with the most language troubles were informative images (with an `alt` attribute, with or without an explicit `lang` attribute).
    - They received an average score of 0.71 (without explicit `lang`) and 0.67 (with explicit `lang`) out of 2.
    - They were announced acceptably (score of 2 or 1) 44% of the time, and unacceptably (score of 0 or -1) 56% of the time.
  - The page title was also quite troublesome, but this is a minor problem by comparison, since it only comes up once (at the beginning of the page), and the same information can usually be found elsewhere, such as the top-level heading).
  - By overall screen reader score: JAWS performed the best, VoiceOver (mobile) performed the worst.
  - By overall browser score: Opera and Chrome performed the best, Firefox performed the worst.
  - By screen reader and browser combination: TalkBalk with Opera performed the best, followed by JAWS with either Chrome, Firefox, or Opera. VoiceOver with Firefox perfomed the worst (it didn't work at all), followed by TalkBack with Firefox.

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
