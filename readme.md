# cuss [![Build Status][travis-badge]][travis]

Map of profanities to sureness rating.
This rating _does not_ represent _how_ vulgar a term is, instead, how
likely it is to be used as either profanity or clean text.

## Installation

[npm][]:

```bash
npm install cuss
```

## Usage

```js
var cuss = require('cuss')

console.log(Object.keys(cuss).length) // 1773

console.log(cuss.beaver) // 0
console.log(cuss.asshat) // 2
```

### Usage of locale versions

_To use the Portuguese from Brazil by example_

```js
var cuss = require('cuss/pt-br')

console.log(Object.keys(cuss).length) // 148

console.log(cuss.burro) // 1
console.log(cuss.bixa) // 2
```

## API

### `cuss`

**Type**: `Object.<number>` — **cuss** exposes a dictionary
of phrases to ratings, where each key can be considered a profanity,
and each rating is a number between `0` and `2` (both including),
representing the certainty the key is used as a profanity depending
on context.

| Rating | Use as a profanity | Use in clean text | Example |
| ------ | ------------------ | ----------------- | ------- |
| 2      | likely             | unlikely          | asshat  |
| 1      | maybe              | maybe             | addict  |
| 0      | unlikely           | likely            | beaver  |

## Support

*   [`index.json`](index.json) — ± 1770 English profane words and phrases from
    [Luis von Ahn’s Research Group (Carnegie Mellon)][luis-von-ahn], the
    [`List of ethnic slurs` from WikiPedia][racial-slurs], and other many more
    since)
*   [`ar-latn.json`](ar-latn.json) — ± 250 Arabic (Latin-Script) profane words
    and phrases from [`naughty-words`][ar-source-naughty-words] and
    [`youswear`][ar-source-youswear]
*   [`es.json`](es.json) — ± 650 Spanish profane words and phrases from
    [`naughty-words`][es-source-naughty-words],
    [`revistagq.com`][es-source-revistagq], [`taringa.net`][es-source-taringa],
    [`mundoxat.om`][es-source-mundoxat]
*   [`fr.json`](fr.json) — ± 740 French profane words and phrases from
    [`wiktionary.org`][fr-source]
*   [`pt-br.json`](pt-br.json) — ± 148 Brazilian Portuguese profane words from
    [`aprenderpalavras.com`][pt-br-source]

## Related

*   [buzzwords](https://github.com/words/buzzwords)
    — List of buzzwords
*   [dale-chall](https://github.com/words/dale-chall)
    — List of familiar American-English words (1995)
*   [fillers](https://github.com/words/fillers)
    — List of filler words
*   [hedges](https://github.com/words/hedges)
    — List of hedge words
*   [profanities][]
    — List of the same profane words, but without the sureness
*   [spache](https://github.com/words/spache)
    — List of simple American-English words (1974)
*   [weasels](https://github.com/words/weasels)
    — List of weasel words

## Contributing

Thanks, contributions are greatly appreciated!  :+1:

New terms can be added to the corresponding JSON file as listed in the support
section.

To add a new language, create a new JSON file using a lowercased preferred
BCP-47 tag (feel free to ask for help if you’re not sure).

After adding a word, run `npm install` to install all required dependencies,
then `npm test` to update: the project includes some scripts to make sure
everything is in order.
Finally, open a Pull Request.

## License

[MIT][license] © [Titus Wormer][author]

<!-- Definitions -->

[travis-badge]: https://img.shields.io/travis/words/cuss.svg

[travis]: https://travis-ci.org/words/cuss

[npm]: https://docs.npmjs.com/cli/install

[license]: license

[author]: http://wooorm.com

[profanities]: https://github.com/words/profanities

[fr-source]: https://fr.wiktionary.org/wiki/Cat%C3%A9gorie:Insultes_en_fran%C3%A7ais

[ar-source-naughty-words]: https://github.com/LDNOOBW/List-of-Dirty-Naughty-Obscene-and-Otherwise-Bad-Words/blob/master/ar

[ar-source-youswear]: http://www.youswear.com/index.asp?language=Arabic

[es-source-taringa]: https://www.taringa.net/posts/info/7253513/Listado-de-vulgarismos-y-malas-palabras-en-espanol.htm

[es-source-mundoxat]: https://www.mundoxat.com/foro/showthread.php?301-Lista-de-palabras-MALAS-Necesito-AYUDA%21

[es-source-naughty-words]: https://github.com/LDNOOBW/List-of-Dirty-Naughty-Obscene-and-Otherwise-Bad-Words/blob/master/es

[es-source-revistagq]: https://www.revistagq.com/la-buena-vida/articulos/221-insultos-en-castellano-que-deberias-saber/19728

[pt-br-source]: https://aprenderpalavras.com/lista-de-palavroes-xingamentos-e-girias/

[luis-von-ahn]: http://www.cs.cmu.edu/~biglou/resources/

[racial-slurs]: https://en.wikipedia.org/wiki/List_of_ethnic_slurs
