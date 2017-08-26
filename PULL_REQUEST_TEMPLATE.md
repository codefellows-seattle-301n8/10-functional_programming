#### Single-line Summary
**Today, Aaron, Cole and Kyle paired together. It took about 6 hours**

#### Reflect and summarize on your process for each `TODO` item :  
admin.html
  1. <!-- TODO: Setup a template for each row of the Author Stats section of this page: -->
  Added handlebars template for author stats.
  2. <!-- TODO: Due to changes in article.js and articleView.js to attach their interior objects to a global 'app' object, we need to make changes to the contents of the following <script> tag: --><!-- // TODO: After we fetch and load all the articles, what view function do we want to run next?
  // Let's pass in a callback function, to determine what happens AFTER all articles are loaded. -->
  Added fetchAll function with articleView.initAdminPage passed in as a parameter.

index.html
  1. <!-- TODO: Due to changes in article.js and articleView.js to attach their interior objects to a global 'app' object, we need to make changes to the contents of the following <script> tag: -->
  Added fetchAll function with articleView.initIndexPage passed in as a parameter.

new.html
  1. <!-- TODO: Due to changes in article.js and articleView.js to attach their interior objects to a global 'app' object, we need to make changes to the contents of the following <script> tag: -->
  Added fetchAll function with articleView.initNewArticlePage passed in as a parameter.

article.js
  1. <!-- // TODO: Wrap the contents of this file, except for the preceding 'use strict' and 'var app...' declararions, in an IIFE.
  // Give the IIFE a parameter called 'module'.
  // At the very end of the code, but still inside the IIFE, attach the 'Article' object to 'module'.
  // Where the IIFE is invoked, pass in the global 'app' object that is defined above. -->
  Wrapped contents of file in IIFE with a parameter of module.
  2. <!-- // TODO: Refactor this forEach code, by using a `.map` call instead, since what we are trying to accomplish
  // is the transformation of one collection into another. Remember that we can set variables equal to the result
  // of functions. So if we set a variable equal to the result of a .map, it will be our transformed array.
  // There is no need to push to anything. -->
  Refactored old forEach code using .map to transform variables into an array.
  3. <!-- // TODO: Chain together a `map` and a `reduce` call to get a rough count of all words in all articles. -->
  Used body.match in the .map method to use a regexp formula to roughly calculate the number of words in each article body. Used .reduce method with parameter.length to calculate number of elements in array.
  4. <!-- // TODO: Chain together a `map` and a `reduce` call to produce an array of unique author names. You will
  // probably need to use the optional accumulator argument in your reduce call. -->
  Used author.match in the .map method to use a regexp formula to roughly calculate the number of authors. Used .reduce method with parameter.length to calculate number of elements in array.
  5. <!-- // TODO: Transform each author string into an object with properties for
  // the author's name, as well as the total number of words across all articles
  // written by the specified author.
  // HINT: This .map should be setup to return an object literal with two properties.
  // The first property should be pretty straightforward, but you will need to chain
  // some combination of filter, map, and reduce to get the value for the second
  // property. -->
  Used .filter to get total number of words per author for all articles.

articleView.js
  1. <!-- // TODO: Wrap the contents of this file, except for the preceding 'use strict' and 'var app...' declararions, in an IIFE.
  // Give the IIFE a parameter called 'module'.
  // At the very end of the code, but still inside the IIFE, attach the 'articleView' object to 'module'.
  // Where the IIFE is invoked, pass in the global 'app' object that is defined above.
  // Keep in mind that all references to 'Article' in this file now need to be renamed to 'app.Article'. There are not separate instructions for those; you'll need to debug and find them on your own. -->
  Wrapped contents of file in IIFE with a parameter of module.
  2. <!-- // TODO: Call the Handlebars `.compile` function, which will return a function for you to use where needed.
  // Make sure you assign the result of your Handlebars.compile call to a variable called "template", since
  // we are then calling "template" on line 117. -->
  Called Handlebars using .compile function.


#### Checklist (before submitting, fill in each set of square brackets with an 'x')
- [x] We have titled the Pull Request similar to our branch name (ex: 'brian-rick').
- [x] This PR includes commits from both myself and my partner; e.g. We followed good pair programming practices by switching driver/navigator roles.
- [x] There is no extraneous, unrelated code included in this PR.
- [x] We have summarized our `TODO:` process above.
