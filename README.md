# Assem's Arabic Stemmer [![Gitter](https://badges.gitter.im/arabicstemmer/Lobby.svg)](https://gitter.im/arabicstemmer/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

This is an algorithm for Arabic stemming written on Snowball framework language. If offers light stemming and text normalization. voc


## Requirements:

- [Snowball framework](https://github.com/snowballstem/snowball)
- [Snowball-data](https://github.com/snowballstem/snowball-data)
- [Golden-Arabic-Corpus](https://github.com/LBenzahia/golden-corpus-arabic/archive/master.zip)
- [NLTK](http://www.nltk.org/)
- [mkdocs](http://www.mkdocs.org/)

- You can download it automatically using:
```sh
    $ make download
```

- Install python requirements
```sh
    $ sudo pip install -r requirements.txt
```
or manually by:

- extracting snowball into the root folder `{Root}/snowball`
- extracting snowball-data/arabic/voc.txt.gz into `{Root}/test_data/voc.txt`

## Build:

- light stemming
```sh
      $ make build
```
- root-based stemming
```sh
      $ make build_root_based_stemmer
```

## Run:

- Light Stemmer
```sh
  	 $ make run
  	  الطالب
  	  طالب
```
- Root-Based Stemmer
```sh    
      $ make run_root
      الطالب
      طلب
```

## Test:
We configured tests to run against snowball-data arabic sample.

- time:
```sh
      $ make time
```

- grouping effect:
```sh
      $ make grouping
```
- all:
```sh
      $ make test
```
- Test SAS with golden arabic corpus:
```sh
      $ make test_arabicstemmer
```
- Test ISRI Stemmer with golden arabic corpus:
```sh
     $ make test_isri
```
## Distributions:

- dist light stemmer to available languages:
```sh
    $ make dist
```
- dist root-based stemmer to available languages:
```sh
    $ make dist_rooter
```


## Results:
Snowball Arabic (Stemmer & rooter) Results

Word | Stem | root
------------ | ------------- | ------------
طفل | طفل  | طفل
اطفال | اطفال  | طفل
الاطفال | اطفال  | طفل
اطفالكم | اطفال  | طفل
فأطفالكم | اطفال  | طفل
اطفالهم | اطفال  | طفل
والاطفال | اطفال| طفل
فاطفالهم | اطفال  | طفل
وطفل | طفل  | طفل
الطفولة | طفول  | طفل
  والطفلتين | طفل |طفل
طفلتان | طفل | طفل
