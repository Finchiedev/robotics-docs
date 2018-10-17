Code structure
==============

The structural rules for the code are simple, and go as follows: ::

    README.md is for users to get started
    main.js is for the Electron renderer process
    package.json & package-lock.json are for NPM use
    .travis.yml & .circleci/ are for CI
    App/*.html is for all HTML files
    App/CSS/*.css is for all CSS files used by the HTML pages
    App/JS/*.js is for all JavaScript files used by the HTML pages
    App/JS/Resources/ is for NodeJS resources
