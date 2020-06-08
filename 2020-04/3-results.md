# Results

## Scoring

I gave scores for each test case. Check out [the Google Sheet's Scores tab](https://docs.google.com/spreadsheets/d/1pzFHgOq6djG-131ogKMdjjQIvWj0NunMrV0_Phs9jas/edit#gid=0):

- 3: Perfect announcement.
  - For element descriptions: the language and voice match (either both in Finnish or both in English)
  - For decorative image with empty `alt`: the element is skipped completely
  - For portion in Spanish: the text is announced in a Spanish voice
  - For all others: the text content is announced in an English voice
- 2: Acceptable announcement.
  - Like perfect announcement, but there's some small issue, such as additional content, additional elements with no content, etc.
- 1: Bad announcement.
  - For element descriptions: the language and voice don't match, or they are mixed
  - For decorative image: the element is not skipped completely
  - For all other: the text content is announced in the wrong voice.
- 0: Terrible announcement.
  - An element is skipped when it shouldn't, or the combination of screen reader and browser just doesn't work

## Analysis

I did some analysis. Check out [the Google sheet's Analysis tab](https://docs.google.com/spreadsheets/d/1pzFHgOq6djG-131ogKMdjjQIvWj0NunMrV0_Phs9jas/edit#gid=1084790845):

- All combinations had major issues that severely impact users, but the issues varied wildly.
- The element with most language trouble (average score: 1.23 out of 3) was the page title. This is a relatively minor problem, because it's often only heard once, and it usually matches the top-level heading of the page.
- The second most significant problem occurred in informative images with an `alt` text. Whether the image had an explicit `lang` attribute made no difference.
  - They received an average score of 1.52 out of 3.
  - They were only announced perfectly in 25% of the test cases.
  - They were announced badly (score 1) or terribly (score 0) 68% of the time.
- In contrast, decorative images with an empty `alt` had the least issues. This is not surprising, given that the correct screen reader behavior in this test case is to skip the element completely; still, some test cases did not achieve this.
- By screen reader:
  - NVDA had the highest score.
  - VoiceOver (mobile) had the lowest score, because it doesn't automatically switch languages.
- By browser:
  - Chrome had the highest score.
  - Firefox had the lowest score.
- By screen reader and browser combination:
  - The most successful combination was NVDA + Firefox. This is interesting, considering that Firefox performed the worst with all other screen readers.
  - JAWS performed the best, and equally well, with Chrome and Opera.
  - TalkBack performed the best, and equally well, with Chrome and Edg
  - VoiceOver (mobile) had the exact same behavior in all cases.
  - VoiceOver (desktop) performed the best, and equally well, with Safari, Chrome, and Edge. This is interesting, since I've heard often that VoiceOver is most suited to work with Safari.
