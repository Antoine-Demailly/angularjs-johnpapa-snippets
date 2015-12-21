# AngularJS John Papa snippets for Atom

A set of AngularJS snippets based on [John Papa's style guide].

### Snippets

You can use the following snippets in JavaScript files.

##### ngmodule
``` javascript
(function() {
  'use strict';

  angular
    .module('${1:module}', [
        '${2:dependencies}'
    ]);
})();
```

##### ngcontroller
``` javascript
(function() {
  'use strict';

  angular
    .module('${1:module}')
    .controller('${2:Controller}', ${2:Controller});

  ${2:Controller}.$inject = ['${3:dependencies}'];

  /* @ngInject */
  function ${2:Controller}(${3:dependencies}) {
    var vm = this;

    vm.${4:example} = ${4:example};

    function ${4:example}() {

    }
  }
})();
```

##### ngfactory
``` javascript
(function() {
  'use strict';

  angular
    .module('${1:module}')
    .factory('${2:factory}', ${2:factory});

  ${2:factory}.$inject = ['${3:dependencies}'];

  /* @ngInject */
  function ${2:factory}(${3:dependencies}) {
    var service = {
      ${4:function}: ${4:function}
    };

    return service;

    function ${4:function}() {

    }
  }
})();
```

##### ngdirective
``` javascript
(function() {
  'use strict';

  angular
    .module('${1:module}')
    .directive('${2:directive}', ${2:directive});

  /* @ngInject */
  function ${2:directive}() {
    var directive = {
      restrict: '${3:EA}',
      templateUrl: '${4:templateUrl}',
      scope: {
      },
      link: linkFunc,
      controller: ${5:Controller},
      controllerAs: 'vm',
      bindToController: true
    };

    return directive;

    function linkFunc(scope, el, attr, ctrl) {

    }
  }

  ${5:Controller}.$inject = ['${6:dependencies}'];

  /* @ngInject */
  function ${5:Controller}(${6:dependencies}) {
    var vm = this;

    activate();

    function activate() {

    }
  }
})();
```

##### ngservice
``` javascript
(function() {
  'use strict';

  angular
    .module('${1:module}')
    .service('${2:Service}', ${2:Service});

  ${2:Service}.$inject = ['${3:dependencies}'];

  /* @ngInject */
  function ${2:Service}(${3:dependencies}) {
    var vm = this;

    vm.${4:function} = ${4:function};

    function ${4:function}() {

    }
  }
})();
```

##### ngfilter
``` javascript
(function() {
  'use strict';

  angular
    .module('${1:module}')
    .filter('${2:filter}', ${2:filter});

  function ${2:filter}() {
    return ${2:filter}Filter

    function ${2:filter}Filter(${3:params}) {
      return ${3:params};
    }
  }
})();
```


[john papa's style guide]: <https://github.com/johnpapa/angular-styleguide>
