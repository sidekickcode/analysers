# Analysers

Listing of all analysers that can be used by Sidekick - if you've written one please make a PR!

### The format of additions to the analyser list should be as follows:

```
  "[analyser name goes here]": {
    "registry": "[registry name goes here]",
    "config" : [analyser config in JSON format goes here]
  }
```

 - where `analyser name` needs to be unique in our list of analysers. If you are wrapping an open source project, then its probably good to reference the underlying project in the name, e.g. sidekick-eslint (uses the eslint project).
 - where `registry name` needs to be a publically available registry such as `npm`.
 - where `analyer config` is the contents of your analyser's `config.json` file. 

Check out our guide to writing your own analysers [here](https://github.com/sidekickcode/sidekick-analyser).
  
e.g.
  
```
  "sidekick-eslint": {
    "registry": "npm",
    "config" : {
      "analyser": "eslint",
      "version": "0.0.1",
      "interpreter": "node",
      "script": "eslint.js",
      "scope": "blob",
      "category": "object",
      "tagger": false,
      "configurable": true,
      "configFiles": [
         ".eslintrc"
      ],
      "shortName": "eslint",
      "displayColor": "purple",
      "language": "js",
      "displayName": "Code issues (eslint)",
      "displayCategory": "quality",
      "shortDescription": "Checks your code for quality issues.",
      "underlyingAnalyser": {
       "name": "eslint",
       "url" : "https://github.com/eslint/eslint"
      }
    }
  }
```  
  
  
