# Karma-Read-JSON
Karma helper function to make reading `JSON` files easier

## Installation

    $ bower install karma-read-json --save
    
      OR
    
    $ npm install karma-read-json --save-dev
    
      OR
    
    $ yarn add karma-read-json --dev

## Usage

### 1. Put `karma-read-json.js` in your Karma files. 

  Example (for installation through `bower`):
  

        files = [
    
          . . .
        
          'bower_components/karma-read-json/karma-read-json.js',
        
          . . .
         
        ],

  Example (for installation through `npm` or `yarn`):

        files = [
    
          . . .
        
          'node_modules/karma-read-json/karma-read-json.js',
        
          . . .
        
        ],

### 2. Make *sure* your `JSON` is being served by `Karma`. 

  Example:

        files = [
    
          . . .
    
          // Fixtures
          { 
            include: false,
            pattern: 'www/js/tests/**/*.json',
            served: true,
            watch: true
          },
    
          . . .
    
        ],

### 3. Use the `readJSON` function in your tests. 

  Example:

      var response = readJSON('www/js/tests/json/foobar.json');
    
      $httpBackend.whenGET(/api\/foo\/bar\/).respond(response);


