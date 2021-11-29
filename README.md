# Wobfuscator: JS To WebAssembly Transformation Obfuscator

This repo contains the data from our submission titled "Wobfuscator: Obfuscating JavaScript Malware via Opportunistic Translation to WebAssembly". 

## Datasets
The detectors we compare against in our paper ([Cujo](https://github.com/Aurore54F/lexical-jsdetector), [Zozzle](https://github.com/Aurore54F/syntactic-jsdetector), [JaSt](https://github.com/Aurore54F/JaSt), and [JStap](https://github.com/Aurore54F/JStap)) are trained against a set of benign and malicious samples. Our benign samples come from the [150k Javascript Dataset]([https://www.sri.inf.ethz.ch/js150) dataset made public by ETH Zürich. The malicious samples come from three datasets. Two datasets are made available: the [Javascript Malware Collection by HynekPetrak](https://github.com/HynekPetrak/javascript-malware-collection) and the [Malicious Javascript Dataset by GeeksOnSecurity](https://github.com/geeksonsecurity/js-malicious-dataset). The third dataset is provided by VirusTotal. This dataset can be obtained by [requesting it from them](https://www.virustotal.com/gui/contact-us/).

## Data
We provide the detection results obtained by applying different combinations of our transformation rules against each of the detection tools described in the paper. The results are in the `Data` directory in CSV and Excel format.

## Projects
In our correctness validation and efficiency measurement, we use the following npm modules:
- [Lodash](https://github.com/lodash/lodash)
- [Chalk](https://github.com/chalk/chalk)
- [Commander.js](https://github.com/tj/commander.js)
- [Debug](https://github.com/visionmedia/debug)
- [Async](https://github.com/caolan/async)
- [Node-Fetch](https://github.com/node-fetch/node-fetch)

We provide these packages with the translations applied under the `Projects` directory. These packages have had the library files (and test files for node-fetch) transformed using all of the transformation rules. The following directories of each project are where the library files are located (and where our transformations are applied):
- Lodash: `.internal`
- Chalk: `source`
- Commander.js: `index.js`
- Debug: `src`
- Async: `lib/internal`
- Node-Fetch: `src`, `test`

For each of these locations, we also provide the original, unobfuscated library files in directories with `_original` appended to the names above, e.g. `.internal_original` for lodash.
