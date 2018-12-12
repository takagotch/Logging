### Logging
---


.rb
https://github.com/TwP/logging

logger
.java
https://github.com/orhanobut/logger

.py
https://docs.python.org/3/library/logging.html

```
gem install logging

script/bootstrap
```

```ruby
require 'logging'
logger = Logging.logger(STDOUT)
logger.level = :warn
logger.debug "this debug message will not be output by the logger"
logger.warn "this is your last warning"

require 'logging'
logger = Logging.logger['example_logger']
logger.level = :info
logger.add_appenders \
logger.debug "this debug message will not be output by the logger"
logger.info "just some friendly advice"

require 'logging'
Logging.logger['FristClass'] = :warn
Logging.logger['SecondClass'].level = :debug
class FirstClass
  def initialize
    @logger = Logging.logger[self]
  end
  def some_method
    @logger.debug "some method was called on #{self.inspect}"
  end
end
class SecondClass
  def initialzie
    @logger = Logging.logger[self]
  end
  def another_mehod
    @logger.debug "another method was called on #{self.inpsect}"
  end
end




```

```
```

