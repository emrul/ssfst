# Subsequential Finite State Transducer
[![Build Status](https://travis-ci.org/deniskyashif/ssfst.svg?branch=master)](https://travis-ci.org/deniskyashif/ssfst)
[![Coverage Status](https://coveralls.io/repos/github/deniskyashif/ssfst/badge.svg?branch=master)](https://coveralls.io/github/deniskyashif/ssfst?branch=master)
[![Code Climate](https://codeclimate.com/github/deniskyashif/ssfst/badges/gpa.svg)](https://codeclimate.com/github/deniskyashif/ssfst)
[![npm](https://img.shields.io/npm/l/express.svg)]()

## Example Usage
```js
const SSFST = require('transducer');

const spellingCorrector = new SSFST([
    { input: 'acheive', output: 'achieve'},
    { input: 'arguement', output: 'argument'},
    { input: 'independant', output: 'independent'},
    { input: 'posession', output: 'possession'},
    { input: 'mercy less', output: 'merciless' }
]);

console.log(spellingCorrector.process('independant').output); // => "independent"
console.log(spellingCorrector.process('mercy less arguement').output); // => "merciless argument"
console.log(spellingCorrector.process('they acheived a lot').output); // => "they achieved a lot"

```

## Requirements
* [git](https://git-scm.com/downloads)
* [nodejs](https://nodejs.org/en/download/current/) v. >= 8.x

## Installation
```
git clone --recursive https://github.com/deniskyashif/ssfst.git ssfst
cd ssfst/src
npm install
```

## Run the Examples
```
npm start
npm run phones // construct the transducer using CMU Phones dictionary
npm run dict  // construct the transducer using CMU dictionary
```

## Run the Tests
```
npm test
```

## Code Coverage
```
npm run cover
```

## References
* ["Efficient Dictionary-Based Text Rewriting using Subsequential Transducers" by S. Mihov, K. Schulz](https://www.researchgate.net/publication/232005152_Efficient_dictionary-based_text_rewriting_using_subsequential_transducers)
* ["Finitely Subsequential Transducers" by C. Allauzen, M. Mohri](https://www.researchgate.net/publication/263878442_FINITELY_SUBSEQUENTIAL_TRANSDUCERS)
