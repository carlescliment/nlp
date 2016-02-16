## Exercises

#### Chapter 1

17)
```
text9[621:644]
```

18)
```
>>> all_words = []
>>> for sent in [sent1, sent2, sent3, sent4, sent5, sent6, sent7, sent8]:
...   all_words += [word for word in sent if word.isalpha()]
... 
>>> sorted(set(all_words))
```

19)
The first sentence brings the complete vocabulary sorted and in lowercase. The second does the same, but those words appearing both with upper and lowercased letters will show up twice. Thus, the second can be longer.

20)
`w.isupper()` is true if all the chars are uppercased, while `not w.islower()` is true if any of the letters is uppercased.

21)
```
text2[-2:]
```

22)
```
[word for word, times in FreqDist([word for word in text5 if len(word) == 4]).most_common()]
```

23)
```
>>> for word in text6:
...   if word.isupper():
...     print word
```

24)
```
[word for word in text6 if word.endswith('ize')]
[word for word in text6 if 'z' in word]
[word for word in text6 if 'pt' in word]
[word for word in text6 if word.isalpha() and word == word.capitalize()]

25)
```
>>> for printable in [word for word in sent if word.startswith('sh')]:
...   print printable

```

26)

Brings the count of letters plus punctuation in a text. We can't use it to work out the average word length, since it includes punctuation. But we could substract the total count of punctuation chars to calculate the average.

27)
```
>>> def vocab_size(text):
...   return len(set(text))
```

28)
```
>>> from __future__ import division
>>> def percent(word, text):
...   text_length = len([w for w in text if w.isalpha()])
...   appeareances = FreqDist(text)[word]
...   return appeareances*100 / text_length
```

29)

`set(sent3) < set(text1)` means that the words in `sent3` are a subset of the words in `text1`. We could for instance find out if a text is written in a given language.

