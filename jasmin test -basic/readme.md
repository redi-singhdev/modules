this is a copy of [this github project](https://github.com/JeremyMarshall/jasmine-node)

jasmine-node
============

You  need jasmine-node which is a node.js package

it puts them in a node_module directory (which is one directory up on my setup) where you run it from

>sudo npm install jasmine-node

so there will be a ../node_modules/jasmine-node/bin/jasmine-node file
currently the javascript test is in <src>/javascript/demo
and you run the tests with

>node_modules/jasmine-node/bin/jasmine-node --verbose --junitreport --noColor  spec

this creates junit output which can be loaded using the jenkins junit plugin

There is also javascript coverage using istanbul

>sudo npm install -g istanbul


-----
>> this is going to install at following location 
>>C:\Users\U6020512\AppData\Roaming\npm\istanbul -> C:\Users\U6020512\AppData\Roaming\npm\node_modules\istanbul\lib\cli.js
make sure your run the istanbul from the one installed

/usr/local/bin/istanbul -> /usr/local/lib/node_modules/istanbul/lib/cli.js
istanbul@0.2.4 /usr/local/lib/node_modules/istanbul


run the tests like this (from demo)
>>for me in folder : /c/Users/U6020512/AppData/Roaming/npm/istanbul

>/usr/local/bin/istanbul cover spec/PlayerSpec.js

>/usr/local/bin/istanbul report cobertura

##output of coverage, generated in console

(for me in folder $ /c/Users/U6020512/AppData/Roaming/npm/istanbul cover spec/PlayerSpec.js
=============================================================================
Writing coverage object [C:\work2\github\modules\jasmin test -basic\coverage\coverage.json]
Writing coverage reports at [C:\work2\github\modules\jasmin test -basic\coverage]
=============================================================================

=============================== Coverage summary ===============================
Statements   : 98.25% ( 56/57 )
Branches     : 100% ( 4/4 )
Functions    : 95% ( 19/20 )
Lines        : 98.25% ( 56/57 )
================================================================================



## output of running test, generated in console

u6020512@U6020512-TPD-A MINGW64 /c/work2/github/modules/jasmin test -basic (jasmin-test-basic)
$ node_modules/jasmine-node/bin/jasmine-node --verbose --junitreport --noColor spec

Player - 9 ms
    should be able to play a Song - 3 ms

    when song has been paused - 3 ms
        should indicate that the song is currently paused - 1 ms
        should be possible to resume - 0 ms
    tells the current song if the user has made it a favorite - 1 ms

    #resume - 1 ms
        should throw an exception if song is already playing - 1 ms

Player - 9 ms
    should be able to play a Song - 3 ms

    when song has been paused - 3 ms
        should indicate that the song is currently paused - 1 ms
        should be possible to resume - 0 ms
    tells the current song if the user has made it a favorite - 1 ms

    #resume - 1 ms
        should throw an exception if song is already playing - 1 ms

Finished in 0.032 seconds
5 tests, 8 assertions, 0 failures, 0 skipped
