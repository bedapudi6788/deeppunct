# deepcorrect

Code and checkpoints corresponding to the posts https://medium.com/@praneethbedapudi/deepcorrection-3-spell-correction-and-simple-grammar-correction-d033a52bc11d and https://medium.com/@praneethbedapudi/deepcorrection2-automatic-punctuation-restoration-ac4a837d92d9

Pre-trained models for punctuation correction (trained on google news, wikipedia and tatoeba) are available at https://drive.google.com/open?id=1Yd8cJaqfQkrJMbRVWIWtuyo4obTDYu-e

Demo of the punctuation model trained on google news corpus is available at http://bpraneeth.com/projects/deeppunct

This repo uses a seq2seq model written by me in keras with tensorflow backend. The multi-purpose seq2seq model can be found at https://github.com/bedapudi6788/txt2txt/

Requirements:

Tensorflow Version: 1.4
Keras Version: 2.1.5

Usage:
```
from deepcorrect import DeepCorrect
corrector = DeepCorrect('params_path', 'checkpoint_path')
corrector.correct('hey')
'Hey!'
```

# Installation:

pip install deepcorrect

# Points to Note:

Max input and output lengths are 200

Segment text into sentences using https://github.com/bedapudi6788/deepsegment and run punctuation correction on each sentence seperately.
