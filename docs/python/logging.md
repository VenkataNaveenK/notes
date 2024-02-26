# The Logging module
The logging module in Python is a ready-to-use and powerful module that is designed to meet the needs of beginners as well as enterprise teams. It is used by most of the third-party Python libraries, so you can integrate your log messages with the ones from those libraries to produce a homogeneous log for your application.

Adding logging to your Python program is as easy as this:
```py
import logging
```
## Levels
With the logging module imported, you can use something called a “logger” to log messages that you want to see. By default, there are 5 standard levels indicating the severity of events. Each has a corresponding function that can be used to log events at that level of severity. 

The defined levels, in order of increasing severity, are the following:

* DEBUG
* INFO
* WARNING
* ERROR
* CRITICAL

```py
import logging

logging.debug('This is a debug message')
logging.info('This is an info message')
logging.warning('This is a warning message')
logging.error('This is an error message')
logging.critical('This is a critical message')
```
output:
```shell
WARNING:root:This is a warning message
ERROR:root:This is an error message
CRITICAL:root:This is a critical message
```
Notice that the debug() and info() messages didn’t get logged. This is because, by default, the logging module logs the messages with a severity level of WARNING or above. You can change that by configuring the logging module to log events of all levels if you want. You can also define your own severity levels by changing configurations, but it is generally not recommended as it can cause confusion with logs of some third-party libraries that you might be using.
## Basic Configurations
You can use the basicConfig(**kwargs) function to configure the logging.
Some of the commonly used parameters for basicConfig() are the following:

* level: The root logger will be set to the specified severity level.
* filename: This specifies the file.
* filemode: If filename is given, the file is opened in this mode. The default is a, which means append.
* format: This is the format of the log message.

By using the level parameter, you can set what level of log messages you want to record. This can be done by passing one of the constants available in the class, and this would enable all logging calls at or above that level to be logged. Here’s an example:
```py
import logging

logging.basicConfig(level=logging.DEBUG)
logging.debug('This will get logged')
```
```shell title='output'
DEBUG:root:This will get logged
```
All events at or above DEBUG level will now get logged.

Similarly, for logging to a file rather than the console, filename and filemode can be used, and you can decide the format of the message using format. The following example shows the usage of all three:
```py
import logging

logging.basicConfig(filename='app.log', filemode='w', format='%(name)s - %(levelname)s - %(message)s')
logging.warning('This will get logged to a file')
```
```shell title='output'
root - ERROR - This will get logged to a file
```
The message will look like this but will be written to a file named app.log instead of the console. The filemode is set to w, which means the log file is opened in “write mode” each time basicConfig() is called, and each run of the program will rewrite the file. The default configuration for filemode is a, which is append.
## Formatting the Output
### Showing process id and levelname
```py
import logging

logging.basicConfig(format='%(process)d-%(levelname)s-%(message)s')
logging.warning('This is a Warning')
```
```shell title='output'
18472-WARNING-This is a Warning
```
### Showing asctime and message
```py
import logging

logging.basicConfig(format='%(asctime)s - %(message)s', level=logging.INFO)
logging.info('Admin logged in')
```
```shell title='output'
2018-07-11 20:12:06,288 - Admin logged in
```
### Formatting asctime
```py
import logging

logging.basicConfig(format='%(asctime)s - %(message)s', datefmt='%d-%b-%y %H:%M:%S')
logging.warning('Admin logged out')
```
```shell title='output'
12-Jul-18 20:53:19 - Admin logged out
```
## Logging variable data
```py
import logging

name = 'John'

logging.error('%s raised an error', name)
```
```shell title='output'
ERROR:root: John raised an error
```
## Example
```py
# Importing module
import logging

# Create and configure logger
logging.basicConfig(
        # filename="std.log",
        format="%(asctime)s %(levelname)s: %(message)s",
        # filemode="w"
        )

# Creating an object
logger = logging.getLogger()

# Setting the threshold of logger to DEBUG
logger.setLevel(logging.DEBUG)

# Test messages
logger.debug("Harmless debug Message")
logger.info("Just an information")
logger.warning("Its a Warning")
logger.error("Did you try to divide by zero")
logger.critical("Internet is down")
```
```shell title='output'
2024-02-26 16:39:14,915 DEBUG: Harmless debug Message
2024-02-26 16:39:14,915 INFO: Just an information
2024-02-26 16:39:14,916 WARNING: Its a Warning
2024-02-26 16:39:14,916 ERROR: Did you try to divide by zero
2024-02-26 16:39:14,916 CRITICAL: Internet is down
```
