# arduino-php-wrapper

If you are wondering how to control the Arduino serial port via PHP, here is the solution. 
The **arduino://** wrapper is a easy and straightforward way to write and read data from Arduino.

## Usage

to write date on Arduino serial just use the regular I/O functions in PHP such as **fwrite** or file_put_contents**

``` php
//reads data from Arduino
$resource = fopen('arduino://ttyUSB0', 'r+');
print fread($resource, 1024); 
```

Or if you prefer, you can use **file_get_contents** and get the same result
``` php
print file_get_contents('arduinno://ttyUSB0');
```

To write data in the Arduino serial is as easy as it could be

``` php
//writes data to Arduino
$resource = fopen('arduino://ttyUSB0', 'r+');
print fwrite('hello Arduino'); 
```

``` php
print file_put_contents('hello Arduino');
```

## Improvements

As you can see is really simple and we can improve it much more as the sensors are identified