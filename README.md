# biblename-dbgenerator

Generates an sqlite database of names and sentimant of the verses in which they are mentioned in the Bible in json format using NLTK's Vadar library. This makes use of the json formatted bible found here: https://github.com/honza/bibles/blob/master/ESV/ESV.json .

A lot of mistakes are seen in the extract:

1. Plurals and singular variants of the same name are recongized as different names.
2. NLTK detects a lot of words as proper nouns though they are not names. For example, the words: Accordingly, Afterward, Affliction and Against were all detected as nouns. A database of these terms may need to be built so that the code can ignore them.
3. The Vadar library certainly isn't tuned for Bibilical English as some very negative sentences are detected as neutral.
