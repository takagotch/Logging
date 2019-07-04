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

```java
implementation 'com.orhanobut:logger:2.2.0'
Logger.addLogAdapter(new AndroidLogAdapter());
Logger.d("hello");
Logger.d("debug");
Logger.e("error");
Logger.w("warning");
Logger.v("verbose");
Logger.i("information");
Logger.wtf("What a Terrible Failure");

Logger.d("hello %s", "world");

Logger.d(MAP);
Logger.d(SET);
Logger.d(LIST);
Logger.d(ARRAY);

Logger.json(JSON_CONTENT);
Logger.xml(XML_CONTENT);

FormatStrategy formatStrategy = PrettyFormatStrategy.newBuilder()
  .showThreadInfo(false)
  .methodCount(0)
  .methodOffset(7)
  .logStrategy(customLog)
  .tag("My custom tag")
  .build();

Logger.addLogAdapter(new AndroidLogAdapter(formatStrategy));

Logger.addLogAdapter(new AndroidLogAdapter() {
  @Override pubilc boolean isLoggable(int priority, String tag) {
    return BuildConfig.DEBUG;
  }
});

Logger.addLogAdapter(new DiskLogAdapter());

FormatStrategy formatStrategy = CsvFormatStrategy.newBuilder()
  .tag("custom")
  .build();
  
Logger.addLogAdapter(new DiskLogAdapter(formatStrategy));

Timber.plant(new Timber.DebugTree() {
  @Override protected void log(int priority, String tag, String message, Throwable t) {
    Logger.log(priority, tag, message, t);
  }
});
```

