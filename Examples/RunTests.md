EXECUTION:
    To run all feature files:
        npx wdio wdio.conf.js

    To run a particular feature file:
        npx wdio wdio.conf.js --spec ./relative-path-of-feature-file

        eg:
        npx wdio wdio.conf.js --spec ./features/Facebook/login.feature 

    To run scenarios using tagName:
        npx wdio wdio.conf.js --cucumberOpts.tagExpression '@tag1'

        eg:
        npx wdio wdio.conf.js --cucumberOpts.tagExpression '@imp'
        npx wdio wdio.conf.js --cucumberOpts.tagExpression '@login-2 or @imp'
        npx wdio wdio.conf.js --cucumberOpts.tagExpression '@login-2 and @imp'
        npx wdio wdio.conf.js --cucumberOpts.tagExpression 'not @login'



LOCAL TESTING WITH CHROME DRIVER
        npx wdio config/wdio.conf.js
        npx wdio config/wdio.conf.js --spec ./features/Facebook/login.feature
        npx wdio config/wdio.conf.js --spec ./features/Darksky/timeline.feature
        
LOCAL CROSS-BROWSER TESTING
        npx wdio config/wdio.conf-cb.js
        npx wdio config/wdio.conf-cb.js --spec ./features/Facebook/login.feature

REMOTE BROWSERSTACK TESTING
        npx wdio config/wdio.conf-bstk.js
        npx wdio config/wdio.conf-bstk.js --spec ./features/Facebook/login.feature

PORT 4444 IS ALREADY IN USE
        kill $(lsof -t -i:4444)

ALLURE COMMANDS
    allure generate
    allure open
    allure generate  --clean && allure open