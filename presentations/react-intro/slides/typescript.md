##  TypeScript

* Supported by **any** environment that already supports **JavaScript**
* **Strongly Typed** *superset* of **JavaScript**
    * *Compile time* **validation**
    * *Project wide* **refactoring**
    * Support for **modern** programming constructs (generics, lambda's, etc...)
* **Seamless** integration with **ALL** existing **JavaScript** libraries
    * Simply download or create a typings definition file

---

#### Full JavaScript Compatibility

* Superset of **JavaScript** means all **JavaScript** is valid **TypeScript**
    * **Mix-and-match** **TypeScript** and **JavaScript** together in the samem file
* **TypeScript** can be *transpiled* into **ECMAScript 3** (**IE6** support even!)
    * Reduced support for language features when targeting **ES3**
    * All language features supported when targetting **ES5** or higher
* Typing and refactoring support for most major IDE's (Visual Studio, Atom, Sublime, etc...)
    * **Visual Studio 2015 Update 3** already has **full support** built-in
    * See references, usages, definitions of types in your editor context

---

#### Strong Typing

* We can now define types for our variables and functions
    * Function **return** types, **variable** types, **parameter** types, function **delegate** types
* Catch errors before running, validate execution flow integrity
    * Errors appear in your IDE errors list automatically
* Easily refactor project wide files without introducing bugs
* Organize project modules within *importable* namespaces
    * Bring organization and clarity to large front end projects
* Full `jsdoc` support
    * Get intellisense within your IDE when developing

---

#### Strong Typing

A Simple Example Declaration

```ts
import * as Rx from 'rx';

export interface SearchService<T> {
  /**
   * This documentation shows up in intellisense
   * 
   * @param queryText text to search for
   * @param skip number of records to skip from the beginning (paging)
   * @param take number of records to return (exclude for all records)
   */
  getResults(queryText: string, skip?: number, take?: number): Rx.Observable<T[]>; 
}

export class SearchImpl<T> {
  constructor(private service: SearchService<T>) {
  }

  public search(queryText: string, skip?: number, take?: number) {
    return this.service.getResults(queryText, skip, take);
  }
}
```

---

#### Strong Typing

A Simple Example Implementation

```ts
import * as Rx from 'rx';

const DumbSearchService = <SearchService<string>>{
  getResults(queryText: string, skip = 0, take = 0) {
    var result = Rx.Observable
      .return([ 'ABC', 'BCD', 'CDE' ])
      .select(x => x.filter(y => y.includes(queryText)));

    if (skip > 0) {
      result = result.skip(skip);
    }

    if (take > 0) {
      result = result.take(take);
    }
  }
};

const DumbSearch = new SearchImpl(DumbSearchService);
const result = DumbSearch.search('B', 1, 2);
// result = async [ 'BCD' ]
```

---

#### 3rd Party Library integration

* Describe **JavaScript** libraries with *type definitions*
* Use `typings` `npm` module to install well-known typings
    * Many popular typings already exist
* Write your own custom typings for any other library (example below)

```ts
// mylib.d.ts

declare namespace MyLib {
  export interface SearchService<T> {
    getResults(queryText: string, skip?: number, take?: number): Rx.Observable<T[]>;
  }

  export class SearchImpl<T> {
    public search(queryText: string, skip?: number, take?: number): Rx.Observable<T[]>;
  }
}

declare module 'mylib' {
  export = MyLib;
}
```

note:
    none
